# Password Recovery 

## Set Password to Router

Enable secret [password]:

```
enable secret 123
```
## Password Recovery Steps for Router

1. During boot, press CTRL+PAUSE and go to bootloader shell.
2. Set register to 2142:
   
```
>confreg 2142
```
3. Reset:
```
>reset
```  
4. Copy startup config to running config:
```
#copy startup_config running_config
```
5. Remove password or set new one:
```
no secret
enable secret 0000
``` 
6. Config reg to 2102:
```
#config-register 2102
```
<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/200-301-Tra2210_9/3layer.PNG" alt="CCNA ||" width="500"/></a>

## Port Types

**Trunk:** Path to transfer all VLAN traffic.

**Access:** Specific VLAN traffic will pass.

**Dynamic:** Becomes the same as the connected port mode; if it is trunk, it becomes trunk; if it is access, it becomes access. It is not recommended to leave ports Dynamic.


```
interface range fastEthernet 0/1-20
switch port mode trunk
switch port mode access
switch port access vlan 2
``` 

## VLAN Types

**Local:** Exists only on one switch.

**End to End:** Exists on multiple switches and is connected using trunk ports.

<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/200-301-Tra2210_9/vlantypes.PNG" alt="CCNA ||" width="500"/></a>

## We Have Two Trunk Types

**Single Tag (802.1q):** Is better than double tag.

**Double Tag:**


**Native VLAN:** Packets without VLAN tags transfer via native VLAN. We put the biggest network into native VLAN to reduce traffic because it doesn't need 1q tag.

If we don't have a managed switch, we shouldn't change the native VLAN.

<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/200-301-Tra2210_9/ex1-scenario.PNG" alt="CCNA ||" width="500"/></a>

## Check VLAN and its Interfaces

```
show vlan brief
```

* If we can't see some ports in the show vlan brief report, it means they are trunk or their VLAN is cleared.

## Check Trunk Ports


```
show int trunk 
```

## Erase Configs and VLANs

VLANs are not saved in startup_config; they are in vlan.dat in flash. Check flash using the command below:

```
show flash:
```

```
erase startup_config
```
## To Delete VLAN File
```
delete flash:
 delete filename []? vlan.dat
```

## Idle Utility Should Be Between 4%-5%

```
show process
```

## VLAN Routing 

### 2 Port

Useless, takes 2 ports from the router.

<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/200-301-Tra2210_9/vlan%20routing1.PNG" alt="CCNA ||" width="500"/></a>

### Sub Interface 

<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/200-301-Tra2210_9/vlan%20routing-subint.PNG" alt="CCNA ||" width="500"/></a>

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

## VTP

Creates and shares VLANs over connected switches. It just creates VLAN; you should assign VLAN to each interface.

### Server Mode

```
vtp domain hsh.com
vtp password 123
vtp mode server
```

### Client Mode

```
vtp domain hsh.com
vtp password 123
vtp mode server
```

### Transparent Mode

Just passes settings to other switches and doesn't create VTP server VLANs itself.

2:07:00
