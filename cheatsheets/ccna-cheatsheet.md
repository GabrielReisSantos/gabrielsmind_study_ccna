# CCNA Cheatsheet (Gabrielsmind)

**Bootstrap**
enable ; conf t ; hostname R1 ; service password-encryption ; enable secret <pw> ; username admin secret <pw> ; line vty 0 15 ; login local ; transport input ssh ; ip domain-name lab.local ; crypto key generate rsa ; ip ssh version 2 ; copy run start

**VLAN/Trunk/SVI**
vlan 10 ; name IT ; int fa0/1 ; switchport mode access ; switchport access vlan 10 ; int gi0/1 ; switchport trunk encapsulation dot1q ; switchport mode trunk ; int vlan 10 ; ip address 192.168.10.1 255.255.255.0 ; no sh

**Routing**
ip route 0.0.0.0 0.0.0.0 10.10.10.1 ; router ospf 1 ; network 192.168.10.0 0.0.0.255 area 0 ; router eigrp 100 ; network 10.10.40.0 0.0.0.255 ; no auto-summary ; router rip ; version 2 ; network 192.168.10.0 ; no auto-summary

**ACL/NAT/HSRP**
ip access-list extended WEB-ONLY ; permit tcp any host 192.168.0.1 eq 80 ; deny ip any any log ; ip nat inside source static 10.0.0.10 100.1.1.1 ; int gi0/1 ; standby 10 ip 172.167.10.10 ; standby preempt
