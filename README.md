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

- Create a Network Security Group (NSG)
- Associate the NSG
- Define Security Rules to Inspect Traffic
- Traffic Evaluation and Logging

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/GsRnimP.png[/img] height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a resource group, then create a Windows 10 virtual machine and select that resource group during setup, allowing Azure to automatically create a new virtual network and subnet. Next, create a Linux (Ubuntu) virtual machine, again selecting the same resource group and the same virtual network, using username/password authentication. Ensure that both virtual machines are deployed within the same virtual network and subnet.
</p>
<br />

<p>
<img src="https://i.imgur.com/87KdB4E.png[/img] height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
If you are using a Mac, install Microsoft Remote Desktop and use it to connect to your Windows 10 virtual machine. Once connected to the Windows 10 virtual machine, install Wireshark to enable network traffic capture and analysis.
</p>
<br />

<p>
<img src="https://i.imgur.com/et4Tyvd.png[/img] height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/y2AsdOg.png[/img] height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Within the Windows 10 virtual machine, install Wireshark, open the application, and start a packet capture. Apply a filter to display only ICMP traffic, then retrieve the private IP address of the Ubuntu virtual machine and attempt to ping it from the Windows 10 virtual machine.
</p>
<br />

<p>
<img src="https://i.imgur.com/tOuDxb5.png[/img] height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Observe the ICMP ping requests and replies in Wireshark, then from the Windows 10 virtual machine open Command Prompt or PowerShell and ping a public website such as **[www.google.com](http://www.google.com)**, monitoring the resulting network traffic in Wireshark.
</p>
<br />

<p>
<img src="https://i.imgur.com/ab6ulMi.png[/img] height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>
<img src="https://i.imgur.com/TVP6bun.png[/img] height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>
<img src="https://i.imgur.com/8Ebspan.png[/img] height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>
<img src="https://i.imgur.com/6HBvclz.png[/img] height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Begin by sending a continuous ping from the Windows 10 virtual machine to the Ubuntu virtual machine. Then, access the Network Security Group assigned to the Ubuntu VM and block inbound ICMP traffic. Switch back to the Windows 10 VM and monitor the results using Wireshark along with the ping command output. After observing the blocked traffic, re-enable inbound ICMP in the Network Security Group. Return to the Windows 10 VM to verify that ICMP traffic is flowing again in Wireshark and that the ping responses resume. Once confirmed, stop the ping process.
</p>
<br />

<p>
<img src="https://i.imgur.com/sJdctRu.png[/img] height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Sign back into the Windows virtual machine and launch Wireshark to begin a new packet capture. Set a display filter to show only SSH traffic. Using the Windows 10 VM, initiate an SSH connection to the Ubuntu virtual machine through its private IP address by opening PowerShell and entering ssh labuser@<private IP address>. As you authenticate and run commands within the Linux session, watch the SSH traffic populate in Wireshark. Once you are done, close the SSH session by typing exit and pressing Enter.
</p>
<br />

<p>
<img src="https://i.imgur.com/3RoYHVD.png[/img] height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Return to Wireshark and apply a filter to display only DNS traffic. From the Windows 10 virtual machine, open a command-line window and use the nslookup command to find the IP addresses associated with google.com and disney.com. As the queries run, observe the corresponding DNS traffic appearing in Wireshark.</p>
<br />
