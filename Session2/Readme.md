# RIP protocol

## versions:

1.V1: broadcast  255.255.255.0

2.V2: multicast classful 255.0.0.9

3.NG:

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
