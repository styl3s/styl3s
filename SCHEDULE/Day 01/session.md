# Day 01 of 45 — Routing Fundamentals

**Domain:** IP Connectivity (~25% of exam) — your weakest and highest-weighted domain, so this is where we start.

**Exam objectives covered:** 3.1 (interpret the components of a routing table), 3.2 (determine how a router makes a forwarding decision by default).

**Time:** Core section ~35-45 min. Optional deeper section at the end if you have more time today — skip it if you don't, we'll circle back later.

---

## Why this day, first

In your diagnostic, IP Connectivity scored 36% — the lowest of any domain — and it's the single biggest chunk of the real exam. Several later mix-ups (administrative distance, default routes, FHRP) all trace back to not having a rock-solid mental model of *what a routing table actually is and how a router uses it*. That's today's entire goal. Everything for the next 11 days builds on this.

## Core Concept: What a Router Actually Does

A router's job, at its core, is simple: **for every packet, look at the destination IP address, find the best matching entry in the routing table, and forward the packet out the interface that entry points to.** That's it. Everything else (routing protocols, administrative distance, summarization) exists to answer one question: *how does that table get built and kept accurate?*

### The Routing Table

Run `show ip route` on any Cisco router and you'll see entries like this:

```
Codes: C - connected, S - static, O - OSPF, D - EIGRP, * - candidate default

Gateway of last resort is 203.0.113.1 to network 0.0.0.0

O    10.0.0.0/24 [110/20] via 192.168.1.2, 00:12:33, GigabitEthernet0/1
C    192.168.1.0/24 is directly connected, GigabitEthernet0/1
L    192.168.1.1/32 is directly connected, GigabitEthernet0/1
S*   0.0.0.0/0 [1/0] via 203.0.113.1
```

Break down each entry:

- **Code letter** — how the router learned this route: `C` = directly connected, `L` = local (the router's own interface IP, a /32), `S` = static (manually configured), `O` = OSPF, `D` = EIGRP, `R` = RIP, `B` = BGP.
- **Network/prefix** (`10.0.0.0/24`) — the destination network this entry matches.
- **`[110/20]`** — two numbers in brackets: **administrative distance** (110 = OSPF's default trust rating) and **metric** (20 = OSPF's cost to reach it). We'll cover AD in depth on Day 03 — for today just know it exists and is separate from the metric.
- **`via 192.168.1.2`** — the next-hop IP address to forward toward.
- **Outgoing interface** — which physical/logical interface to send the packet out of.

### How a Router Picks the Best Route

When a packet arrives, the router doesn't just grab any matching route — it applies two rules in order:

1. **Longest prefix match wins.** If both `10.0.0.0/24` and `10.0.0.0/16` are in the table and the packet is going to `10.0.0.5`, the router picks the `/24` because it's more specific. This is true regardless of how the route was learned.
2. **If there's a genuine tie in prefix length**, only then does administrative distance (which *source* is more trusted) and metric (which *path* is best within that source) come into play. We'll dig into this on Day 03.

If **no route matches at all** — not even a default route — the router drops the packet and (usually) sends back an ICMP "destination unreachable" message.

### Directly Connected and Local Routes

The two route types you *don't* have to configure a protocol for:

- **Connected (`C`)** — appears automatically the instant an interface is up/up with an IP address configured. This is the network the interface itself lives on.
- **Local (`L`)** — a /32 (host route) for the interface's own exact IP address. This exists so the router can efficiently recognize traffic destined *to itself* versus traffic that just needs to be *routed through* it.

Every other route type (static, OSPF, EIGRP, RIP, BGP) has to be either manually configured or learned dynamically from a neighboring router — nothing "just appears" beyond connected/local.

## Quick Self-Check

Answer these before moving on (no need to write anything down, just think them through):

1. A router has both `172.16.0.0/16` and `172.16.5.0/24` in its table. A packet arrives for `172.16.5.10`. Which route does it use, and why?
2. What's the difference between a `C` route and an `L` route for the same interface?
3. If a router receives a packet for a network with no matching entry in the routing table at all, what happens to it?

<details>
<summary>Answers (click to expand mentally / check after you've answered)</summary>

1. The `/24` — longest prefix match always wins regardless of source.
2. `C` is the connected subnet itself; `L` is the /32 host route for the router's own interface address on that subnet.
3. It's dropped, and the router typically sends an ICMP destination-unreachable message back to the source.

</details>

## Hands-On Lab (Packet Tracer)

1. Open Packet Tracer and build a simple topology: **PC1 — Router1 — PC2**, with Router1 having two interfaces, each on a different subnet (e.g. `192.168.1.0/24` and `192.168.2.0/24`).
2. Configure the IP addresses on both router interfaces and both PCs, and bring the interfaces up (`no shutdown`).
3. Run `show ip route` on Router1. You should see two `C` entries and two `L` entries — nothing else yet, since no static routes or protocols are configured.
4. From PC1, ping PC2. It should work — both are directly connected to the same router. Ping the router's own interface IPs too, and notice both work via the `L` routes.
5. Add a third router (Router2) connected to Router1, with a third subnet on the far side. Configure IPs but do **not** add any static routes or routing protocol yet.
6. Try to ping from PC1 across to a PC on Router2's subnet — it will **fail**. Run `show ip route` on Router1 again and confirm there's genuinely no route to that far subnet. This is the setup for Day 02, where you'll fix this with static routes.

## Summary — What You Learned Today

- A router forwards every packet based on the single best match in its routing table — nothing more mysterious than that.
- Longest prefix match always decides between routes to different-sized networks; administrative distance and metric only break ties between equally-specific routes (more on this Day 03).
- Connected (`C`) and Local (`L`) routes appear automatically from interface configuration; every other route type must be configured or learned.
- You built a topology in Packet Tracer and directly observed a router with no route to a destination dropping traffic — the exact problem static routing (tomorrow) solves.

**You have completed DAY 1 of your 45 day training plan!**
