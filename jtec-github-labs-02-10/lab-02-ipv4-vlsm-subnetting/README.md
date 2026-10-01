# Lab 02 — IPv4 VLSM & Subnetting

## Objective

Design an IPv4 addressing plan using VLSM from the `10.10.0.0/16` private address space.

The lab establishes the addressing foundation used by later VLAN and Layer 3 labs.

## Network design

| Network | VLAN | Subnet |
|---|---:|---|
| Guest | 70 | 10.10.0.0/24 |
| Users | 20 | 10.10.1.0/25 |
| Voice | 60 | 10.10.1.128/25 |
| Sales | 30 | 10.10.2.0/26 |
| Servers | 50 | 10.10.2.64/26 |
| Management | 10 | 10.10.2.128/27 |
| Finance | 40 | 10.10.2.160/27 |
| Net-Mgmt | 80 | 10.10.2.192/27 |
| R&D | — | 10.10.2.224/27 |
| Native | 99 | 10.10.99.0/27 |

## Subnetting example

For `10.10.2.224/27`:

- Mask: `255.255.255.224`
- Network: `10.10.2.224`
- Usable: `10.10.2.225–10.10.2.254`
- Broadcast: `10.10.2.255`

## Verification

Use the addressing table and verify later SVI/interface configuration with:

```cisco
show ip interface brief
show ip route
```

## Skills demonstrated

- IPv4 subnetting
- VLSM
- Network/broadcast identification
- Usable host calculation
- Address planning
- Documentation

## Lessons learned

VLSM allows address space to be allocated according to the size of each network rather than assigning the same subnet size everywhere.
