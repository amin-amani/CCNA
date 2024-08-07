# RIP protocol

<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/200-301-Tra2210_01/rip-properties.PNG" alt="CCNA ||" width="700"/></a>

open standard

max hop count 15

class-full

converge time slow

redistributable: means it can translate from one protocol to another and vice versa

## versions:

1.V1: broadcast  255.255.255.0

2.V2: multicast classful 255.0.0.9

3.NG:

change version example:

```
router rip
version 2
```
## Enable RIP in router
```
router rip
```
## announce networks

```
network 192.168.1.1
network 192.168.2.2
```
## Debug protocol

```
debug ip rip
no debug ip rip
undebug all
```
## RIP timers 

timer basic update invalid hold flash
```
timer basic 35 193 200 210
no timer basic
```

## see protocol on router

show ip protocol

