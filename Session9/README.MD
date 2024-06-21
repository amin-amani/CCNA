# Switch configurations

<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/Session9/vlan-routing.PNG" alt="CCNA ||" width="200"/></a>

## VLAN

## vtp

```
interface range fastEthernet 0/1-20
```

```
show process
```

```
interface FastEthernet0/0.1
encapsulation dot1Q 1 native
ip address 192.168.10.1 255.255.255.0

interface FastEthernet0/0.2
encapsulation dot1Q 2
ip address 192.168.20.1 255.255.255.0
```
