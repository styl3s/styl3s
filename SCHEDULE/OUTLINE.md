# CCNA 200-301 — 45-Day Training Plan Outline

## Diagnostic Assessment (2026-09-18)

Background: general IT knowledge, attempted the CCNA once before (2021,
did not pass), no fixed exam date, variable daily study time, has Cisco
Packet Tracer for labs.

32 diagnostic questions were asked across two rounds (a 20-question spread
quiz, then 12 follow-up questions targeting weak/uncertain areas).

| Domain (blueprint weight) | Score | Read |
|---|---|---|
| IP Connectivity (~25%) | 4/11 (36%) | Weakest domain AND heaviest-weighted. Core gaps: administrative distance, distance-vector vs. link-state classification, inter-VLAN routing (SVI vs. trunk), default routes, FHRP. |
| IP Services (~10%) | 1/3 (33%) | DHCP process order and NAT vs. PAT both missed. |
| Network Fundamentals (~20%) | 4/7 (57%) | Subnetting mechanics are inconsistent (missed /30 host count), IPv6 basics and cabling/auto-MDIX shaky but improving. |
| Network Access (~20%) | 3/5 (60%) | VLAN/trunking basics solid; STP purpose and native VLAN purpose both missed. |
| Security Fundamentals (~15%) | 3/3 (100%) | Strong — ACLs, port security, VPN concepts all correct. |
| Automation and Programmability (~10%) | 3/3 (100%) | Strong — REST APIs, YAML, SDN/controller concepts all correct. |

**Weighting decision:** IP Connectivity gets by far the most days (it's
both the biggest exam domain and the biggest gap). Network Fundamentals
and Network Access get solid but shorter blocks to fix specific holes.
IP Services gets a focused block despite its smaller exam weight, because
the gap there is large. Security and Automation get light review only
since Ben is already scoring 100% — no need to over-invest there.

## Day-by-Day Map

### IP Connectivity — Days 1-12 (heaviest focus)

| Day | Topic |
|---|---|
| 01 | Routing fundamentals — how routers forward packets, anatomy of the routing table |
| 02 | Static routing — standard static routes and default routes (0.0.0.0/0) |
| 03 | Administrative distance and route selection between sources |
| 04 | Floating static routes and backup path design |
| 05 | Distance-vector vs. link-state routing protocols |
| 06 | RIP overview (legacy distance-vector protocol) |
| 07 | EIGRP fundamentals and metrics |
| 08 | OSPF fundamentals (single area) — router ID, neighbor states |
| 09 | OSPF network types and DR/BDR election |
| 10 | OSPF configuration and verification commands |
| 11 | Inter-VLAN routing — router-on-a-stick vs. SVI |
| 12 | FHRP (HSRP/VRRP/GLBP) and route summarization — IP Connectivity review |

### Network Fundamentals — Days 13-20

| Day | Topic |
|---|---|
| 13 | OSI model and TCP/IP stack |
| 14 | Cabling and connectors, including auto-MDIX |
| 15 | IPv4 addressing and subnetting review |
| 16 | VLSM (variable-length subnet masking) |
| 17 | IPv6 addressing types and subnetting |
| 18 | Wireless fundamentals — 802.11 standards and frequencies |
| 19 | Network topologies and virtualization concepts |
| 20 | Network Fundamentals review and practice questions |

### Network Access — Days 21-28

| Day | Topic |
|---|---|
| 21 | VLANs deep dive |
| 22 | Trunking, 802.1Q, and the native VLAN |
| 23 | Spanning Tree Protocol fundamentals and port states |
| 24 | RSTP, PortFast, and BPDU Guard |
| 25 | EtherChannel |
| 26 | Wireless architecture — WLC and AP modes |
| 27 | Wireless security — WPA2, WPA3, 802.1X |
| 28 | Network Access review and practice questions |

### IP Services — Days 29-34

| Day | Topic |
|---|---|
| 29 | DHCP deep dive |
| 30 | DNS fundamentals |
| 31 | NAT and PAT deep dive |
| 32 | NTP and syslog |
| 33 | SNMP and QoS basics |
| 34 | IP Services review and practice questions |

### Security Fundamentals — Days 35-38 (light review, already strong)

| Day | Topic |
|---|---|
| 35 | Security concepts and common threats |
| 36 | ACLs deep dive |
| 37 | Port security and DHCP snooping |
| 38 | VPN concepts and Security Fundamentals review |

### Automation and Programmability — Days 39-41 (light review, already strong)

| Day | Topic |
|---|---|
| 39 | Automation concepts and controller-based networking (SDN) |
| 40 | APIs and data formats (JSON/YAML) |
| 41 | Automation tools overview (Ansible/Puppet/Chef) and review |

### Final Review — Days 42-45

| Day | Topic |
|---|---|
| 42 | Mixed-domain review 1 (weighted toward IP Connectivity + IP Services) |
| 43 | Mixed-domain review 2 (weighted toward Network Fundamentals + Network Access) |
| 44 | Full-length practice exam |
| 45 | Final review and weak-area cleanup, based on practice exam results |

## Living Document Note

This outline is the master reference. Each day's session file is
generated just-in-time (not all 45 in advance) from this outline plus
whatever has been learned about Ben's progress since — so later days,
and this table itself, may shift slightly (e.g. more days added to a
domain that turns out to need it) based on how earlier days go.
