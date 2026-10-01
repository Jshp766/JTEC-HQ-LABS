# Lab 04 — Cisco IOS Security & SSH

## Objective

Secure Cisco network devices and replace insecure remote management methods with SSH.

## Security configuration

The lab covered:

- Hostnames
- Local privilege-15 administrator
- Enable secret
- Login banner
- Console authentication
- VTY local authentication
- Five-minute EXEC timeout
- RSA key generation
- SSH version 2
- SSH-only VTY access
- Saving the configuration

## Core configuration

```cisco
hostname JTEC-DEVICE

enable secret <REDACTED>

username admin privilege 15 secret <REDACTED>

ip domain-name jtec.local

crypto key generate rsa

ip ssh version 2

line console 0
 login local
 exec-timeout 5 0

line vty 0 4
 login local
 transport input ssh
 exec-timeout 5 0
```

> Passwords/secrets are deliberately not stored in this repository.

## Verification

```cisco
show running-config
show ip ssh
show users
```

Test SSH only after the management VLAN and IP connectivity are operational.

## Skills demonstrated

- Cisco IOS hardening
- Local authentication
- SSH
- RSA keys
- VTY configuration
- Secure remote management
- Configuration persistence
