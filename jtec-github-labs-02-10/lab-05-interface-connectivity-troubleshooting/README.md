# Lab 05 — Interface & Connectivity Troubleshooting

## Objective

Develop a structured Layer 1 and interface troubleshooting process by investigating deliberately introduced faults.

## Faults investigated

The lab included:

- Speed mismatch
- Duplex mismatch
- Administratively shut interface
- Incorrect cable/interface connection

## Troubleshooting process

Start with the interface state:

```cisco
show ip interface brief
```

Use the quick status view:

```cisco
show interfaces status
```

Then inspect detailed interface information:

```cisco
show interfaces
```

## Example investigation

If an interface reports:

```text
down/down
```

investigate Layer 1 first:

1. Check the cable.
2. Check the connected interface.
3. Check whether the interface is shut down.
4. Check speed/duplex.
5. Check interface errors.

For an administratively disabled interface:

```cisco
interface GigabitEthernet0/1
 no shutdown
```

## Result

The lab was completed successfully and demonstrated a structured approach to interface and cabling faults.

## Additional concept

Single-mode fibre (SMF) is suited to longer-distance links, while multimode fibre (MMF) is generally used for shorter-distance applications.

## Skills demonstrated

- Layer 1 troubleshooting
- Interface state analysis
- Speed/duplex checking
- Cabling fault isolation
- Cisco IOS verification
