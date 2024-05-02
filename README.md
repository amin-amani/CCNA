# CCNA
CCNA Training Course


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
