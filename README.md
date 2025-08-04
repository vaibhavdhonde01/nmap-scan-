Nmap & Wireshark Analysis Report
📄 Overview
This report details a network scanning and packet analysis exercise using Nmap and Wireshark. It includes installation, scanning steps, analysis, and identification of potential vulnerabilities.

📂 File Information
File Name: Nmap_Wireshark_Report.pdf

Prepared By: Vaibhav Dhonde

Domain: Cybersecurity

Contents:

Nmap installation

IP range identification

TCP SYN scan execution

Scan results with open ports

Wireshark packet capture and analysis

Security risks

🛠 Tools Used
Nmap – Network scanning and port enumeration

Wireshark – Packet capturing and traffic analysis

✅ Steps Covered in Report
Install Nmap
Download from Nmap official website

Find Local IP Range

Windows:
ipconfig

Linux:
ifconfig
# or
ip addr
Perform TCP SYN Scan

nmap -sS [Target IP Address]
Example Output
Nmap scan report for 10.10.14.116
PORT   STATE SERVICE
21/tcp open  ftp
22/tcp open  ssh
80/tcp open  http
Wireshark Analysis

Start Wireshark before running the scan

Apply filters like:
tcp.port == 21
tcp.port == 22
tcp.port == 80

Common Services

Port 21 → FTP (File Transfer Protocol)

Port 22 → SSH (Secure Shell)

Port 80 → HTTP (Web Server)

Potential Security Risks

HTTP (80): No encryption, vulnerable to sniffing

SSH (22): Brute-force risk with weak passwords

FTP (21): Transmits data in plain text

⚠ Security Considerations
Do not scan unauthorized systems or networks

Use FTPS/HTTPS instead of FTP/HTTP for security

Enforce strong passwords for SSH

🔍 How to Reproduce
Install Nmap and Wireshark

Find your local IP range

Run:
nmap -sS <target-ip>
Open Wireshark, start capture, and filter packets by TCP port

