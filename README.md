<p align="center">
<img src="https://i.imgur.com/9ln5C0j.png" alt="Networking pic"/>
</p>

<h1>Inspecting Network Traffic with Wireshark</h1>
In this lab I inspected network traffic between two machines utilizing Wireshark.<br />


<h2>Technology Utilized</h2>

- Microsoft Azure (Virtual Machines/Cloud)
- Remote Desktop
- Command Line tools (Windows & Linux)
- Various Network Protocols
- Wireshark

<h2>Operating Systems</h2>

- Ubuntu Server 20.04
- Windows 10 (21H2)

<h2>Overview of Tasks</h2>

- Provision a Windows 10 machine and a Ubuntu Server machine in Microsoft Azure.
- Download and Install Wireshark on the Windows machine.
- Ping the Ubuntu machine from the Windows machine.
- Change Firewall security rules on the Ubuntu machine and observe how this affects ping.
- Observe network traffic from different protocols in WireShark (ICMP, SSH, DHCP, DNS).

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/O4H3L4N.png" height="80%" width="80%" alt="ICMP"/>
</p>
<p>
I provisioned a Windows 10 Pro machine and a Ubuntu Server machine in Microsoft Azure. I connected with the Windows machine through RDP (Remote Desktop Protocol). I then downloaded Wireshark onto the Windows machine. In the Windows machine command line I sent a continuous ping (ping -t) to the Ubuntu machine. I observed the initial ping failure. I then configured the Ubuntu machine's Firewall Rules to allow ICMP inbound requests. I then observed the successful pings from the Windows machine. I then opened Wireshark and set a filter to display ICMP traffic. I observed the ICMP echo requests and echo replies for the ping process. I also observed the text sent in the ICMP traffic to be plaintext.
</p>
<br />

<p>
<img src="https://i.imgur.com/p6cmdVk.png" height="80%" width="80%" alt="SSH"/>
</p>
<p>
I then set the Wireshark filter to display SSH traffic. I connected to the Ubuntu machine from the Windows machine via SSH in the command line. I observed the SSH traffic in Wireshark. I noticed the messages in the SSH traffic to be encrypted. 
</p>
<br />

<p>
<img src="https://i.imgur.com/lwtBJzU.png" height="80%" width="80%" alt="DNS"/>
</p>
<p>
I then observed DNS and DHCP network traffic in Wireshark. I created these packets with "ipconfig /renew" and "Nslookup". 
</p>
<br />
