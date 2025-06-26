# 🔒 Task 3: Basic Network Vulnerability Assessment

## 🎯 Objective  
Conduct a vulnerability assessment using Nessus Essentials to detect potential security risks within a local network.

---

## 🧰 Tool Utilized  
**Tenable Nessus Essentials** – A widely adopted and free vulnerability scanning solution for identifying network threats.

---

## 🛠️ Scan Configuration  
- **Interface**: Nessus Web-Based Console  
- **Scan Mode**: Basic Network Scan  
- **IP Range Scanned**: `10.147.19.0/24`  
- **Scan Duration**: 29 minutes  
- **Number of Devices Scanned**: 2  
- **Scanning Policy**: Default Basic Network Scan  
- **Severity Rating System**: CVSS v3.0  

---

## 📊 Summary of Results  

### 📌 Overall Findings  
- **Total Detected Vulnerabilities**: 49  
- **Critical**: 0  
- **High**: 0  
- **Medium**: 22  
- **Low**: 1  
- **Informational**: 26  

---

### 🖥️ Vulnerabilities by Host

| Host IP         | Critical | High | Medium | Low | Info | Total |
|----------------|----------|------|--------|-----|------|-------|
| 10.147.19.244  | 0        | 0    | 17     | 1   | 91   | 109   |
| 10.147.19.239  | 0        | 0    | 5      | 0   | 104  | 109   |

---

## 🚨 Noteworthy Security Issues

### 🔶 Multiple Windows-Based Vulnerabilities
- **Category**: Operating System Weaknesses  
- **Details**: May include outdated patches, unsecured services, or misconfigured features  
- **Mitigation**:
  - Ensure systems are regularly updated
  - Apply system hardening techniques

### 🔶 SSL/TLS Configuration Issues
- **Impact**: Potential for data leakage or man-in-the-middle attacks  
- **Common Problems**:
  - Usage of outdated encryption protocols
  - Presence of self-signed or expired certificates  
- **Recommendations**:
  - Restrict to TLS 1.2 or higher
  - Replace certificates with valid, signed ones

---

### ⚠️ ICMP Timestamp Disclosure (Low Severity)
- **Plugin ID**: 10114  
- **CVE**: [CVE-1999-0524](https://nvd.nist.gov/vuln/detail/CVE-1999-0524)  
- **Impact**: Exposes system clock information which can assist in targeted attacks  
- **Solution**:
  - Disable ICMP timestamp responses through firewall settings

---

## 📦 Additional Observations

### ℹ️ Informational Data Points
- Banner grabbing of services like HTTP, SMB, SSH  
- Port scanning results  
- Detection of OS-specific characteristics  
- Network services disclosure (Netstat, service fingerprinting)

---

## ✅ Suggested Remediation Steps

### 🔧 Short-Term Actions
- Filter unnecessary ICMP traffic  
- Address Windows-related security advisories  
- Apply recommended SSL/TLS configurations  

### 🔄 Long-Term Strategy
- Schedule routine scans to stay updated on new threats  
- Keep software and systems patched consistently  
- Implement proper firewall policies  
- Educate team members on network security awareness  

---

## 🗂️ Quick Technical Overview

| Item            | Details                              |
|-----------------|--------------------------------------|
| Scan Label      | Vulnerabilities                      |
| Description     | Analyze internal LAN for weaknesses  |
| Target IP Range | 10.147.19.0/24                       |
| Execution Time  | 8:26 PM – 8:54 PM                    |
| Duration        | 29 minutes                           |

---
