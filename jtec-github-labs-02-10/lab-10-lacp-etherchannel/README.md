# Lab 10 — LACP EtherChannel

## Objective

Combine multiple physical links between CORE1 and CORE2 into a single logical Port-Channel using LACP.

The objective was to provide link redundancy and simplify Layer 2/STP operation by presenting the bundled links as one logical connection.

## Physical links

The lab uses two physical Gigabit links between the core switches:

```text
CORE1 Gi1/6 ───────── CORE2 Gi1/7
CORE1 Gi1/7 ───────── CORE2 Gi1/8
```

These links form:

```text
Port-Channel1
```

## LACP configuration

CORE1:

```cisco
interface range GigabitEthernet1/6 - 7
 channel-group 1 mode active
```

CORE2:

```cisco
interface range GigabitEthernet1/7 - 8
 channel-group 1 mode active
```

## Port-Channel configuration

```cisco
interface Port-channel1
 switchport mode trunk
 switchport trunk native vlan 99
 switchport trunk allowed vlan 10,20,30,40,50,60,70,80,99
```

## Verification

```cisco
show etherchannel summary
show interfaces trunk
show spanning-tree
```

A healthy Layer 2 EtherChannel should show the Port-Channel as operational.

Example expected status:

```text
Po1(SU)
```

Where:

- `S` = Layer 2 EtherChannel
- `U` = in use / operational

## Troubleshooting scenario

An initial EtherChannel fault was investigated where one side's member configuration prevented the bundle from forming correctly.

The investigation used:

```cisco
show etherchannel summary
```

The member interfaces and channel configuration were compared and corrected.

## Redundancy testing

A physical member link was taken out of service to verify that the logical EtherChannel retained connectivity through the remaining member.

The purpose was to validate the design rather than simply confirm that the configuration existed.

## STP interaction

The bundled Port-Channel is treated as a logical Layer 2 connection by STP rather than presenting each physical member as an independent path.

## Skills demonstrated

- EtherChannel
- LACP
- Link redundancy
- 802.1Q trunking
- STP/EtherChannel interaction
- Failure testing
- Cisco IOS verification
- Structured troubleshooting
