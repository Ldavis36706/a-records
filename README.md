<p align="center">
<img src="https://i.imgur.com/RtQ7SeN.png" alt="DNS"/>
</p>

<h1>Domain Name System(DNS) CNAME Records </h1>
This tutorial outlines how to manage DNS records and understand CNAME Records.

.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- Command Line Interface

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Overview Steps</h2>

Step 1 CNAME Record Exercise
  - Connect/log into Domain Controller virtual machine as your domain admin account (mydomain.com\jane_admin)
  - Connect/log into Client virtual machine as an admin (mydomain\jane_admin)
  - Go to Domain Controller virtual machine and create a CNAME record that points the host “search” to “www.google.com”
  - Go to Client virtual machine and attempt to ping “search”, observe the results of the CNAME record
  - On Client virtual machine, nslookup “search”, observe the results of the CNAME record



<h2>Testing & Implementation Steps</h2>

<p>
<img src="https://i.imgur.com/aYuvFT0.png" height="80%" width="80%" alt="Pinging"/>
</p>
<p>
With CNAME records DNS server maps one hostname to another hostname. I attempted to ping(check for connectivity) to the hostname "search." There was no connectivity because there is no DNS record for "search."  
</p>
<br />

<p>
<img src="https://i.imgur.com/RcKvVlX.png" height="80%" width="80%" alt="Create CNAME DNS record"/>
</p>
<p>
I created a CNAME record titled "search." I made the "search" hostname map to hostname "www.google.com."
</p>
<br />

<p>
<img src="https://i.imgur.com/XvpEWN8.png" height="80%" width="80%" alt="Successful Ping"/>
</p>
<p>
I was able to ping the hostname "search" after creating a CNAME Record for it. This lab helps me better understand how DNS works.
  
  


