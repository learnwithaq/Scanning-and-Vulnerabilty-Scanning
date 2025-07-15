# Scanning & Vulnerability Scanning Commands
Scanning and Vulnerability Scanning


```bash
#check your own IP Address first
ifconfig

#use netdiscover to discover devices on our network
netdiscover -i eth0 -r 192.168.10.0/24

#ping scan all the network
nmap -sn 192.168.10.0/24

#To scan all ports
nmap -p- <target-ip>

#To scan specific port
nmap -p 80,443 <target-ip>

#To scan service version
nmap -sV <target-ip>

#To scan or guess the Operating System
nmap -sV -O <target-ip>

#To scan aggressively with T4 (Tier4)
nmap -sV -O -A -T4 <target-ip>

#Output the scan in txt format
nmap -sV -O -A -T4 <target-ip> -oN output-scan.txt

#Output the scan results in xml format
nmap -sV -O -A -T4 <target-ip> -oX output.xml

#To scan for Vulnerability
nmap -sV -O -A -T4 <target-ip> --script vuln

#Verifying vulnerablity using SEARCHSPLOIT in Kali Linux
searchsploit <vulnerable code / CVE>

#Verify vulnerabilty on exploit-db.com
https://exploit-db.com

#Verify vulnerability on cvedetails.com
https://cvedetails.com

#Verify vulnerability on google.com
Enter the vulnerability code or CVE on google.com and you will find them and their exploits
