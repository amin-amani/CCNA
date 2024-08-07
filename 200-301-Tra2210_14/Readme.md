# DHCP SNOOPING

createting facke dhcp server to apply fake settings in clients computers.

dhcp starvation: send ip reauest with fake generated mac and fill dhcp server ip list 

### enable dhcp snooping generally and for vlan 1. set f0/10 as trusted port

```
ip dhcp snooping
ip dhcp snooping vlan 1
int f0/10
ip dhcp snooping trust
ip dhcp limi rate 5 //prevent starvation attack
```

# routing protocols:

<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/200-301-Tra2210_14/ospfvsEIGRP.PNG" alt="CCNA ||" width="700"/></a>

### IGB(Interior Gateway Protocol)

* Distance Vector: RIP

* Link state: OSPF

* Advanced Distance Vector: EIGRP - RIP v2

### EGP(Exerior Gateway Protocol)

* EGP

* BGP


1:14:0
