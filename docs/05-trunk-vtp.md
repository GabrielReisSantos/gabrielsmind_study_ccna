# 05 — Trunk & VTP
```text
int gi0/1
 switchport trunk encapsulation dot1q
 switchport mode trunk
 switchport nonegotiate
 switchport trunk native vlan 99
 switchport trunk allowed vlan 10,20,99
show interface trunk
!
vtp domain LAB
vtp version 3
vtp mode server
show vtp status
```
