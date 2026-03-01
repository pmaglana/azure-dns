<p align="center">
<img width="606" height="247" alt="dnsbanner" src="https://github.com/user-attachments/assets/d9302ce5-6c22-40e4-8530-94c02b638548" />
</p>

<h1>Domain Name System Fundamentals</h1>

<h2>What is Domain Name System</h2>

<t>Domain Name System (DNS) is a hierarchical, distributed naming system that translates human-readable domain names (like google.com) into IP addresses (such as 142.250.190.14) that computers use to identify each other on a network. DNS enables users to access websites and services without needing to remember numeric IP addresses.</t>

<h2>About this Project</h2>
In this project we will be managing A-Record, and do some exercises on Local DNS Cache and CNAME Record.

<h2>Environment & Technology Used</h2>

- Microsoft Azure Virtual Machines 
- Microsoft Windows Server
- Microsoft Windows (Host machine)
- Remote Desktop

<h2>Prerequisites</h2>

- osTicket-Installation-Files.zip
- PHPManagerForIIS_V1.5.0.msi

<h2>Getting Started</h2>

<h3>A-Record Exercise</h3>

1. Connect/log into DC-1 as your domain admin account (mydomain.com\jane_admin)
2. Connect/log into Client-1 as an admin (mydomain\jane_admin)
3. From Client-1 try to ping “mainframe” notice that it fails
4. Nslookup “mainframe” notice that it fails (no DNS record)
5. Create a DNS A-record on DC-1 for “mainframe” and have it point to DC-1’s Private IP address
6. Go back to Client-1 and try to ping it. Observe that it works

<h3>Local DNS Cache Exercise</h3>

1. Go back to DC-1 and change mainframe’s record address to 8.8.8.8
2. Go back to Client-1 and ping “mainframe” again. Observe that it still pings the old address
3. Observe the local dns cache (ipconfig /displaydns)
4. Flush the DNS cache (ipconfig /flushdns).
5. Observe that the cache is empty (ipconfig /displaydns)
6. Attempt to ping “mainframe” again. Observe the address of the new record is showing up

<h3>CNAME Record Exercise</h3>

1. Go back to DC-1 and create a CNAME record that points the host “search” to “www.google.com”
2. Go back to Client-1 and attempt to ping “search”, observe the results of the CNAME record
3. On Client-1, nslookup “search”, observe the results of the CNAME record




<h2>Finishing Up</h2>
<h3>Congratulations for completing the DNS activities.</h3>


<sub>*For comments and question, please reach out to paulo@maglana.com*</sub>
