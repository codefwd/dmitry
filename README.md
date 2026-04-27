# Using dmitry for information gathering
reconnaissance phase
## Overview
In this tutorial I am in the reconnaissance phase using the Deepmagic Information Gathering Tool
# Using Kali/dmitry to gather information from the public internet and a port scan on a virtual machine
Open source tools that directly probe the target can be used to gather information about it. Examining the target from an adversarial standpoint and determining the amount of information that can be obtained is helpful when testing for vulnerabilities. Kali offers numerous tools for collecting data. I'll use Dimitri to identify the public internet registration information of the yahoo website and i'll Port scan on a virtual machine on my network.

## First: public internet registration information of the yahoo.com website
The first thing that Dimitri provides is the target IP address:  
<img width="268" height="58" alt="the target IP address" src="https://github.com/user-attachments/assets/90e5405f-f198-4cc6-9a63-51531d302cdc" />

dmitry shows the Registration information of yahoo.com is in the internet address block 98.129.0.0 - 98.158.237.255
<img width="580" height="76" alt="address block" src="https://github.com/user-attachments/assets/d69cea36-6ae8-4770-a8e7-c4571a76036d" />

Now further along with the information gathering we found a wider IP address range for a series of subdomains:

<img width="472" height="430" alt="yahoo subdomains" src="https://github.com/user-attachments/assets/672cdcc3-abef-4253-86c4-ce1aa2f90f26" />

dmitry also identified a number of email addresses belonging to yahoo.com. this can be useful for an attacker crafting phishing attacks:

<img width="287" height="306" alt="email addresses" src="https://github.com/user-attachments/assets/480b23de-a8ec-42f0-83f8-a693fa5fb348" />

dmitry also checks for open ports on servers. We can see here that yahoo.com has an open web service:

<img width="563" height="188" alt="open web service" src="https://github.com/user-attachments/assets/3e56b3fb-cb2e-4b1c-8d86-cf1bf048bd3c" />

## Second: public internet registration information of the yahoo.com website

We can use dmitry for just Port scanning. I have a virtual machine running Metasploitable. I'll check the ports on my VM using a simple linux command with the minus P switch

$dmitry -pb 10.0.2.5

I also used the b switch to see what version of software is used for the port service. dmitry reports back on the most commonly used 150 ports.

<img width="571" height="577" alt="port scanning my VM metasploitable" src="https://github.com/user-attachments/assets/b37e51a0-d973-4c53-807b-a9acc40a218a" />

It gives me enough information to even show the software used 

For example the FTP Port 21 shows that the software used is ftpd 2.3.4 

## Conclusion:
dimitry can be used to do a whois lookup of a host, identify subdomains and scan a target looking for open ports. dmitry is a great tool that helps determine what systems are publicly visible on the internet so defenders can reduce exposure.

