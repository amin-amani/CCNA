
<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/Session3/routings.PNG" alt="CCNA ||" width="500"/></a>

eigrp route priority = sum delay + bandwidth

Check buttle neck on the packet way

now EIGRP is open-standard



Administrtive Distance:

specify routing protocol priority



lower is more important


converge time :

open standard:?

router eigrp <as number>

<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/Session3/eigrp-protocols.PNG" alt="CCNA ||" width="500"/></a>

Autonomous Systems:

protocols where works under one administration

inside each AS we use IGP(interior gateway protocols) protocols and between each AS we use EGP(exterior gateway protocols)

https://iana.org is responsible to distribute AS numbers

wild card: A wildcard mask is a 32-bit binary number that is mainly used to indicate which bits of an IP address must match and which bits do not matter

subnet mask:  255.255.255.128 -> wild card: 0.0.0.127 -> wildcard = 255.255.255.255 - sub.sub.sub.sub 

rouer eigrp [AS number]

network [ip] [wildcard]

if the network is class-full don't need to write wildcards


ex:

```
rouer eigrp 100
network 192.168.1.10 0.0.0.255

```
announce network 

network 192.168.1.10 wildcard


```
eigrp neighbors

show ip protocols

```
<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/Session3/eigrp%20metric.PNG" alt="CCNA ||" width="500"/></a>
