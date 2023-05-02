<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create Azure Virtual Machines with Windows 10 and Ubuntu.
- Remote into the Windows Virtual Machines and install Wireshark. 
- Use Wireshark to observe ICMP, SSH, DHCP, DNS, and RDP traffic between the two virtual machines.

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/aYGXwVM.png"/>
</p>
<p>
First, we created two Azure Virtual Machines, one with Windows 10 and the other with Ubuntu. The image above shows the topology of this virtual network: both virtual machines along with their virtual network interfaces, virtual network seurity groups, and IP addresses.
</p>
<br />

<p>
<img src="https://i.imgur.com/OVrSGf7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Second, we logged in remotely to the Windows virtual machine using its IP address. This was done through Microsoft Remote Desktop on Mac OS. Once logged in, we installed Wireshark to be able to examine network traffic between the two virtual machines.
</p>
<br />

<p>
<img src="https://i.imgur.com/mmWar8f.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/OIGiIP5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lastly, along with Wireshark we used the command-line interface on the Windows virtual machine to observe the network traffic. Using the Ubuntu virtual machine's private IP address, we used the ping command to observe ICMP traffic, the ipconfig command to observe DHCP traffic, the nslookup command to observe DNS traffic. We also observed SSH traffic by connecting to the Ubuntu virtual machine for a terminal session.
</p>
<br />
