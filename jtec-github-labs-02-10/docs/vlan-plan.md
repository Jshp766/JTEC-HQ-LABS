# JTEC VLAN Plan

| VLAN | Name | Function |
|---:|---|---|
| 10 | MANAGEMENT | Device/user management |
| 20 | USERS | General user endpoints |
| 30 | SALES | Sales endpoints |
| 40 | FINANCE | Finance endpoints |
| 50 | SERVERS | Server network |
| 60 | VOICE | Voice network |
| 70 | GUEST | Guest network |
| 80 | NET-MGMT | Network management |
| 99 | NATIVE | Native/infrastructure VLAN |

Standard trunk allowed list:

```text
10,20,30,40,50,60,70,80,99
```

Standard native VLAN:

```text
99
```
