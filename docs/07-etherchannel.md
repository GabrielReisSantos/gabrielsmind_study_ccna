# 07 — EtherChannel
```text
int po10
 switchport mode trunk
!
int range fa0/1-4
 switchport mode trunk
 channel-group 10 mode active
 channel-protocol lacp
show etherchannel summary
```
