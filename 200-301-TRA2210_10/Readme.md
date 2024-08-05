# what is lan?
devices work under one broadcast domain

## vlan types:
* local
* end to end

## vlan routing scenario

<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/200-301-TRA2210_10/vlan-routing-mls1.PNG" alt="CCNA ||" width="500"/></a>

* crete 2 vlan interface in  switch 1

* assign ip  to each interface vlan

```
configure terminal
interface vlan 1
ip address 192.168.1.254 255.255.255.0
no shutdown

interface vlan 1
ip address 192.168.2.254 255.255.255.0
no shutdown
ex
write
```
* crete 2 vlan interface in  switch 1

* assign ip  to each interface vlan

```
configure terminal
interface vlan 1
ip address 192.168.1.253 255.255.255.0
no shutdown
configure terminal
interface vlan 2
ip address 192.168.2.253 255.255.255.0
no shutdown
```

* crete trunk port in switch port 24
```
en
configure terminal
int f0/24
switch trunk encapsulation dot1q
switchport mode trunk
ex
```
* creta 2 vlan interface in MLS
```
vlan 2
ex
interface vlan 1
ip address 192.168.1.1 255.255.255.0
no shutdown
interface vlan 2
ip address 192.168.2.1 255.255.255.0
no shutdown
```
* issue ip route command
```
ip routing
ex
```
## vlan routing scenario

<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/200-301-TRA2210_10/scenario-test2.PNG" alt="CCNA ||" width="700"/></a>

1:56






