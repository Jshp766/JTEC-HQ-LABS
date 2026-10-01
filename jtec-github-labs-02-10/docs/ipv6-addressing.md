# JTEC IPv6 Addressing Plan

The JTEC IPv6 design uses:

`2001:DB8:10::/48`

Each VLAN receives a `/64`.

| VLAN | IPv6 Prefix | Example SVI |
|---:|---|---|
| 10 | 2001:DB8:10:10::/64 | 2001:DB8:10:10::1/64 |
| 20 | 2001:DB8:10:20::/64 | 2001:DB8:10:20::1/64 |
| 30 | 2001:DB8:10:30::/64 | 2001:DB8:10:30::1/64 |
| 40 | 2001:DB8:10:40::/64 | 2001:DB8:10:40::1/64 |
| 50 | 2001:DB8:10:50::/64 | 2001:DB8:10:50::1/64 |
| 60 | 2001:DB8:10:60::/64 | 2001:DB8:10:60::1/64 |
| 70 | 2001:DB8:10:70::/64 | 2001:DB8:10:70::1/64 |
| 80 | 2001:DB8:10:80::/64 | 2001:DB8:10:80::1/64 |
| 99 | 2001:DB8:10:99::/64 | 2001:DB8:10:99::1/64 |

CORE1 uses:

```cisco
ipv6 unicast-routing
```

IPv6 verification:

```cisco
show ipv6 interface brief
show ipv6 route
ping <ipv6-address>
```

IPv6 uses Neighbor Discovery Protocol (NDP) rather than ARP.
