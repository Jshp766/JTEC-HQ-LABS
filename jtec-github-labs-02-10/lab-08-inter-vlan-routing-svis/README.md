# Lab 08 — Inter-VLAN Routing & SVIs

## Objective

Enable communication between VLANs using Switch Virtual Interfaces (SVIs) on a Layer 3 core switch.

## Layer 3 configuration

CORE1:

```cisco
ip routing
ipv6 unicast-routing
```

## SVI addressing

| VLAN | IPv4 SVI | IPv6 SVI |
|---:|---|---|
| 10 | 10.10.2.129/27 | 2001:D88:10:10::1/64 |
| 20 | 10.10.1.1/25 | 2001:D88:10:20::1/64 |
| 30 | 10.10.2.1/26 | 2001:D88:10:30::1/64 |
| 40 | 10.10.2.161/27 | 2001:D88:10:40::1/64 |
| 50 | 10.10.2.65/26 | 2001:D88:10:50::1/64 |
| 60 | 10.10.1.129/25 | 2001:D88:10:60::1/64 |
| 70 | 10.10.0.1/24 | 2001:D88:10:70::1/64 |
| 80 | 10.10.2.193/27 | 2001:D88:10:80::1/64 |
| 99 | 10.10.99.1/27 | 2001:D88:10:99::1/64 |

Example:

```cisco
interface Vlan40
 ip address 10.10.2.161 255.255.255.224
 ipv6 address 2001:D88:10:40::1/64
 no shutdown
```

## Key concept

An SVI provides a Layer 3 gateway for a VLAN. The VLAN does not require a physical switch port to have the gateway IP assigned to it.

The physical switch ports continue to provide Layer 2 connectivity, while the SVI provides the Layer 3 gateway.

## Troubleshooting scenario

A Finance endpoint could not reach the required server network.

The investigation involved checking:

```cisco
show interfaces trunk
show vlan brief
show ip interface brief
show ip route
```

The issue was traced to the Layer 2 uplink/trunk path and corrected before connectivity testing was repeated.

## Verification

Test:

```text
Finance endpoint → Finance gateway
Finance endpoint → Server network
```

Use:

```cisco
ping <gateway>
ping <server>
```

## Skills demonstrated

- Layer 3 switching
- SVI configuration
- Inter-VLAN routing
- IPv4/IPv6 gateways
- Trunk-path troubleshooting
- End-to-end connectivity testing
