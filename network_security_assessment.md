# Network Security Assessment Report

**Date:** July 12, 2025  
**Author:** Suraj Vishwakarma  
**Task:** Final Task – Network Security Assessment (Internship)

---

## 🔍 Objective

To perform a network security assessment using Nmap and Wireshark, and document the findings, vulnerabilities, and observations.

---

## 🛠️ Tools Used

- **Nmap** – for scanning open ports and identifying active services.
- **Wireshark** – for capturing and analyzing live network traffic.

---

## ⚙️ Steps Performed

### 1. Nmap Scan
- Target IP: `10.0.2.15`
- Performed a scan on the local network to detect open ports and active services.
- Command used:
  ```
  nmap -sS -sV 10.0.2.15
  ```
- Output saved as `nmap_results.txt`.

### 2. Wireshark Traffic Capture
- Captured live network traffic using Wireshark.
- Interface selected: `eth0`
- Filter used: `http`
- Browsed a few websites to generate traffic.
- Output saved as `wireshark_capture.pcap`.

---

## 🔎 Observations

### From Nmap:
- Host was **up**
- Ports such as 22 (SSH), 80 (HTTP), and 443 (HTTPS) were scanned.
- Most ports were shown as closed or filtered (depending on the scan output).

### From Wireshark:
- HTTP request packets were observed.
- Some unencrypted HTTP traffic was visible which can be captured by attackers on the same network.
- No evidence of suspicious packets was found during brief capture.

---

## 🧠 Conclusion

This assessment shows that the target machine at `10.0.2.15` is live and reachable. No critical vulnerabilities were found, but monitoring HTTP traffic revealed that it can be intercepted if not encrypted. Tools like **Wireshark** and **Nmap** are helpful in early-stage assessments and must be followed by deeper analysis for serious auditing.

---

## 📎 Attached Files

- `nmap_results.txt`
- `wireshark_capture.pcap`

