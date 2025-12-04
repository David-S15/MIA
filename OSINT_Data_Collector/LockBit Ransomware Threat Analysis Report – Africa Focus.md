# LockBit Ransomware Threat Analysis Report – Africa Focus

---

## 1. Executive Summary
LockBit remains one of the most prolific ransomware groups globally, significantly impacting African organisations across finance, government, and healthcare. Despite global crackdowns, LockBit continues to evolve with variants such as **LockBit 3.0, 4.0, and 5.0**, leveraging double extortion and advanced encryption.

### Key Findings
- **Primary targets:** South Africa, Nigeria, Egypt  
- **Attack vectors:** Exploitation of critical CVEs & phishing campaigns  
- **Estimated losses:** > **$3 billion** (2019–2025)

### Recommendations
- Immediate patching of CVEs  
- IOC monitoring in SIEM  
- Robust incident-response planning  

---

## 2. Background
- **Group:** LockBit (Ransomware-as-a-Service)  
- **Variants:** LockBit 3.0 (Black), LockBit 4.0, LockBit 5.0  
- **Tactics:** Double extortion, Monero-based ransom payments, exploitation of zero-day vulnerabilities  

---

## 3. Scope
- **Region:** Africa (South Africa, Nigeria, Egypt, Kenya)  
- **Sources:** Interpol Africa Cyberthreat Report, Cisco Talos, CISA, Kaspersky, Sophos IOC repositories, VirusTotal  

---

## 4. Methodology
OSINT collection via:
- Leak sites & dark-web forums  
- Threat-intel feeds (CISA, Rewterz, Sophos GitHub)

**Tools Used:** Maltego, SpiderFoot, Shodan, VirusTotal, Ransomware trackers  

---

## 5. Findings

### 5.1 Attack Trends
- **South Africa:** GEPF breach caused 6 days of disruption  
- **Egypt:** El Ezaby Pharmacy listed on LockBit leak site (2024)  
- **West Africa:** LockBit 3.0 used in privileged-credential attacks  

### 5.2 Targeted Sectors
- Finance  
- Government  
- Healthcare  

### 5.3 Techniques & Tactics

#### Exploited CVEs

| CVE | Affected System |
|------|-------------------------------|
| CVE-2023-4966 | Citrix ADC/Gateway |
| CVE-2021-34473 | Microsoft Exchange |
| CVE-2021-44228 | Apache Log4j2 |
| CVE-2018-13379 | Fortinet SSL VPN |

#### Initial Access Methods
- Phishing campaigns  
- Compromised IIS servers  
- PowerShell-based scripts  

---

## 6. Indicators of Compromise (IOCs)

### File Hashes (SHA-256)
- cea3e8a3e541ae4c928c3cd33f6772f1a69746393ac1a5c4575379a09a92d1e1  
- 0f178bc093b6b9d25924a85d9a7dde64592215599733e83e3bbc6df219564335  
- 80f2904d6b331cf689249df1c73e25eaf49a60960bccd46bb4a9816137036146  
- 917e115cc403e29b4388e0d175cbfac3e7e40ca1742299fbdb353847db2de7c2  
- b9678789f2c5a55de90d91da6ad03f1013fb77a984df35a0dd2cf333d1b3f820  

### IP Addresses
- 52.60.114.31  
- 198.244.187.248  
- 193.233.132.177  
- 93.190.143.101  

### Domains
- `lockbit7z2og4jlsmdy7dzty3g42eu3gh2sx2b6ywtvhrjtss7li4fyd.onion`  
- `lockbitapt.uz`  
- `info.openjdklab.xyz`  

### Ransom Note Indicators
- **Filenames:** `Restore-My-Files.txt`, `LockBit_Ransomware_ReadMe.txt`  
- **Language markers:** English + French variants  

---

## 7. Risk Assessment
- **Severity:** High  
- **Likelihood:** Increasing (RaaS expansion + leaked builder)  
- **Impact:** Operational, financial, reputational  

---

## 8. Recommendations
- Patch all critical CVEs immediately  
- Implement MFA with anti-MFA-bombing protection  
- Monitor all LockBit IOCs in SIEM  
- Maintain offline, immutable backups  
- Maintain up-to-date IR playbooks  

---

## 9. Appendices

### Glossary
- **Double Extortion:** Encrypting + leaking stolen data  
- **RaaS:** Ransomware-as-a-Service  
- **CVE:** Common Vulnerabilities and Exposures  

### References
- Interpol Africa Cyberthreat Report  
- Cisco Talos Q3 2025  
- CISA Advisories  
- VirusTotal  
- Ransomware.live  

---
