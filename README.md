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

- Create two VMs (Windows & Linux)
- Observe ICMP Traffic
- Observe SSH Traffic
- Observe DNS Traffic

<h2>Actions and Observations</h2>

<p>
<img width="666" alt="image" src="https://github.com/jckjr21/azure-network-protocols/assets/142818746/7ecce653-c3ea-4c05-88ac-815370c9a5d0">
</p>
<p>

1. Open the Network Security Group your Ubuntu VM is using and disable incoming (inbound) ICMP traffic

2. Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity

3. Re-enable ICMP traffic for the Network Security Group your Ubuntu VM is using

4. Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity (should start working)

5. Stop the ping activity

</p>
<br />

<p>
<img width="667" alt="image" src="https://github.com/jckjr21/azure-network-protocols/assets/142818746/536c8715-f370-403b-b69f-b2b67ba32fb6">
</p>
<p>

  1. Back in Wireshark, filter for SSH traffic only

2. From your Windows 10 VM, “SSH into” your Ubuntu Virtual Machine (via its private IP address)

    a. Type commands (username, pwd, etc) into the linux SSH connection and observe SSH traffic spam in WireShark

    b. Exit the SSH connection by typing ‘exit’ and pressing [Enter]

</p>
<br />

<p>
<img width="653" alt="image" src="https://github.com/jckjr21/azure-network-protocols/assets/142818746/255c4e05-7c7b-44eb-b746-0f3ce29ab0e8">
</p>
<p>

1. Back in Wireshark, filter for DNS traffic only

2. From your Windows 10 VM within a command line, use nslookup to see what google.com and disney.com’s IP addresses are

    a. Observe the DNS traffic being show in WireShark

</p>
<br />
