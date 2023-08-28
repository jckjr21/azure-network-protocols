- Create two VMs (Windows & Linux)
- Observe ICMP Traffic
- Observe SSH Traffic
- Observe RDP Traffic

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
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

  1. Back in Wireshark, filter for SSH traffic only

2. From your Windows 10 VM, “SSH into” your Ubuntu Virtual Machine (via its private IP address)

    a. Type commands (username, pwd, etc) into the linux SSH connection and observe SSH traffic spam in WireShark

    b. Exit the SSH connection by typing ‘exit’ and pressing [Enter]

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
