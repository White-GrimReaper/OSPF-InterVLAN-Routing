<h1>OSPF InterVLAN Routing</h1>
<h2>Objective</h2>
To configure and implement Open Shortest Path First (OSPF) dynamic routing between three Layer 3 switches to enable communication between multiple VLANs and subnets. This project focuses on creating VLANs, assigning IP addresses to switched virtual interfaces (SVIs), enabling IP routing, configuring OSPF to advertise connected networks, and establishing OSPF neighbor adjacencies. The goal is to achieve seamless inter-VLAN connectivity, dynamic route exchange, efficient network traffic forwarding, and reliable end-to-end communication while verifying routing tables and troubleshooting connectivity issues.
<h2>Program</h2>

<p align="center">
<img src="https://i.imgur.com/9oTBlAV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
In this project, we want to configure OSPF on three Layer 3 Switches and VLANs consecutively added per switch and to start off simply is to first configure the switches one at a time with the respective number of VLANs and OSPF.
<p align="center">
<img src="https://i.imgur.com/5cxx9My.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p align="center">
<img src="https://i.imgur.com/4ocahuD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p align="center">
<img src="https://i.imgur.com/WOxwO2S.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p align="center">
<img src="https://i.imgur.com/qwzw756.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
On the first Layer 3 switch, because we’ll be routing through Layer 3, we must enable IP routing. Configure the interfaces that are connected to the end hosts as access ports for VLAN traffic and because we are also using VLANs for network communication, we configure them as interfaces and as a default gateway for the end hosts respectively on their assigned subnet. On the end hosts, we must also configure their IP address, subnet mask, and default gateway in their respective subnet. On the following Layer 3 switches, must also do the same configuration respectively.
<p align="center">
<img src="https://i.imgur.com/8RWSH73.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p align="center">
<img src="https://i.imgur.com/5RVafgK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p align="center">
<img src="https://i.imgur.com/ybAVvw0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p align="center">
<img src="https://i.imgur.com/jea4gIj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p align="center">
<img src="https://i.imgur.com/qTeUDkO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Now moving on from configuring VLANs, we must configure OSPF on all Layer 3 Switches for dynamic routing and configuration.
<p align="center">
<img src="https://i.imgur.com/LJGdWji.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p align="center">
<img src="https://i.imgur.com/rptT49h.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p align="center">
<img src="https://i.imgur.com/fpjqybO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p align="center">
<img src="https://i.imgur.com/mWk23mb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p align="center">
<img src="https://i.imgur.com/2aNmpKm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p align="center">
<img src="https://i.imgur.com/oyIlV3A.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
For a simple OSPF configuration, we can configure the area using 0 as the backbone, the network address and wildcard mask of the VLAN subnets and area number that we configured to be included and Router ID individually, and for the interfaces of the switches connected to one another, we disable the switchport to allow Layer 3 routing and configure its IP address in its own respective subnet and include it in the OSPF configuration for traffic to pass in between dynamically.
