# Lab 03 — IPv6 Dual-Stack Networking

## Objective

Introduce IPv6 alongside the existing IPv4 design and configure the core Layer 3 infrastructure for IPv6 forwarding.

## IPv6 addressing

Base prefix:

`2001:DB8:10::/48`

Each VLAN uses a `/64`.

Example:

```cisco
interface Vlan10
 ipv6 address 2001:DB8:10:10::1/64
```

## IPv6 routing

```cisco
ipv6 unicast-routing
```

This enables IPv6 packet forwarding on the Layer 3 switch.

## Verification

```cisco
show ipv6 interface brief
show ipv6 route
ping <ipv6-address>
```

## Troubleshooting

The lab included checking IPv6 addressing and correcting an addressing issue affecting the Sales network.

## Key concept

IPv6 uses Neighbor Discovery Protocol (NDP) for neighbour discovery and address resolution rather than ARP.

## Skills demonstrated

- IPv6 addressing
- `/64` subnetting
- Dual-stack networking
- NDP concepts
- IPv6 routing
- IPv6 troubleshooting

## Evidence to upload

- Packet Tracer topology screenshot
- `show ipv6 interface brief`
- `show ipv6 route`
- Successful IPv6 ping
- Final `.pkt` file
