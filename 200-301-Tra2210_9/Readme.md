## set password to router

enable secret [password]
```
enable secret 123
```
## passsword recovery step router

1. during boot press CTRL+PAUSE and go to bootloader shell
2. set register to 2142
```
>confreg 2142
```
3. reset
```
>reset
```  
4. copy startup config to running config
```
#copy startup_config running_config
```
5. remove password or set new one
```
no secret
enable secret 0000
``` 
6. config reg to 2102
```
#config-register 2102
```
<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/200-301-Tra2210_9/3layer.PNG" alt="CCNA ||" width="500"/></a>
## port types

Trunk: path to trnasfer all vlan traffic

Access: spefific vlan trafic will pass

Dynamic: become same as connected port mod if it is trunk become trunk if it is access become acces.it is not recomanded to leave ports Dynamic

```
interface f0/0
switch port mode trunk
switch port mode access
switch port access vlan 2
``` 

## vlan types:

local: meanse exist only on one switch

end to end: meanse exist on multiple switchs and connected using trunk port

<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/200-301-Tra2210_9/vlantypes.PNG" alt="CCNA ||" width="500"/></a>

## we have two truk types:

single tag(802.1q): is beter than double tag.

double tag:


Native vlan: packets without vlan tags transfer via native vlan. we put bigest network into native vlan to reduce traffic because it doenst need 1q tag

if we dont have mange switch we sholdnt change native vlan


<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/200-301-Tra2210_9/ex1-scenario.PNG" alt="CCNA ||" width="500"/></a>

## check vlan and it's interfaces

```
show vlan brief
```

* if we can't see some ports in show vlan brief report it means it they are trunk or their vlan cleared 

## check trunk ports: 

```
show int trunk 
```

## erase configs and vlans

vlans are no saved in  startup_config they are in vlan.dat in flash. chcke flash using below command:

```
show flash:
```

```
erase startup_config
```
## To delete vlan file:
```
delete flash:
 delete filename []? vlan.dat
```

## Idle utility should between  4%-5%

```
show process
```
## vlan routing 

## 2 port

<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/200-301-Tra2210_9/vlan%20routing1.PNG" alt="CCNA ||" width="500"/></a>

### sub interface 

<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/200-301-Tra2210_9/vlantypes.PNG" alt="CCNA ||" width="500"/></a>

```
interface f0/0
no shutdown
int f0/0.1
encapsulation dot1Q 1 //vlan1
ip address 192.168.10.1
no shutdown
ex

int f0/0.2
encapsulation dot1Q 2 //vlan2
ip address 192.168.20.1
no shutdown
ex

```
  
2:07:00
