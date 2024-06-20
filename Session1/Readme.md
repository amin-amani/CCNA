# Static Routing

<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/Session1/1.png" alt="CCNA ||" width="600"/></a>


## Route types:

1. Host route

2. Network route

3. Default rout


if you received a packet with destination ip with  netmask send it to the next hope

```
ip route 192.168.16.0 255.255.240.0 172.16.42.2
```
```
r0#configure terminal 
Enter configuration commands, one per line.  End with CNTL/Z.
r0(config)#interface fastEthernet 0/0
r0(config-if)#ip address 192.168.1.1 255.255.255.0
r0(config-if)#no shutdown 
r0(config-if)#ex
r0(config)#interface fastEthernet 0/1
r0(config-if)#ip address 192.168.20.1 255.255.240.0
r0(config-if)#no shutdown 
```


```
show ip interface brief 
Interface              IP-Address      OK? Method Status                Protocol 
FastEthernet0/0        192.168.1.1     YES manual up                    up 
FastEthernet0/1        192.168.20.1    YES manual up                    up 
Vlan1                  unassigned      YES unset  administratively down down
```
## WIC interfaces
```
clock rate 64000
```



## Set administrative distance for static route

Administrative distance is the first criterion that a router uses to determine which routing protocol to use if two protocols provide route information for the same destination
```
ip route 192.168.16.0 255.255.240.0 172.16.42.2 1
```


