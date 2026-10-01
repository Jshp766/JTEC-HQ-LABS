# Cisco Troubleshooting Command Reference

## Interface status

```cisco
show ip interface brief
show interfaces
show interfaces status
```

## VLANs

```cisco
show vlan brief
show interfaces GigabitEthernet0/10 switchport
```

## Trunks

```cisco
show interfaces trunk
```

## Discovery

```cisco
show cdp neighbors
show cdp neighbors detail
```

## MAC and ARP

```cisco
show mac address-table
show arp
```

## Routing

```cisco
show ip route
show ipv6 route
```

## EtherChannel

```cisco
show etherchannel summary
show interfaces port-channel 1
```

## STP

```cisco
show spanning-tree
show spanning-tree vlan 20
```

## Connectivity

```cisco
ping <destination>
traceroute <destination>
```

## Troubleshooting workflow

1. Confirm the reported symptom.
2. Check physical/interface state.
3. Check VLAN membership.
4. Check trunk status.
5. Check MAC learning.
6. Check IP addressing.
7. Check ARP/IPv6 neighbour information.
8. Check routing.
9. Check the relevant Layer 2 control protocol.
10. Make the smallest appropriate change.
11. Re-test.
12. Document the root cause and resolution.
