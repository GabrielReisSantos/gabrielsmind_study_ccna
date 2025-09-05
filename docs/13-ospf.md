# 13 — OSPF
```text
router ospf 1
 network 192.168.10.0 0.0.0.255 area 0
int gi0/1
 ip ospf cost 1562
 ip ospf hello-interval 10
 ip ospf dead-interval 40
show ip ospf neighbor
```
