# Introduction of Classful IP Addressing

An IP address is an address that has information about how to reach a specific host, especially outside the LAN. 

An IP address is a 32-bit unique address having an address space of 232.

Classful IP addressing is a way of organizing and managing IP addresses, which are used to identify devices on a network. Think of IP addresses like street addresses for houses; each device on a network needs its unique address to communicate with other devices. In this article, we are going to discuss Classful IP addresses, and their types in detail.

## What is an IPV4 Address?
An IPv4 address is a unique number assigned to every device that connects to the internet or a computer network. It’s like a home address for your computer, smartphone, or any other device, allowing it to communicate with other devices.

Format: An IPv4 address is written as four numbers separated by periods, like this: 192.168.1.1. Each number can range from 0 to 255.
The IPv4 address is divided into two parts: Network ID and Host ID.
Purpose: The main purpose of an IPv4 address is to identify devices on a network and ensure that data sent from one device reaches the correct destination.
Example: When you type a website address into your browser, your device uses the IPv4 address to find and connect to the server where the website is hosted.
Host ID
Think of an IPv4 address as a phone number for your device. Just as you dial a specific number to reach a particular person, devices use IPv4 addresses to connect and share information.

There are two notations in which the IP address is written, dotted decimal and hexadecimal notation.

Dotted Decimal Notation
Some points to be noted about dotted decimal notation: 

The value of any segment (byte) is between 0 and 255 (both included).
No zeroes are preceding the value in any segment (054 is wrong, 54 is correct).
Dotted Decimal Notation
Dotted Decimal Notation

Hexadecimal Notation
 


Need For Classful Addressing
Initially in 1980’s IP address was divided into two fixed part i.e., NID(Network ID) = 8bit, and HID(Host ID) = 24bit. So there are 28 that is 256 total network are created and 224 that is 16M Host per network.

There are one 256 Networks and even a small organization must buy 16M computer(Host) to purchase one network. That’s why we need classfull addressing.

Classful Addressing
The 32-bit IP address is divided into five sub-classes. These are given below:

Class A
Class B
Class C
Class D
Class E
Each of these classes has a valid range of IP addresses. Classes D and E are reserved for multicast and experimental purposes respectively. The order of bits in the first octet determines the classes of the IP address. 

The class of IP address is used to determine the bits used for network ID and host ID and the number of total networks and hosts possible in that particular class. Each ISP or network administrator assigns an IP address to each device that is connected to its network. 

Classful Addressing 
Classful Addressing 

Note: 

IP addresses are globally managed by Internet Assigned Numbers Authority(IANA) and Regional Internet Registries(RIR).
While finding the total number of host IP addresses, 2 IP addresses are not counted and are therefore, decreased from the total count because the first IP address of any network is the network number and whereas the last IP address is reserved for broadcast IP.
Occupation of The Address Space In The Classful Addressing
Occupation of The Address Space In Classful Addressing

Class A
IP addresses belonging to class A are assigned to the networks that contain a large number of hosts. 

The network ID is 8 bits long.
The host ID is 24 bits long.
The higher-order bit of the first octet in class A is always set to 0. The remaining 7 bits in the first octet are used to determine network ID. The 24 bits of host ID are used to determine the host in any network. The default subnet mask for Class A is 255.x.x.x. Therefore, class A has a total of:

2^24 – 2 = 16,777,214 host ID
IP addresses belonging to class A ranges from 0.0.0.0 – 127.255.255.255. 

Class A
Class A

Class B
IP address belonging to class B is assigned to networks that range from medium-sized to large-sized networks. 

The network ID is 14 bits long.
The host ID is 16 bits long.
The higher-order bits of the first octet of IP addresses of class B are always set to 10. The remaining 14 bits are used to determine the network ID. The 16 bits of host ID are used to determine the host in any network. The default subnet mask for class B is 255.255.x.x. Class B has a total of: 

2^14 = 16384 network address
2^16 – 2 = 65534 host address
IP addresses belonging to class B ranges from 128.0.0.0 – 191.255.255.255.
 

Class B
Class B

Class C
IP addresses belonging to class C are assigned to small-sized networks.

The network ID is 24 bits long.
The host ID is 8 bits long.
The higher-order bits of the first octet of IP addresses of class C is always set to 110. The remaining 21 bits are used to determine the network ID. The 8 bits of host ID are used to determine the host in any network. The default subnet mask for class C is 255.255.255.x. Class C has a total of:

2^21 = 2097152 network address
2^8 – 2 = 254 host address
IP addresses belonging to class C range from 192.0.0.0 – 223.255.255.255.

Class C
Class C

Class D
IP address belonging to class D is reserved for multi-casting. The higher-order bits of the first octet of IP addresses belonging to class D is always set to 1110. The remaining bits are for the address that interested hosts recognize.

Class D does not possess any subnet mask. IP addresses belonging to class D range from 224.0.0.0 – 239.255.255.255.

Class D
Class D

Class E
IP addresses belonging to class E are reserved for experimental and research purposes. IP addresses of class E range from 240.0.0.0 – 255.255.255.255. This class doesn’t have any subnet mask. The higher-order bits of the first octet of class E are always set to 1111.

Class E
Class E

Range of Special IP Addresses
169.254.0.0 – 169.254.0.16 : Link-local addresses
127.0.0.0 – 127.255.255.255 : Loop-back addresses
0.0.0.0 – 0.0.0.8: used to communicate within the current network.
Rules for Assigning Host ID
Host IDs are used to identify a host within a network. The host ID is assigned based on the following rules:

Within any network, the host ID must be unique to that network.
A host ID in which all bits are set to 0 cannot be assigned because this host ID is used to represent the network ID of the IP address.
Host ID in which all bits are set to 1 cannot be assigned because this host ID is reserved as a broadcast address to send packets to all the hosts present on that particular network.
Rules for Assigning Network ID
Hosts that are located on the same physical network are identified by the network ID, as all host on the same physical network is assigned the same network ID. The network ID is assigned based on the following rules:

The network ID cannot start with 127 because 127 belongs to the class A address and is reserved for internal loopback functions.
All bits of network ID set to 1 are reserved for use as an IP broadcast address and therefore, cannot be used.
All bits of network ID set to 0 are used to denote a specific host on the local network and are not routed and therefore, aren’t used.
