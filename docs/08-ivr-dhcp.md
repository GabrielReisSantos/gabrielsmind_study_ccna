# 08 — Inter-VLAN (ROAS) + DHCP
```text
int gi0/0.10
 encapsulation dot1q 10
 ip address 10.0.10.1 255.255.255.0
!
ip dhcp excluded-address 10.0.10.1 10.0.10.20
ip dhcp pool VLAN-10
 network 10.0.10.0 255.255.255.0
 default-router 10.0.10.1
 dns-server 10.0.10.2
show ip dhcp binding
```
