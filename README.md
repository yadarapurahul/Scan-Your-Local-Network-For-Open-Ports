# Scan-Your-Local-Network-For-Open-Ports
Scanned local network for open ports using Nmap on Kali Linux. Performed TCP SYN scan, research services and identified risks.

## Tools Used
- **Kali Linux**: Operating System for cybersecurity tasks.
- **Nmap 7.95**: Network Scanning tool pre-installed

## Steps
1. Firstly, you need to update your kali linux using **sudo apt update && sudo apt upgrade -y**
2. Nmap is pre-installed in Kali Linux. To confirm use the command **nmap --version**
3. If not installed then use the command **sudo apt install nmap -y**
4. For find local IP adddress use the command **ip a or ip addr show**
5. Run the *TCP SYN scan* using the command **sudo nmap -sS local IP address**.
6. Noted IP address and open ports from scan results.
7. Reserched common services on open ports using the command **sudo nmap -sS -sV local IP address**
8. Identified potential security risk associated with open ports.
9. I saved the result in text format using commands **sudo nmap -sS local IP address -oN file_name.txt**
10. I save as in also HTML format but directly not save HTML format then I do first saved in xml then convert to HTMl for xml command is**sudo nmap -sS local IP address -oX file_name** and HTMl command is **xsltproc file_name.xml -o file_name.html**
11. I captured screenshot of Nmap Version and scan process.

## Findings:
- **192.168.37.57**: port 53 (DNS-Domain Name system) open.
- **192.168.37.89**: port 3306 (MySQL) open.
- **192.168.37.248**: All 1000 scanned ports closed (reset).

## common Services
- **port 53 (DNS)**: Domain Name System, used for resolving domain names to IP addresses.
- **port 3306 (MySQL)**: MySQL database service, used for database management.

## Potential Security Risks
- **port 53 (DNS)**: Vulnerable to DNS spoofing or amplification attacks if not secured with DNSSEC or rate limiting.
- **port 3306 (MySQL)**: Risk of Unauthorize access or data leakage if default credentials or outdated versions are used; recommend strong passwords and updates.

## Files Included
- 'Local_Scan.txt': Nmap scan output in text format.
- 'Local_Scan.html': Nmap scan output in HTML format.
- 'updating the kali linux_1.jpg': Screenshot of updating or upgrading the kali linux.
- 'check nmap version_2.jpg': Screenshot of checking the nmap version or nmap is install or not.
- 'finding IP address_3.jpg': Screenshot of finding the IP address.
- 'TCP SYN scan_4.jpg': Screenshot of scanning the network of TCP SYN.
- 'Scanning each port_5.jpg': Screenshot of scanning the each open ports, researching and identifiying any potential security risk are there.
- 'result save in txt format_6.jpg': Screenshot of save the result nmap scan in the format text format.
- 'result save in html format_6.jpg': Screenshot of save the result nmap scan in the format HTML format.
