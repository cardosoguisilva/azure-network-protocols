<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

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

- Create Resources
- Observe Traffic Between the Two VMs

<h2>Actions and Observations</h2>

1 Creating VMs
- In Azure, create a Windows 10 and a Linux Ubuntu Server in the same resource group respectively.

![image](https://github.com/cardosoguisilva/azure-network-protocols/assets/157248613/149c0a2f-d7b2-4c9b-891f-5df14ed0385d)

- Make Ubuntu's VM is in the same Vnet and Subnet.

![image](https://github.com/cardosoguisilva/azure-network-protocols/assets/157248613/a3df6377-409b-4233-bfd2-f60fef43e989)



-
