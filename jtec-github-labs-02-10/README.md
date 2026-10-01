# JTEC Network Engineering Lab Portfolio — Labs 02–10

Hands-on Cisco networking portfolio built in Cisco Packet Tracer.
The project documents practical network design, configuration,
verification and troubleshooting.

## Current scope

This package documents Labs 02–10:

| Lab | Project | Status |
|---|---|---|
| 02 | IPv4 VLSM & Subnetting | Complete |
| 03 | IPv6 Dual-Stack Networking | Complete |
| 04 | Cisco IOS Security & SSH | Complete |
| 05 | Interface & Connectivity Troubleshooting | Complete |
| 06 | VLAN Configuration | Complete |
| 07 | 802.1Q Trunking | Complete |
| 08 | Inter-VLAN Routing & SVIs | Complete |
| 09 | Network Discovery & Verification | Complete |
| 10 | LACP EtherChannel | Complete |

## Portfolio methodology

Each lab follows:

**Plan → Configure → Verify → Troubleshoot → Test → Document**

The portfolio focuses on evidence of practical skills rather than only listing technologies.

## Core technologies demonstrated

- IPv4 addressing and VLSM
- IPv6 addressing and routing
- VLAN segmentation
- Access ports
- 802.1Q trunking
- Native VLANs
- Layer 3 switching
- Switch Virtual Interfaces (SVIs)
- Inter-VLAN routing
- Cisco IOS device security
- SSH
- CDP
- EtherChannel
- LACP
- Basic STP verification
- Structured Layer 1/Layer 2/Layer 3 troubleshooting

## Network architecture

The JTEC environment uses redundant core switches and multiple access switches.

```text
                         JTEC ENTERPRISE NETWORK

                         +----------------+
                         |     CORE1      |
                         |   L3 SWITCH    |
                         +-------+--------+
                                 ||
                          LACP EtherChannel
                                 ||
                         +-------+--------+
                         |     CORE2      |
                         |   L3 SWITCH    |
                         +---+----+----+--+
                             |    |    |
                         ACCESS1 ACCESS3 ACCESS4
                             |
                         ACCESS2

                    End devices connect at access layer
```

Documented core/access links include:

- ACCESS1 Gi0/1 → CORE1 Gi1/4
- ACCESS2 Gi0/1 → CORE1 Gi1/5
- ACCESS3 Gi0/1 → CORE2 Gi1/4
- ACCESS4 Gi0/1 → CORE2 Gi1/5
- CORE1 Gi1/6–Gi1/7 ↔ CORE2 Gi1/7–Gi1/8

The CORE1–CORE2 links are later combined into Port-Channel1 using LACP.

## VLAN architecture

| VLAN | Name |
|---:|---|
| 10 | MANAGEMENT |
| 20 | USERS |
| 30 | SALES |
| 40 | FINANCE |
| 50 | SERVERS |
| 60 | VOICE |
| 70 | GUEST |
| 80 | NET-MGMT |
| 99 | NATIVE |

The standard trunk configuration carries:

`10,20,30,40,50,60,70,80,99`

with VLAN 99 used as the native VLAN.

## Evidence

Each lab folder contains:

- Lab README
- Configuration examples
- Verification commands
- Troubleshooting methodology
- Lessons learned
- Space for screenshots
- Space for the relevant `.pkt` file

> The `.pkt` files and screenshots must be copied from the user's own Packet Tracer project. This package does not fabricate those files.

## Career relevance

The labs are designed to demonstrate practical skills relevant to:

- Junior NOC Engineer
- Network Support Engineer
- Junior Network Administrator
- Network Operations roles
- Data Centre Technician roles with networking responsibilities

## Disclaimer

This is a personal lab environment. It should not be presented as production experience.
