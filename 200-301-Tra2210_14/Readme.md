# DHCP SNOOPING

createting facke dhcp server to apply fake settings in clients computers.

dhcp starvation: send ip reauest with fake generated mac and fill dhcp server ip list 

### enable dhcp snooping generally and for vlan 1. set f0/10 as trusted port

```
ip dhcp snooping
ip dhcp snooping vlan 1
int f0/10
ip dhcp snooping trust
```
