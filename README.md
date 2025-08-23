<p align=center>
 <ins>Static IPv4 Addressing and Subnetting Topology</ins>
</p>

<p align=center>
 <img src="https://github.com/Fehral/networkprojectv1/blob/main/networkprojectv1_topology.png?raw=true"></img>
</p>

<p align=center>
 <ins>Overview of Concepts</ins>
</p>

Subnetting
 * divides larger networks into smaller networks, subnetworks, subnets
 * subnets have their own broadcast domain, broadcast packets are not routed outside of the subnet
 * network bits are borrowed from host bits to create subnets, i.e., a 24-bit network address will have to borrow 1 host bit to create two subnets

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
Router(config-if)#exit
Router(config)#exit
Router#copy run start
```

