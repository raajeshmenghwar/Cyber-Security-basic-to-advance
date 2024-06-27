# Cyber Security Roadmap: From Beginner to Advanced

## Disclaimer
This roadmap is designed for educational purposes only. Always use the tools and techniques mentioned here ethically and within legal boundaries.

## Step 1: Foundational IT Knowledge

### Complete CompTIA A+ Certification Syllabus
- **Resources:**
  - [CompTIA 220-1001 A+ Training Course - Professor Messer](https://www.professormesser.com/free-a-plus-training/220-1001/)
  - [CompTIA A+ Certification Video Course - PowerCert Animated Video](https://www.youtube.com/playlist?list=PLTAL7efVw9dtmQ_XZl5hrGM2y1UTs2h7N)

### Complete CompTIA Network+ Certification Syllabus
- **Resources:**
  - [CompTIA Network+ N10-007 Training Course - Professor Messer](https://www.professormesser.com/network-plus/n10-007/)
  - [CompTIA Network+ Certification Video Course - PowerCert Animated Video](https://www.youtube.com/playlist?list=PLTAL7efVw9dtmQ_XZl5hrGM2y1UTs2h7N)

### Complete CompTIA Security+ Certification Syllabus

- **Resources:**
  - [CompTIA Security+ SY0-501 Training Course - Professor Messer](https://www.professormesser.com/security-plus/sy0-501/sy0-501-training-course/)

## Step 2: Creating a Home Lab

### Minimum Requirements for Home Lab
![Laptop Specs](image.png)

### Virtualization Software
- **Install VMware Workstation or VirtualBox**
  - [VMware Workstation](https://www.vmware.com/products/workstation-pro/workstation-pro-evaluation.html)
  - [VirtualBox](https://www.virtualbox.org/)

## Step 3: Learn Linux

### Resources
- [Linux Basics for Hackers](https://www.amazon.com/Linux-Basics-Hackers-Networking-Scripting/dp/1593278551) by OccupyTheWeb
- [The Linux Command Line](https://linuxcommand.org/tlcl.php) by William Shotts

## Step 4: Get Hands-On with Top Cyber Security Tools

### OSINT Tools
- **Tools:**
  - Maltego
  - Ang-Roc
- **Resources:**
  - [TCM Security OSINT Tutorial](https://www.youtube.com/channel/UCk7v5cUsvYENKOxkV6h1FWA)

### Network Scanning Tools
- **Tools:**
  - netdiscover
  - Angry IP Scanner
  - Advanced IP Scanner
  - nmap
  - rustscan
  - Wireshark
  - tcpdump

### Offensive Tools
- **Tools:**
  - metasploit
  - Aircrack-ng
  - Burp Suite
  - OWASP-ZAP

### Password Cracking Tools
- **Tools:**
  - John the Ripper
  - Hashcat
  - Hydra

### Vulnerability Assessment
- **Tools:**
  - OpenVAS
  - Nessus

### Phishing Tools
- **Tools:**
  - Gophish
  - King Phisher
  - EvilURL
  - BlackEye
  - StormBreaker

### Encryption Tools
- **Tools:**
  - VeraCrypt
  - OpenSSL

### Defensive Tools
- **Tools:**
  - Snort
  - pfSense
  - ClamAV

### Forensics/Reverse Engineering Tools
- **Tools:**
  - Radare2
  - OllyDbg
  - Ghidra
  - x64dbg
  - IDA Pro

## Step 5: Advanced Topics

### Metasploit Framework
- **Overview:**
  Metasploit is a powerful tool for penetration testing, which allows you to find, exploit, and validate vulnerabilities. It includes various modules like exploits, payloads, and auxiliaries.
- **Resources:**
  - [Metasploit Unleashed](https://www.offensive-security.com/metasploit-unleashed/)
  - [Metasploit Documentation](https://docs.metasploit.com/)

### MSFvenom
- **Overview:**
  MSFvenom is a combination of Msfpayload and Msfencode, used to generate and encode payloads in various formats.
- **Resources:**
  - [MSFvenom Cheat Sheet](https://www.offensive-security.com/metasploit-unleashed/msfvenom/)

### Live Example
- **Scenario:**
  - Conduct a penetration test on a vulnerable machine (e.g., Metasploitable2)
  - Steps:
    1. Setup Metasploitable2 on VMware/VirtualBox
    2. Scan the network using `nmap` to identify open ports and services
    3. Use Metasploit to exploit a vulnerability found in the scan
    4. Gain access and demonstrate post-exploitation techniques

### Advanced Topics
- **ngrok:**
  - Tool to expose local servers behind NATs and firewalls to the internet.
  - [ngrok Documentation](https://ngrok.com/docs)

- **Obfuscation:**
  - Techniques to make malicious code harder to detect.
  - Tools:
    - Veil
    - Shellter
    - Hyperion

- **Obfuscation Techniques:**
  - Code obfuscation
  - Encryption
  - Polymorphism

## Conclusion

This roadmap provides a structured path for beginners to advance their skills in cyber security. Remember to continuously update your knowledge and practice ethically.

---

This structured guide ensures a comprehensive learning path from foundational IT knowledge to advanced cyber security techniques, using the latest tools and resources.