# Lab 06 — VLAN Configuration

## Objective

Create and assign VLANs to access ports to provide logical network segmentation.

## VLANs

```text
10  MANAGEMENT
20  USERS
30  SALES
40  FINANCE
50  SERVERS
60  VOICE
70  GUEST
80  NET-MGMT
99  NATIVE
```

## Access-port configuration

Example:

```cisco
interface GigabitEthernet0/10
 switchport mode access
 switchport access vlan 30
```

The exact interface should match the endpoint being connected.

## Verification

```cisco
show vlan brief
show interfaces GigabitEthernet0/10 switchport
```

## Troubleshooting scenario

Deliberate VLAN assignment faults included endpoints being placed into the wrong VLAN, such as:

- Sales endpoint in the wrong VLAN
- User endpoint in the wrong VLAN
- Finance endpoint in the wrong VLAN

The troubleshooting process was to compare the endpoint requirement against:

```cisco
show vlan brief
```

and:

```cisco
show interfaces <port> switchport
```

## Design note

Uplink/trunk configuration was deliberately deferred to Lab 07 so that VLAN creation and access-port assignment could be verified independently.

## Skills demonstrated

- VLAN creation
- VLAN naming
- Access-port configuration
- VLAN troubleshooting
- Layer 2 segmentation
