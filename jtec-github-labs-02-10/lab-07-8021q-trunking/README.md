# Lab 07 — 802.1Q Trunking

## Objective

Configure switch-to-switch trunking so multiple VLANs can traverse a single physical link.

## Trunk requirements

- 802.1Q trunking
- Native VLAN 99
- Allowed VLANs 10,20,30,40,50,60,70,80,99

## Example configuration

```cisco
interface GigabitEthernet1/4
 switchport mode trunk
 switchport trunk native vlan 99
 switchport trunk allowed vlan 10,20,30,40,50,60,70,80,99
```

## Verification

```cisco
show interfaces trunk
```

Check:

- Operational mode
- Native VLAN
- Allowed VLANs
- Active VLANs
- Forwarding VLANs

## Troubleshooting scenario

A deliberate native-VLAN mismatch was introduced and investigated.

The troubleshooting principle was to compare the native VLAN configured on both ends of the trunk.

Both ends should use:

```text
Native VLAN 99
```

## Skills demonstrated

- 802.1Q trunking
- Native VLANs
- Allowed VLAN lists
- Switch uplink configuration
- Trunk troubleshooting
- Layer 2 verification
