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

- Step 1 Create Our Resources
- Step 2 Observe different Types of Network Traffic



<h2>Actions and Observations</h2>

<h2>Create Our Resources</h2>
<p>
<img src="https://i.imgur.com/IxRBOmL.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create 2 Virtual Machine (VM) one running Windows 10 and name it "VM1". The other running Linux(Ubuntu) and name it "VM2". Select the  Resource Group and Vnet you created when you made VM1.
</p>
<br />

<h2>Install Wireshark onto Windows 10 VM1</h2>
<p>
<img src="https://i.imgur.com/EkZh6mf.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
Use Remote Desktop to connect to your Windows 10 Virtual Machine (VM).
</p>
<br />

<p>
<img src="https://i.imgur.com/uFX1sbY.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, install Wireshark on your Windows 10 Virtual Machine (VM)
</p>
<br />

<h2>Observing ICMP Traffic and Creating Inbound Security Rules</h2>
<p>
<img src="https://i.imgur.com/OoSGPCH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open Wireshark and type "ICMP" in the search barand press enter. Open PowerShell or a command line, and send a ping to VM2s private IP address. VM2s private IP address is located on Azure. Traffic will appear on Wireshark after the ping to VM2.
</p>
<br />

<p>
<img src="https://i.imgur.com/zLIGsGp.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open Network Security Groups in Azure. Set the port ranges to ICMP then set action to deny. Return to VM1 and observe the perpetual ping to VM2 timeout and observe the traffic.
</p>
<br />

<p>
<img src="https://i.imgur.com/I6bgTLc.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>In Powershell enter ssh labuser@VM2 Private IP address. Use your VM2 username and password (Password will not show in the box). Type ssh in Wireshark and press enter. Enter a Linux command: "id", "uname -a"  to observe traffic. 
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
