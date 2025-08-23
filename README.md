<p align=center>
 Static IPv4 Addressing and Subnetting Topology
</p>

<p align=center>
 <img src="https://github.com/Fehral/networkprojectv1/blob/main/networkprojectv1_topology.png?raw=true"></img>
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
Router(config-if)#exit
Router(config)#exit
Router#copy run start
```

