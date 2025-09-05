# 17 — HSRP
```text
int gi0/1
 standby 10 ip 172.167.10.10
 standby 10 priority 120
 standby preempt
 standby 10 timers 5 15
show standby
```
