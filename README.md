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
