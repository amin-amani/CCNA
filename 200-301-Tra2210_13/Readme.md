# FHRP(First Hup Redundant Protocol):

* HSRP(hot standby) cisco
* VRRP (virtual ) open standard
* GLBP (Gateway load balance protocol)

 ## FHRP first scenario

<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/200-301-Tra2210_13/fhrp-scenario1.PNG" alt="CCNA ||" width="700"/></a>

## issue this command under specific interfaces

* in route 1
```
int f0/0
standby 1 ip 192.168.10.3
standby 1 priority 100
standby 1 preempt
standby 1 track f0/1 //track interface connected to intrnet. interface down causes decrease from priority
```
* on route 2
```
int f0/0
standby 1 ip 192.168.10.3
standby 1 priority 105
standby 1 preempt
```
### when both priorities are same firs connected router used as gate way to internet

see standby status:

```
show standby brief
```

