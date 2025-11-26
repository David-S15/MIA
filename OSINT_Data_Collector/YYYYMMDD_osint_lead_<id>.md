# BlazeStealer Malware Report

BlazeStealer is a malicious infostealer malware that specifically targets developers by masquerading as legitimate Python obfuscation tools in the Python Package Index (PyPI).

📌 Sources:  
- [The Hacker News](https://thehackernews.com/2023/11/beware-developers-blazestealer-malware.html?utm_source=chatgpt.com)  
- [SecurityWeek](https://www.securityweek.com/blazestealer-malware-delivered-to-python-developers-looking-for-obfuscation-tools/?utm_source=chatgpt.com)  
- [Hive Pro](https://www.hivepro.com/wp-content/uploads/2023/11/BlazeStealer-Malware-Uncovered-in-Python-Packages-on-PyPI_TA2023454.pdf?utm_source=chatgpt.com)  
- [Checkmarx](https://checkmarx.com/blog/python-obfuscation-traps/?)  
- [ThreatsHub](https://www.threatshub.org/blog/blazestealer-python-malware-allows-complete-takeover-of-developer-machines/?utm_source=chatgpt.com)  
- [IAES](https://iaes.or.id/waspada-para-pengembang-malware-blazestealer-kini-terdeteksi-dalam-paket-python-di-pypi/?utm_source=chatgpt.com)  
- [WithSecure](https://www.withsecure.com/content/dam/with-secure/documents/threat-reports/WS_Threat_Highlight_report_November_2023_en.pdf?utm_source=chatgpt.com)  

---

## 1. Campaign Overview
- **Start Date:** January 2023  
- **Distribution:** Attackers used **eight malicious PyPI packages** disguised as obfuscation tools.  
- **Package Names:**  
  - `Pyobftoexe`  
  - `Pyobfusfile`  
  - `Pyobfexecute`  
  - `Pyobfpremium`  
  - `Pyobflite`  
  - `Pyobfadvance`  
  - `Pyobfuse`  
  - `pyobfgood`  

---

## 2. Infection Vector & Distribution
- **PyPI Packages:** Published as fake obfuscation tools.  
- **Malicious Script Fetching:**  
  - Setup scripts (`setup.py` / `__init__.py`) fetch external payloads from `transfer[.]sh`.  
  - Payload = BlazeStealer malware.  

---

## 3. Capabilities & Behaviour
BlazeStealer provides a **Discord bot** as its command-and-control (C2) interface.

### Main Features
- **Data Exfiltration**  
  - Steals browser credentials  
  - Captures screenshots  
  - Keylogging  
  - Harvests host information  

- **Remote Command Execution**  
  - Executes arbitrary commands  
  - Downloads additional files  

- **System Disruption**  
  - Disables Microsoft Defender Antivirus  
  - Disables Task Manager  
  - Overloads CPU → shutdown  
  - Forces Blue Screen of Death (BSOD)  

- **File Encryption / Ransom**  
  - Encrypts user files (espionage + ransom motive)  

- **Camera Access**  
  - Installs `WebCamImageSave.exe`  
  - Captures photo → sends via Discord → deletes traces  

- **Psychological Component**  
  - Sends mocking/threatening messages via Discord bot  

---

## 4. Target Profile & Motivation
- **Primary Target:** Developers (esp. those using obfuscation tools).  
- **Motivation:**  
  - Access to proprietary code & sensitive data  
  - Credential theft (including crypto wallets)  
  - Espionage + ransom  

---

## 5. Impact & Risk
- **Security Risks:**  
  - Complete system compromise  
  - Data breach (credentials, personal data)  
  - Privacy violation (screenshots, webcam)  
  - Persistent C2 via Discord  

- **Operational Risks:**  
  - System instability (CPU overload, BSOD)  
  - Security bypass (Defender, Task Manager disabled)  
  - Supply chain risk via PyPI  

- **Prevalence:**  
  - ~2,438 downloads before removal  
  - Geographical spread: US, China, Russia, Ireland, Hong Kong, Croatia, France, Spain  

---

## 6. Detection & Analysis
- **Threat Intelligence Reports:**  
  - Checkmarx  
  - WithSecure  

- **Indicators of Compromise (IoCs):**  
  - Malicious package names (listed above)  
  - Remote fetching domain: `transfer[.]sh`  
  - Discord-based C2  

---

## References
1. [Hive Pro](https://www.hivepro.com/wp-content/uploads/2023/11/BlazeStealer-Malware-Uncovered-in-Python-Packages-on-PyPI_TA2023454.pdf?utm_source=chatgpt.com)  
2. [Checkmarx](https://checkmarx.com/blog/python-obfuscation-traps/?)  
3. [ThreatsHub](https://www.threatshub.org/blog/blazestealer-python-malware-allows-complete-takeover-of-developer-machines/?utm_source=chatgpt.com)  
4. [The Hacker News](https://thehackernews.com/2023/11/beware-developers-blazestealer-malware.html?utm_source=chatgpt.com)  

---
 
## Metadata
- **Collector:** David  
- **Source:** Social  
