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
Cloud Infrastructure Setup (Microsoft Azure)
  
- Created and configured a resource group to manage cloud resources efficiently
- Deployed a Windows 10 virtual machine, allowing Azure to automatically provision a virtual network and subnet
- Provisioned a Linux (Ubuntu) virtual machine within the same resource group and virtual network
- Configured username/password authentication for secure access
- Ensured both virtual machines operated within the same virtual network and subnet to enable internal communication
</p>
<br />

<p>
<img src="https://i.imgur.com/87KdB4E.png[/img] height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Remote Access & Network Analysis Setup

- Installed Microsoft Remote Desktop on macOS to enable secure remote access to a Windows 10 virtual machine
- Established remote connection to a cloud-hosted Windows environment for system management and testing
- Installed Wireshark to capture and analyze network traffic
- Performed basic network packet analysis to monitor and evaluate communication between systems
</p>
<br />

<p>
<img src="https://i.imgur.com/et4Tyvd.png[/img] height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/y2AsdOg.png[/img] height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Network Traffic Analysis (ICMP Testing)

- Installed and configured Wireshark within a Windows 10 virtual machine to capture live network traffic
- Initiated packet captures and applied ICMP filters to isolate specific network activity
- Retrieved and utilized the private IP address of a linux (Ubuntu) virtual machines for connectivity testing
- Executed ping test (ICMP requests/replies) between virtual machines to validate network communication
- Analyzed packet date to verify successful transmission and troubleshoot connectivity within a virtual network
</p>
<br />

<p>
<img src="https://i.imgur.com/tOuDxb5.png[/img] height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Network Monitoring & External Connectivity Testing

- Monitored ICMP request and reply traffic using Wireshark to analyze communication between virtual machines
- Utilized Command Prompt/Powershell within a Windows 10 virtual machine to execute network diagnostics
- Performed connectivity tests to external hosts (e.g., Google) using ping commands
- Captured and analyzed network traffic to observe external vs. internal communication behavior
- Validated outbound network connectivity and assessed response patterns through packet inspection 
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
Network Security Group (NSG) Testing & Traffic Conrol

- Conducted continuous ICMP testing between Windowsand Linux virtual machines to monitor real-time connectivity
- Configured Nertwork Security Group (NSG) rules ro block inbound ICMP traffic to a virtual machine
- Observed and analyzed dropped packets using Wireshark and command-line ping results
- Re-enabled ICMP traffic within NSG settings to restore connectivity between systems
- Validated network rule changes by confirming traffic flow resumption and successful ping responses
- Demonstrated unsderstanding of firewall rules, network security controls, and traffic filtering in a cloud environment
</p>
<br />

<p>
<img src="https://i.imgur.com/sJdctRu.png[/img] height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
SSH Traffic Analysis & Secure Remote Access

- Captured and analysed SSH traffic using Wireshark within a Windows 10 virtual machine
- Applied protocol-specific filters to isolate SSH (Secure Shell) network activity
- Established secure remote access to a Linux (Ubuntu) virtual machine via SSH using private IP addressing
- Authenticated and excuted commands within a remote Linux session to simulate administrative tasks
- Monitored encrypted SSH traffic in real time to understand secure communication behavior
- Validated session termination and traffic patterns upon closing the SSH connection

Lab Coverage on:

- Cloud (Azure)

- Networking (ICMP, NSG)

- Security (firewall rules, SSH)

- Tools (Wireshark, Poershell)
</p>
<br />

<p>
<img src="https://i.imgur.com/3RoYHVD.png[/img] height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
DNS Traffic Analysis & Name Resolution Testing

- Captured and analyzed DNS traffic using Wireshark within a Windows 10 virtual machine
- Applied protocol filters to isolate DNS query and response traffic
- Utilized command-line tools (nslookup) to perform domain name resolution for external sites (e.g., Google and The Walt Disney Company
- Mapped domain names to corresponding IP addresses to validate DNS functionality
- Observed and analyzed real-time DNS queries in packet captures to understand network resolution processes

Networking lab project section covering:
  
  -ICMP (ping)
  
  -DNS
  
  -SSH
  
  -Network security (NSG)
  
  -Packet analysis (Wireshark)
<br />
