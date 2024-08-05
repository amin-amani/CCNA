# what is lan?
devices work under one broadcast domain

## vlan types:
* local
* end to end

## vlan routing scenario

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
