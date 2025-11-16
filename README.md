Network Scan & Vulnerability Assessment – Task 1

Overview:
This repository contains the deliverables for Task 1 of my cybersecurity internship: scanning a local network, identifying exposed services, and documenting potential security risks. The objective was to understand network exposure through port scanning and translate raw Nmap output into security insights with actionable recommendations.

All sensitive information (IP addresses, MAC addresses, environment details) has been sanitized intentionally.

Workflow Summary:
-Identified the target network range using 'ifconfig'.
-Inspected local interface to determine subnet (e.g., 172.X.X.X/24).
-Performed a TCP SYN scan using Nmap.
-Command used:
 nmap -sS -oN scan_results.txt X.X.X.X/24
 Chosen because SYN scans are fast, stealthy, and commonly used for reconnaissance.

Analyzed open & filtered ports:
-Looked up service behavior and known security risks.
-Mapped findings to real-world attack scenarios (FTP plaintext auth, DNS zone transfers, SMB/EternalBlue risk, etc.).
-Assessed risk levels.
-High-risk host identified due to exposed insecure legacy protocols (FTP) and potentially misconfigured DNS service exposed to the network.
-Medium-risk host with firewall protection but vulnerable if misconfigured.

Repository Contents
Task1.docx            → Full report (sanitized)
scan_results.txt      → Sanitized Nmap output
.gitignore            → Protects sensitive artifacts from being uploaded
README.md             → This documentation

Tool(s) Used:
Nmap 7.94SVN – primary scanning tool

Notes
-All data in this repo is intentionally sanitized for public sharing.
-Raw scan output and internal details were not uploaded.
-This workflow reflects standard security assessment practices with a focus on responsible handling of evidence.
