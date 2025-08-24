<p align=center>
 <ins>Overview of Concepts</ins>
</p>

Static IPv4 Addressing  
 * manual addressing as opposed to dynamic/automatic addressing
 * used in smaller networks in lieu of configuring a DHCP server
 * dedicated devices such as servers, printers, and router interfaces are usually statically-addressed

Subnetting
 * divides larger networks into smaller networks, subnetworks, subnets
 * subnets have their own broadcast domain, broadcast packets are not routed outside of the subnet
 * subnet masks identify the network to which a device belongs, e.g., a subnet mask of 255.255.255.0 identifies a network capable of hosting up to 254 devices (the first address is the network address and the last address is the broadcast address)
 * network bits are borrowed from host bits to create subnets, e.g., a 24-bit network address will have to borrow 1 host bit to create two subnets

<p align=center>
 <img src="https://github.com/Fehral/networkprojectv1/blob/main/subnetting.png?raw=true">
</p>

<p align=center>
 <ins>Static IPv4 Addressing and Subnetting Topology</ins>
</p>

<p align=center>
 <img src="https://github.com/Fehral/networkprojectv1/blob/main/networkprojectv1topology.png?raw=true"></img>
</p>

R1 Configuration
```
Router>en
Router#conf t
Router(config)#int g0/0
Router(config-if)#no shutdown
Router(config-if)#ip address 192.168.1.1 255.255.255.128
Router(config-if)#int g0/1
Router(config-if)#no shutdown
Router(config-if)#ip address 192.168.1.129 255.255.255.128
Router(config-if)#end
Router#copy run start
Destination filename [startup-config]? [Enter]
Building configuration...
[OK]
```

