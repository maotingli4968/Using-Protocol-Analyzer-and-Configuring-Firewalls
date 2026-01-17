<p align="center">
  <img src="https://github.com/user-attachments/assets/a56b5bfe-f82f-4639-a1f5-d95cb35d53ca"
       alt="image"
       width="700" />
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines how to use Wireshark to capture and filter ICMP (ping) traffic between the VMs, and configure Azure NSG inbound rules to block and then re-enable ICMP to observe the change in packet behavior.


<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop Protocol (RDP)
- WireShark (Protocol Analyzer / Packet Sniffer)
- Network Security Group (NSG) in Azure


<h2>Operating Systems Used </h2>

- Windows 10 Pro (Remote VM)
- Ubuntu Linux (Remote VM)
- macOS (for running Microsoft Remote Desktop on local machine)


<h2>List of Prerequisites</h2>

- Windows 11 pro and Linux Virtual Machines created
- Public IP address of the Windows VM
- Private IP address of the Linux VM
- Azure Portal access to manage VM networking and NSG rules
- Microsoft Remote Desktop installed (Mac users download from the App Store)



<h2>Connect to the Windows VM with RDP</h2>

 Open Microsoft Remote Desktop and click Add a PC.
  - Enter the public IP address of the Windows VM as the PC name.
  - Use a friendly name like Windows-VM.
  - Log in with the credentials you created earlier.

<h2>Connect to the Windows VM with RDP</h2>

- Inside the Windows VM, open Microsoft Edge and go to https://www.wireshark.org. 
- Download the Windows 64-bit installer.
- During Setup:
  - Accept default options during setup.
  - Install Npcap (needed for packet capture).
  - Skip USBPcap (not required).
  - Finish the installation and open WireShark.
 
<h2>Connect to the Windows VM with RDP</h2>

- Open WireShark and select the Ethernet interface (the one showing traffic activity).
- Click the shark fin icon in the top left to start capturing.
- You’ll see a continuous stream of packets representing the network traffic to and from your Windows VM

<p align="center">
  <img src="https://github.com/user-attachments/assets/5168c2aa-1815-43ab-bdb5-2907ba5db33a"
       alt="image"
       width="700" />
</p>

<h2>Filter for ICMP (Ping) Traffic</h2>
In the WireShark filter bar, type "icmp" and press Enter. This shows only ICMP traffic, which is used by the ping command to test connectivity. 

<h2>Retrieve Private IP of Linux VM</h2>
In the Azure Portal, open your Linux VM → Networking → Private IP address. 
Copy the IP (e.g., 10.0.0.5). You’ll use this to test connectivity from Windows VM.



<h2>Ping Linux VM from Windows VM</h2>
Inside the Windows VM, open PowerShell and type:

<p align="center">
  <img src="https://github.com/user-attachments/assets/c70382a4-0fc4-47af-8381-79f24ef51dbc"
       alt="image"
       width="700" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/b2f819e2-be3a-40d7-92f4-bf20ca4d2918"
       alt="image"
       width="700" />
</p>













<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
