# 15 — ACL
```text
access-list 1 permit host 192.168.146.10
access-list 1 deny 11.0.0.0 0.0.0.255
int fa0/0
 ip access-group 1 in
!
ip access-list extended WEB-ONLY
 permit tcp any host 192.168.0.1 eq 80
 deny ip any any log
int fa0/0
 ip access-group WEB-ONLY in
```
