# 03 — SSH
```text
hostname SW-1
ip domain-name cisco.local
username admin secret <pw>
crypto key generate rsa
ip ssh version 2
line vty 0 15
 login local
 transport input ssh
```
