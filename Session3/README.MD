
<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/Session3/routings.PNG" alt="CCNA ||" width="500"/></a>

now EIGRP is open standard

Administrtive Distance:

specify routing protocol priority



lower is more important


converge time :

open standard:?

router eigrp <as number>

<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/Session3/eigrp-protocols.PNG" alt="CCNA ||" width="500"/></a>

Autonomous Systems:

protocols where works under one administration
majmoee ei asz protocol HA ke taht ye administration kar mikone

inside each AS we use IGP(interior gateway protocols) protocols and between each AS we use EGP(exterior gateway protocols)

https://iana.org is responsible to distribute AS numbers

ex:

```
rouer eigrp 100
network 192.168.1.10 0.0.0.255

```
announce network 

network 192.168.1.10 wildcard
