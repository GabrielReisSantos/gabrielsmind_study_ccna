# 16 — NAT
```text
! Static
ip nat inside source static 10.0.0.10 100.1.1.1
int fa0/1 ; ip nat inside
int fa0/2 ; ip nat outside

! Dynamic (Pool)
access-list 1 permit 10.0.0.0 0.0.0.255
ip nat pool STUDY 5.5.5.1 5.5.5.11 netmask 255.255.255.0
ip nat inside source list 1 pool STUDY

! PAT (Overload)
access-list 1 permit 192.168.0.0 0.255.255.255
ip nat pool STUDY 20.20.20.2 20.20.20.2 netmask 255.255.255.252
ip nat inside source list 1 pool STUDY overload
```
