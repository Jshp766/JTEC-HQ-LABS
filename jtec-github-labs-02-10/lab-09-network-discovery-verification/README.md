# Lab 09 — Network Discovery & Verification

## Objective

Use Cisco discovery and verification commands to understand the physical/logical topology and validate switch interconnections.

## Documented topology

```text
ACCESS1 Gi0/1 → CORE1 Gi1/4
ACCESS2 Gi0/1 → CORE1 Gi1/5
ACCESS3 → CORE1/CORE2 topology as identified through discovery
ACCESS4 Gi0/1 → CORE2 Gi1/4
CORE1 ↔ CORE2 redundant links
```

CDP was used to identify neighbouring Cisco devices and interfaces.

## Verification commands

```cisco
show cdp neighbors
show cdp neighbors detail
show interfaces trunk
show interfaces status
show vlan brief
```

## Trunk design

The core/access trunk environment uses:

- Native VLAN 99
- Allowed VLANs 10,20,30,40,50,60,70,80,99

## Why this matters operationally

CDP and interface verification are useful when documenting an unfamiliar network, checking physical/logical connections and confirming that a switch's understanding of the topology matches the intended design.

## Skills demonstrated

- Network discovery
- CDP
- Interface mapping
- Trunk verification
- Topology documentation
- Cisco IOS show commands
