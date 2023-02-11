<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this demonstration, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDP, DNS, DHCP, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1: Deploy Windows 10 and Ubuntu Virtual Machines
- Step 2: Run Windows 10 Virtual Machine and install Wireshark from the net
- Step 3: Connect with Ubuntu VM via PowerShell or command prompt, while observing various network protocols in Wireshark

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/2RXOkFp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
"/>
</p>
<p>
Traffic is being observed via a nonstop ping, with Wireshark displaying ICMP communication. Contact with VM2's private IP address is successful. (10.0.0.5 is the private IP of VM2)
</p>
<br />

<p>
<img src="https://i.imgur.com/88FYPhq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
"/>
</p>
<p>
<img src="https://i.imgur.com/VW3720l.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
A new security rule has been created in order to stop the nonstop ping. The second image shows that the rule has been successfully applied. 
</p>
<br />

<p>
<img src="https://i.imgur.com/eHIwJRU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
"/>
</p>
<p>
<img src="https://i.imgur.com/gQvDx5j.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
The security rule is being edited in order to allow nonstop traffic to resume. In this case, the action is being switched from 'Deny' to 'Allow' and then saved. The second image shows the completion of the edit, with resumed traffic and VM2's private IP re-appearing in Wireshark.  
</p>
<br />

<p>
<img src="https://i.imgur.com/gesDY5w.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Secure shell is being utilized to 'log in' to VM2's private IP address (Provides security over otherwise unsecure network). 
</p>
<br />

<p>
<img src="https://i.imgur.com/UE9TE5R.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
DNS is displayed in Wireshark, and PowerShell is being utilized to retrieve the IP address of a public website.
</p>
<br />

<p>
<img src="https://i.imgur.com/tp2A2Ob.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
DHCP is being utilized to issue a new IP address to the Windows 10 VM (VM1), which is displayed in Wireshark. 

  <p>
<img src="https://i.imgur.com/sxS8sjJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
RDP is being utilized via port number 3389 to connect to  VM2. Non-stop traffic is displayed in Wireshark as a sign of remote access to the Ubunt VM (VM2).
