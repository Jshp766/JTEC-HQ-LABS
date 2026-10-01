# JTEC IPv4 Addressing Plan

The JTEC lab uses the `10.10.0.0/16` private address space with VLSM.

| Network | Subnet | Gateway / SVI |
|---|---|---|
| Guest / VLAN 70 | 10.10.0.0/24 | 10.10.0.1 |
| Users / VLAN 20 | 10.10.1.0/25 | 10.10.1.1 |
| Voice / VLAN 60 | 10.10.1.128/25 | 10.10.1.129 |
| Sales / VLAN 30 | 10.10.2.0/26 | 10.10.2.1 |
| Servers / VLAN 50 | 10.10.2.64/26 | 10.10.2.65 |
| Management / VLAN 10 | 10.10.2.128/27 | 10.10.2.129 |
| Finance / VLAN 40 | 10.10.2.160/27 | 10.10.2.161 |
| Network Management / VLAN 80 | 10.10.2.192/27 | 10.10.2.193 |
| R&D | 10.10.2.224/27 | 10.10.2.225* |
| Native / VLAN 99 | 10.10.99.0/27 | 10.10.99.1 |

\* Use the exact R&D gateway from the final Packet Tracer configuration if it differs.

## Lab 2 example subnetting evidence

Example calculation:

`10.10.2.224/27`

- Subnet mask: `255.255.255.224`
- Network: `10.10.2.224`
- Usable range: `10.10.2.225–10.10.2.254`
- Broadcast: `10.10.2.255`

## Verification

```text
show ip interface brief
show ip route
```
