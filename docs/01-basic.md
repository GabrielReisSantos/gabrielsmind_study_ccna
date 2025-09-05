# 01 — Basic
```text
enable
conf t
hostname R1
service password-encryption
enable secret <pw>
username admin secret <pw>
line console 0
 login
 password <pw>
line vty 0 15
 login local
 transport input ssh
ip domain-name lab.local
crypto key generate rsa
ip ssh version 2
banner motd ^ Authorized access only ^
copy run start
```
