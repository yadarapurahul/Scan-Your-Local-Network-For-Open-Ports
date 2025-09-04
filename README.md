# Scan-Your-Local-Network-For-Open-Ports
Scanned the local network for open ports using Nmap on Kali Linux. Performed TCP SYN scan and research services and identified risks.

## Tools Used
- **Kali Linux**: Operating system for cybersecurity tasks.
- **Nmap 7.95**: Network Scanning tool pre-installed

## Steps
1. Firstly, you need to update your kali linux using **sudo apt update && sudo apt upgrade -y**
2. Nmap is pre-installed in Kali Linux. To confirm use the command **nmap --version**
3. If not installed then use the command **sudo apt install nmap -y**
4. To find local IP address, use the command **ip a or ip  addr show**
5. Run the *TCP SYN scan* using the command **sudo nmap -sS local IP address**.
6. Noted IP address and open ports from scan results.
7. Researched common services on open ports using the command **sudo nmap -sS -sV local IP address**
8. Identified potential security risks associated with open ports.
9. I saved the result in text format using the command **sudo nmap -sS local IP address -oN file_name.txt**
10. I save as in also HTML format, but I do not directly save HTML format. I do first saved in XML, then convert to  HTML, for the XML command is **sudo nmap -sS local IP address -oX file_name** and the HTML command is **xsltproc file_name.xml -o file_name.html**
11. I captured a screenshot of the Nmap version and the scan process.

## Findings:
- **192.168.37.57**: port 53 (DNS-Domain Name System) open.
- **192.168.37.89**: port 3306 (MySQL) open.
- **192.168.37.248**: All 1000 scanned ports closed (reset).

## common Services
- **port 53 (DNS)**: Domain Name System, used for resolving domain names to IP addresses.
- **port 3306 (MySQL)**: MySQL database service, used for database management.

## Potential Security Risks
- **port 53 (DNS)**: Vulnerable to DNS spoofing or amplification attacks if not secured with DNSSEC or rate limiting.
- **Port 3306 (MySQL)**: Risk of unauthorized access or data leakage if default credentials or outdated versions are used; recommend strong passwords and updates.

## Files Included
- 'Local_Scan.txt': Nmap scan output in text format.
- 'Local_Scan.html': Nmap scan output in HTML format.
- 'updating the kali linux_1.jpg': Screenshot of updating or upgrading the Kali Linux.
- 'check nmap version_2.jpg': Screenshot of checking the nmap version or whether nmap is installed or not.
- 'finding IP address_3.jpg': Screenshot of finding the IP address.
- 'TCP SYN scan_4.jpg': Screenshot of scanning the network of TCP SYN.
- 'Scanning each port_5.jpg': Screenshot of scanning each open port, researching, and identifying any potential security risks that are there.
- 'result save in txt format_6.jpg': Screenshot of saving the result of the Nmap scan in the text format.
- 'result save in html format_6.jpg': Screenshot of saving the result of the Nmap scan in the HTML format.
