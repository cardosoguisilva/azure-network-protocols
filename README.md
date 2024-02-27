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
- Install Programs
- Observe Traffic Between the Two VMs

<h2>Actions and Observations</h2>

1 Creating VMs
- In Azure, create a Windows 10 and a Linux Ubuntu Server in the same resource group respectively.

![image](https://github.com/cardosoguisilva/azure-network-protocols/assets/157248613/149c0a2f-d7b2-4c9b-891f-5df14ed0385d)

- Make sure Ubuntu's VM is in the same Vnet and Subnet.

![image](https://github.com/cardosoguisilva/azure-network-protocols/assets/157248613/a3df6377-409b-4233-bfd2-f60fef43e989)

2 Install Programs
- Open VM1-Windows10 and install Wireshark.
- Go to https://www.wireshark.org/download.html and select Windows x64 Installer. Install everything by default.

![image](https://github.com/cardosoguisilva/azure-network-protocols/assets/157248613/e69aa49a-08ad-438f-9f5c-55c030d298a7)

3 Observe Traffic Between the Two VMs
- Start Wireshark and choose Ethernet connection, this will show the live traffic in the VM.

![image](https://github.com/cardosoguisilva/azure-network-protocols/assets/157248613/716350cc-ed32-440b-8b56-13fc0b9373b2)

- ICMP Traffic
- - Set the filter on wireshark for ICMP go to PowerShell and ping VM2 private IP Address.

![image](https://github.com/cardosoguisilva/azure-network-protocols/assets/157248613/acfca517-0d07-4188-9a03-43f27a2bbf60)

  - - Changing the Firewall to block ICMP traffic.
    - On Azure go to VM2's Network Security Group (NSG) and add an Inbound Rule to DENY ICMP Traffic.
      
![image](https://github.com/cardosoguisilva/azure-network-protocols/assets/157248613/857d4347-b07d-4da0-91b8-d6b829f4f23b)
   
  - - Now when trying to ping VM2 the request will timeout.
    
![image](https://github.com/cardosoguisilva/azure-network-protocols/assets/157248613/fbeaff72-5011-42fc-a117-5d4b185b6ae1)
  
- SSH Traffic
- - Set SSH filter on wireshark and use PowerShell to "SSH into" VM2 using its private address.
  - Use this command on PowerShell "ssh [username of your vm2]@[private address of VM2]". Type your password. NOTE: Password will not show on Powershell but it does work, type your password anyway and press enter.
  - With this, you can type commands on your VM2 such as id, pwd, ls -lasth, etc.

![image](https://github.com/cardosoguisilva/azure-network-protocols/assets/157248613/85fd1c35-0c4c-4698-b599-58792f167fb0)

 
  
  

 

