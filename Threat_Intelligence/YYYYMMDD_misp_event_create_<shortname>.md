# MISP Event Request —
**Author:** Badmus  
**Date:** 2025-01-19  
**Title:** BlazeStealer RAT - Discord C2 Malware with African Victims  
**Description:** Python-based RAT using Discord for C2 with confirmed Tunisia victim. Features UAC bypass, cryptocurrency wallet theft, ransomware capabilities, and advanced anti-analysis techniques.  
**Distribution:** Your organization only  
**Threat level:** High  
**Analysis level:** 2

## Attributes to add

| Indicator | Type | Category | Comment |
|-----------|------|----------|---------|
| 173.208.142.174 | ip-dst | Network activity | C2 server hosting payload delivery and remote access tools |
| MTQzODk3NTUzNjMyNzI5OTIwMg.GHmGBc.3RvtEDvgQCsmm1YYbpaoXogAv0GrLnFnDJh_UY | other | Network activity | Discord bot token used for C2 communication |
| discord.com | domain | Network activity | C2 communication via Discord API |
| raw.githubusercontent.com | domain | Network activity | Payload delivery for Discord injection module |
| BlazeSquad666/discord-injection | url | Network activity | GitHub repository hosting Discord token stealer |
| 31.215.240.196 | ip-src | Network activity | Confirmed victim IP address - Tunisia |
| f4:39:09:35:8e:09 | mac-address | Network activity | MAC address of confirmed Tunisia victim |
| C:\Windows\System32\Intel\ | filename | Payload delivery | Malware installation directory |
| conhost.exe | filename | Persistence mechanism | Registry Run key name for persistence |
| conhost_update | other | Persistence mechanism | Scheduled task name for persistence |
| HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Run | regkey | Persistence mechanism | Registry key used for startup persistence |
| C:\Windows\Tasks\p4yl0ad | filename | Payload delivery | UAC bypass payload file |
| C:\Windows\Tasks\EventViewerRCE.ps1 | filename | Payload delivery | PowerShell script for UAC bypass |
| eventvwr.exe | filename | Payload delivery | Legitimate binary abused for UAC bypass |
| hackedbyblazesquad2465 | other | Artifacts dropped | Default password set by malware |
| retireed_ | other | Attribution | Primary threat actor Discord username |
| oscaritoxx | other | Attribution | Secondary threat actor Discord username |
| 1432098418930487388 | other | Attribution | Primary threat actor Discord ID |
| 1225098902324117685 | other | Attribution | Secondary threat actor Discord ID |
| Klozy | other | Attribution | Malware author username |
| BlazeSquad666 | other | Attribution | Threat group identifier |
| icracked | other | Attribution | Contact information for malware author |

## MITRE ATT&CK techniques (TIDs + short justification)
**T1548.002** – Bypass User Account Control — Exploits EventViewer vulnerability using malicious XAML payload  
**T1555.003** – Credentials from Web Browsers — Steals passwords, cookies, and tokens from Chrome, Edge, Brave, Opera  
**T1005** – Data from Local System — Targets cryptocurrency wallets (MetaMask, Exodus, Electrum) and browser data  
**T1102.002** – Web Service C2 — Uses Discord bot for command and control communication  
**T1486** – Data Encrypted for Impact — Implements ransomware functionality with Fernet encryption  
**T1497.001** – Virtualization/Sandbox Evasion — Detects VMs via processes, drivers, and registry checks  
**T1562.001** – Impair Defenses — Disables Windows Defender, Task Manager, and security features  
**T1547.001** – Boot/Logon Autostart — Creates registry Run key and scheduled task for persistence  
**T1113** – Screen Capture — Takes screenshots and implements screenshot loops  
**T1056.001** – Input Capture — Implements keylogger functionality with pynput library  
**T1055** – Process Injection — Injects malicious code into Discord client for token theft  
**T1027** – Obfuscated Files or Information — Uses Base64 encoding and .NET serialization for payloads

## References
**Sandbox:** Not available - Python source code analysis  
**OSINT lead:** Discord C2 infrastructure analysis, victim identification via bot logs  
**Forensic appendix:** Complete malware source code analysis, IOC extraction, victim telemetry

## Confidence
**High**
