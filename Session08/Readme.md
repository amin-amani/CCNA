### NAT


int f0/0
ip nat inside
int f0/1
ip nat outside

access-list 1 permit 192.168.1.0 0.0.0.255
ip nat inside source int f0/1


ip nat pool mypool  192.118.116.2 192.118.116.5 netmask 255.255.255.0 
ip nat inside source pool mypool overload 



debug ip icmp
debug ip nat
