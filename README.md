# 🌍 Project MIA: Malware Threat Intelligence in Africa

![Project Status](https://img.shields.io/badge/Status-Phase_1_Completed-success)
![Focus](https://img.shields.io/badge/Focus-Africa_Threat_Landscape-blue)
![Contributors](https://img.shields.io/badge/Team-DigitalFootprints_NYSC_2025-orange)

## 📌 Project Overview
**Project MIA (Malware Threat Intelligence in Africa)** is a 3-month pilot research initiative aimed at studying, analyzing, and documenting emerging malware threats targeting African users and organizations. 

Carried out by the **DigitalFootprints Corp Members (NYSC Batch 2025)**, this project serves as both a practical threat intelligence training platform and a functional research contribution to the broader African cybersecurity community. Our core mandate was to identify regional threats, analyze payloads in isolated environments, and extract actionable Intelligence (IOCs, MITRE mappings, and detection rules).

---

## 📂 Repository Navigation

This repository is organized by operational function to streamline research and handovers. Below is the guide to our directory structure and key deliverables:

### 📑 `General/` (Executive Reports)
This directory serves as the main hub for all finalized intelligence reports and executive summaries.
* **[BlazeStealer Full Intelligence Report](https://github.com/David-S15/MIA/blob/main/General/BlazeStealer_Full_Intelligence_Report.md):** Our primary, completed deep-dive investigation attributing the BlazeStealer RAT threat actors and identifying actively compromised targets (including a confirmed African victim in Tunisia).

### 🕵️ `OSINT_Data_Collector/` (Data & Automation)
This folder contains the data gathered during our research, specifically focusing on the ransomware threat landscape in Africa, alongside the Python automation scripts built for API collection.
* **[LockBit Ransomware Threat Landscape Report](https://github.com/David-S15/MIA/blob/main/OSINT_Data_Collector/LOCKBIT%20RANSOMWARE%20THREAT%20LANDSCAPE%20IN%20AFRICA%20(2019%E2%80%932026).md):** A comprehensive handover report detailing LockBit's targeting of African infrastructure and localized economic damage projections.
* Includes all historical datasets (CSV) of LockBit victims across the continent.

### 🎯 `Threat_Intelligence/` & 🦠 `Malware_Analysis/`
These directories contain the raw technical outputs of our investigations.
* **Indicators of Compromise (IOCs):** Structured CSV datasets containing C2 domains, hashes, and IP addresses ready for MISP and SIEM ingestion.
* **Detection Rules:** Custom YARA, Snort, and Sigma rules written to defend against the payloads analyzed during this pilot.

### 🔍 `Digital_Forensics/`
*Status: On Hold* This directory was provisioned for memory and disk forensic workflows. Due to the adjusted NYSC Passing Out Parade (POP) schedule, dedicated forensic analysis was placed on hold .

---

## 🚀 How to Use the OSINT Scripts
If you are taking over the OSINT data collection (e.g., the LockBit API scraper), please navigate to the `OSINT_Data_Collector/` folder. 

Ensure you have your dependencies installed:
```bash
pip install requests pandas matplotlib
