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

- Create Resource Groups and Virtual Machines
- Install & Run Wireshark
- Observe ICMP Traffic
- Observe SSH Traffic
- Observe DHCP Traffic
- Observe RDP Traffic


<h2>Create Resource Groups and Virtual Machines</h2>

<p>
<img src="https://i.imgur.com/S9Yg4oy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/knC6eiM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. Go to Virtual Machine Portal
<p>
 2. Create Virtual Machine
</p>
<br />

<p>
<img src="https://i.imgur.com/cETHG7u.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You can create a Resource Group when creating a Virtual Machine here
</p>
<br />

<p>
<img src="https://i.imgur.com/Mi33xad.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. Name the Machine VM1
 <p>
  2. Select regieon that is closes to you
  <p> 
   3. Create a Windows 10 image
   <p> 
    4. Make sure the size is at least 2 vcpu
    <p>
     5. Username and password
</p>
<br />

<p>
<img src="https://i.imgur.com/HlgQDkp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/HOEBq9f.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Make sure to create a default Virtual Network
</p>
<br />

<p>
<img src="https://i.imgur.com/tC3NNs7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. Name the Machine VM2
 <p>
  2. Select the same regieon as the first VM
  <p> 
   3. Create a Ubuntu Server(Linix) image
   <p> 
    4. Make sure the size is at least 2 vcpu
    <p>
     5. Username and password
</p>
<br />

<p>
<img src="https://i.imgur.com/UXFf8EE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Make sure you select the same Virtual Network
</p>
<br />


<p>
<img src="https://i.imgur.com/V7OldyP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/pLktSzM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/8CR44Qv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Double check and make sure all VMs that we created are on the same Network
</p>
<br />

<p>
<img src="https://i.imgur.com/u8k0hA6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 1. Virtual Machine -> Overview
 <p>
2. Copy the Public IP address 
</p>
<br />


<p>
<img src="https://i.imgur.com/LKMPaFr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1.Windows Start -> RDP
 <p>
  2. Paste VM1 IP address
</p>
<br />

<p>
<img src="https://i.imgur.com/xlDY3OQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Enter the credential of VM1
</p>
<br />

<h2>Install & Run Wireshark</h2>

<p>
<img src="https://i.imgur.com/xV2ei8m.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open a new Browser and google "Download Wireshark" and click on the first link 
</p>
<br />

<p>
<img src="https://i.imgur.com/YMpQAKr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download Windows installer 64 bit
</p>
<br />

<p>
<img src="https://i.imgur.com/mRoiZ5i.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/V2p0BRb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/DvpACq8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open download and navigate through and install
</p>
<br />

<p>
<img src="https://i.imgur.com/1Ib8AqO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/lCgoUWw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open Wireshark and observe the traffic comming through
</p>
<br />

<p>
<img src="https://i.imgur.com/6B3hmeD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/HGkdSRW.pngg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/ks4Rrva.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/vSMjHoV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/0ySUqvk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/Czwi4Gh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/hhNkvf5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/OiRuIal.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/RsgLlEX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/0rLSjov.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/u5mBDXs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/9bJ8btv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/8cillj3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

