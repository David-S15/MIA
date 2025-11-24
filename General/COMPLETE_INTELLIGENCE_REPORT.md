# 🚨 BLAZESTEALER RAT - COMPLETE INTELLIGENCE REPORT

## EXECUTIVE SUMMARY
**Malware Family:** BlazeStealer RAT / BlazeSquad RAT  
**Threat Level:** CRITICAL  
**African Connection:** ✅ CONFIRMED (Tunisia Victim)  
**Active Victims:** 3 Confirmed  
**Threat Actors:** 2 Identified  
**Report Date:** 2025-01-19

---

## 1. INDICATORS OF COMPROMISE (IOCs)

### Network IOCs
```
C2 Discord Bot Token: [REDACTED}
Discord Guild ID: [REDACTED}
C2 Payload Server: http://173.208.142.174:8080/files/remotepc.zip
C2 Payload Server: http://173.208.142.174:8080/files/libopus-0.x64.dll
GitHub Injection: https://raw.githubusercontent.com/BlazeSquad666/discord-injection/main/injection.js
```

### File System IOCs
```
Malware Path: C:\Windows\System32\Intel\
Registry Key: HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Run\conhost.exe
Scheduled Task: conhost_update
Remote Access Path: %LOCALAPPDATA%\RemotePC\server.exe
```

### IP Addresses
```
C2 Server: 173.208.142.174:8080
Victim 1 (Tunisia): 31.215.240.196
```

### MAC Addresses
```
Victim 1: f4:39:09:35:8e:09
```

---

## 2. CONFIRMED VICTIMS

### 🇹🇳 VICTIM 1: TUNISIA (NORTH AFRICA) - CONFIRMED AFRICAN CONNECTION
```
Username: uare
PC Name: DESKTOP-0V99OKA
IP Address: 31.215.240.196
Location: TUNISIA 🇹🇳 (North Africa)
OS: Windows 10 (64-bit, Build 19045)
CPU: Intel Core i5-9400 (4 cores, Model 158 Stepping 11)
RAM: 11.83GB
GPU: Microsoft Basic Display Adapter
Screen: 1920x1080
MAC: f4:39:09:35:8e:09
BIOS: F.48 (HPQOEM - 1072009)
Infection Date: November 16, 2025, 21:25:03 UTC
Last Active: November 16, 2025, 22:31:59 UTC
Status: ACTIVE - Malware persistent on reboot
```

**Attack Timeline:**
- 21:25:03 - Initial infection, system information exfiltrated
- 21:25:10 - Malware added to startup (persistent)
- 21:25:11 - Startup persistence confirmed
- 21:27:36 - Heartbeat check-in
- 21:43:33 - Heartbeat check-in
- 22:02:21 - Heartbeat check-in
- 22:31:59 - Last heartbeat check-in

**Threat Actor Activity on Victim 1:**
- 21:36:36 - retireed_ attempted `.tokens` command
- 21:37:28 - retireed_ attempted `.help` command
- 21:46:21 - oscaritoxx attempted `.tokens` command
- 22:04:42 - retireed_ attempted `.encryptfiles` (ransomware)
- 22:05:08 - retireed_ attempted `.usernamefucker` (account takeover)
- 22:05:19 - retireed_ attempted `.ransom` (full system lock)
- 13:01:05 (Nov 17) - retireed_ attempted `.cap` (screenshot)

### VICTIM 2: Bruno
```
Username: Bruno
PC Name: DESKTOP-ET51AJO
IP Address: NOT EXTRACTED
Location: UNKNOWN
First Seen: November 17, 2025, 00:59:27 UTC
Last Active: November 17, 2025, 16:31:02 UTC
Status: ACTIVE - Malware persistent on reboot
```

**Attack Timeline:**
- 00:59:27 - Initial infection
- 16:31:02 - Last heartbeat (15 hours later)
- 16:31:11 - Startup persistence confirmed
- 16:31:17 - Bot sent help command prompt

**Threat Actor Activity on Victim 2:**
- 16:31:17 - Bot prompted for commands
- 18:51:05 - retireed_ attempted `.help`
- 18:52:07 - oscaritoxx sent malicious command

### VICTIM 3: james
```
Username: james
PC Name: DESKTOP-0H1EJSV
IP Address: NOT EXTRACTED
Location: UNKNOWN
First Seen: November 18, 2025, 00:53:51 UTC
Last Active: November 18, 2025, 01:45:22 UTC
Status: ACTIVE - Malware persistent on reboot
```

**Attack Timeline:**
- 00:53:51 - Initial infection
- 01:45:22 - Last heartbeat
- 01:45:31 - Startup persistence confirmed

**Threat Actor Activity on Victim 3:**
- 21:33:11 - retireed_ attempted `.tokens` command

---

## 3. THREAT ACTOR ATTRIBUTION

### Primary Operator: retireed_ (👹)
```
Discord ID: 1432098418930487388
Discord Username: retireed_
Display Name: 👹
Clan: identity_guild_id 763311105434714113
Clan Tag: ﷽﷽﷽﷽
Clan Badge: dea97e909a0211e2479d75cd11c2ec41
Role: PRIMARY OPERATOR
Activity: High - Multiple attack commands across all victims
```

**Commands Executed:**
- `.tokens` - Discord token theft
- `.help` - Command reconnaissance
- `.cap` - Screenshot capture
- `.ransom` - Full system ransom lock
- `.usernamefucker` - Account takeover
- `.encryptfiles` - File encryption/ransomware

### Secondary Operator: oscaritoxx (Oscarito)
```
Discord ID: 1225098902324117685
Discord Username: oscaritoxx
Display Name: Oscarito
Global Name: Oscarito
Avatar: 8fda32111f6d9f5d4a039e5664a220be
Avatar Decoration: a_3c97a2d37f433a7913a1c7b7a735d000 (SKU: 1144308439720394944)
Clan: identity_guild_id 1366533822958534676
Clan Tag: FIVE
Clan Badge: 0bbace64a460a43475fd2453612d6b51
Role: SECONDARY OPERATOR
Activity: Moderate - Token theft attempts
```

**Commands Executed:**
- `.tokens` - Discord token theft
- Malicious commands on Victim 2

### Malware Author: Klozy / BlazeSquad666
```
Username: Klozy
Group: BlazeSquad666
Discord Contact: icracked
License Type: 1 Month
Plan: Monthly
License Expires: 2025-12-14 20:25:31
Default Password: hackedbyblazesquad2465
Bot Username: klozy
Bot ID: 1438975536327299202
Bot Discriminator: 5928
```

---

## 4. MALWARE CAPABILITIES

### Information Stealing
- Discord tokens (all browsers)
- Browser passwords, cookies, history, downloads
- Credit card information
- Cryptocurrency wallets (Metamask, Exodus, Electrum, etc.)
- System information (CPU, GPU, RAM, BIOS, MAC)
- IP geolocation
- Clipboard logging
- Keylogging

### Remote Access
- Full remote desktop via ngrok tunneling
- Command execution (CMD/PowerShell)
- File upload/download
- Screenshot capture (single + loop)
- Webcam photo/video capture
- Screen recording
- Microphone recording (real-time streaming)

### System Manipulation
- Ransomware (file encryption + system lock)
- Username/password modification
- Wallpaper changes
- Volume control
- Screen on/off control
- Taskbar hide/show
- Mouse/keyboard control
- Window manipulation

### Destructive Capabilities
- Blue Screen of Death (BSOD)
- Boot sector destruction
- System file deletion
- Storage bomber (fills disk)
- CPU killer (burns CPU)
- Disable Windows Defender
- Disable Task Manager, Control Panel, Registry Editor
- Disable Windows Update, System Restore, Safe Mode
- Block websites (antivirus, Google, YouTube)
- USB port disabling

### Persistence Mechanisms
- Startup registry key
- Scheduled task creation
- File hiding (attrib +h)
- Anti-kill process (critical process flag)
- Anti-shutdown blocker
- Discord injection (persistent token stealer)

### Anti-Analysis
- VM detection (VirtualBox, VMware, Xen)
- Debugger detection (process name blacklist)
- IP blacklist (security researchers)
- DLL/driver detection
- Registry checks
- Process termination (Task Manager, debuggers)

---

## 5. C2 INFRASTRUCTURE

### Discord C2 Server
```
Guild ID: [REDACTED}
Bot Token: [REDACTED}
Bot Name: klozy#5928
Command Prefix: .
```

**Channel Structure (Per Victim):**
- `active` - Heartbeat notifications
- `information` - System info exfiltration
- `tokens` - Discord token theft
- `startup` - Persistence confirmation
- `commands` - Command execution
- `injection` - Discord injection webhooks
- `voice` - Microphone streaming
- `screenshots` - Screenshot loop storage
- `ransom_logs` - Ransom payment tracking

### Payload Delivery Server
```
IP: 173.208.142.174
Port: 8080
Payloads:
  - /files/remotepc.zip (Remote desktop RAT with ngrok)
  - /files/libopus-0.x64.dll (Voice codec for mic streaming)
```

### GitHub Repository
```
Repository: https://github.com/BlazeSquad666/discord-injection
File: injection.js (Discord token stealer injection)
Purpose: Persistent Discord token theft via client modification
```

---

## 6. ATTACK FLOW

```
1. Initial Infection
   ├─ UAC Bypass (EventViewer exploit)
   ├─ Anti-VM/Anti-Debug checks
   ├─ Close Task Manager
   └─ Hide console window

2. System Compromise
   ├─ Disable Windows Defender
   ├─ Disable Task Manager, Control Panel, Registry
   ├─ Disable Windows Update, System Restore, Safe Mode
   ├─ Disable USB ports
   ├─ Block antivirus websites
   └─ Disable boot protection

3. Persistence Establishment
   ├─ Copy to C:\Windows\System32\Intel\
   ├─ Create scheduled task (conhost_update)
   ├─ Add registry startup key
   └─ Hide malware files

4. C2 Communication
   ├─ Connect to Discord bot
   ├─ Create victim category channels
   ├─ Exfiltrate system information
   ├─ Steal Discord tokens
   └─ Send heartbeat notifications

5. Data Exfiltration
   ├─ Browser credentials, cookies, history
   ├─ Cryptocurrency wallets
   ├─ Discord tokens
   ├─ Credit card information
   └─ System information

6. Remote Access
   ├─ Download remotepc.zip from C2
   ├─ Extract server.exe
   ├─ Launch ngrok tunnel
   └─ Send connection details to operators

7. Post-Exploitation
   ├─ Await operator commands
   ├─ Execute ransomware (optional)
   ├─ Screenshot/keylog monitoring
   └─ Maintain persistence
```

---

## 7. AFRICAN CONNECTION INVESTIGATION

### ✅ CONFIRMED: Tunisia Victim
**Evidence:**
- IP Address: 31.215.240.196 (Tunisia, North Africa)
- Username: uare
- PC: DESKTOP-0V99OKA
- Infection Date: November 16, 2025

### Investigation Tasks for Other Victims
1. **Extract IP addresses from Victim 2 & 3 information channels**
2. **Geolocate IPs to identify additional African victims**
3. **Analyze Discord token data for geographic indicators**
4. **Check browser history for African websites/services**
5. **Examine timezone data from system information**

### Potential African Indicators
- Username patterns (African names)
- Browser history (African news sites, services)
- Timezone offsets (African time zones)
- Language settings (French, Arabic, Swahili, etc.)
- Currency in browser data (African currencies)

---

## 8. DETECTION RULES

### YARA Rule
```yara
rule BlazeStealer_RAT {
    meta:
        description = "Detects BlazeStealer RAT malware"
        author = "OSINT Investigation"
        date = "2025-01-19"
        threat_level = "critical"
        
    strings:
        $discord_token = "[REDACTED}"
        $c2_server = "173.208.142.174:8080"
        $github_repo = "BlazeSquad666/discord-injection"
        $malware_path = "C:\\Windows\\System32\\Intel"
        $registry_key = "conhost.exe"
        $scheduled_task = "conhost_update"
        $default_password = "hackedbyblazesquad2465"
        $author = "Klozy"
        $group = "BlazeSquad666"
        $contact = "icracked"
  
        
    condition:
        any of them
}
```

### Snort Rule
```
alert tcp any any -> 173.208.142.174 8080 (msg:"BlazeStealer C2 Communication"; flow:to_server,established; content:"remotepc.zip"; http_uri; classtype:trojan-activity; sid:1000001; rev:1;)
alert tcp any any -> any any (msg:"BlazeStealer Discord C2"; flow:to_server,established; content:"MTQzODk3NTUzNjMyNzI5OTIwMg"; classtype:trojan-activity; sid:1000002; rev:1;)
```

### Sigma Rule
```yaml
title: BlazeStealer RAT Activity
status: experimental
description: Detects BlazeStealer RAT malware activity
references:
    - Internal OSINT Investigation
tags:
    - attack.execution
    - attack.persistence
    - attack.credential_access
logsource:
    category: process_creation
    product: windows
detection:
    selection:
        - CommandLine|contains:
            - 'C:\Windows\System32\Intel'
            - 'conhost_update'
            - 'hackedbyblazesquad2465'
            - '173.208.142.174'
    condition: selection
falsepositives:
    - None expected
level: critical
```

---

## 9. MITIGATION RECOMMENDATIONS

### Immediate Actions
1. **Block C2 Infrastructure:**
   - IP: 173.208.142.174
   - Domain: discord.com/api/* (for bot token)
   - GitHub: raw.githubusercontent.com/BlazeSquad666/*

2. **Revoke Discord Bot Token:**
   - Token: [REDACTED}
   - Report to Discord Trust & Safety

3. **Hunt for IOCs:**
   - File path: C:\Windows\System32\Intel\
   - Registry: HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Run\conhost.exe
   - Scheduled task: conhost_update
   - MAC address: f4:39:09:35:8e:09

4. **Isolate Infected Systems:**
   - Victim 1: 31.215.240.196 (Tunisia)
   - Victim 2: DESKTOP-ET51AJO
   - Victim 3: DESKTOP-0H1EJSV

### Long-term Recommendations
1. Deploy EDR solutions with behavioral detection
2. Implement application whitelisting
3. Enable Windows Defender Tamper Protection
4. Restrict PowerShell execution policies
5. Monitor Discord API usage on corporate networks
6. Educate users on social engineering tactics
7. Implement network segmentation
8. Enable Windows Event Logging (Sysmon)

---

## 10. VICTIM SUPPORT

### For Infected Users
If you believe you are infected with BlazeStealer:

1. **Disconnect from Internet immediately**
2. **Do NOT pay any ransom demands**
3. **Boot into Safe Mode**
4. **Run the desinfect command (if possible):**
   ```
   .desinfect
   ```
5. **Manually remove malware:**
   - Delete: C:\Windows\System32\Intel\
   - Remove registry key: HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Run\conhost.exe
   - Delete scheduled task: conhost_update
   - Remove: %LOCALAPPDATA%\RemotePC\

6. **Re-enable security features:**
   ```cmd
   REG delete HKCU\Software\Microsoft\Windows\CurrentVersion\Policies\System /v DisableTaskMgr /f
   REG delete "HKLM\SOFTWARE\Policies\Microsoft\Windows Defender" /v DisableAntiSpyware /f
   ```

7. **Change all passwords:**
   - Windows account password
   - Discord password (enable 2FA)
   - Browser saved passwords
   - Cryptocurrency wallet passwords

8. **Scan with multiple antivirus tools:**
   - Malwarebytes
   - Kaspersky Rescue Disk
   - ESET Online Scanner

9. **Monitor financial accounts for fraud**

10. **Report to local law enforcement**

---

## 11. LAW ENFORCEMENT CONTACT

### Threat Actor Identifiers
```
Discord IDs:
  - 1432098418930487388 (retireed_)
  - 1225098902324117685 (oscaritoxx)
  - 1438975536327299202 (klozy bot)

Discord Usernames:
  - retireed_
  - oscaritoxx
  - klozy

Contact Information:
  - Discord: icracked
  - GitHub: BlazeSquad666
  - Group: BlazeSquad666

Infrastructure:
  - C2 Server: 173.208.142.174
  - Discord Guild: 1438975480635199722
```

### Recommended Agencies
- **Tunisia:** Agence Nationale de la Sécurité Informatique (ANSI)
- **International:** INTERPOL Cybercrime Unit
- **US:** FBI Internet Crime Complaint Center (IC3)
- **EU:** Europol European Cybercrime Centre (EC3)

---

## 12. CONCLUSION

BlazeStealer RAT is a sophisticated, multi-functional malware with extensive capabilities for information theft, remote access, and system destruction. The confirmed infection of a Tunisian victim establishes a direct African connection to this threat.

**Key Findings:**
- ✅ **African Connection Confirmed:** Tunisia victim (IP: 31.215.240.196)
- 🚨 **3 Active Victims:** All with persistent infections
- 👥 **2 Active Threat Actors:** retireed_ (primary), oscaritoxx (secondary)
- 💀 **Critical Threat Level:** Ransomware, data theft, remote access, system destruction
- 🌐 **Active C2 Infrastructure:** Discord bot + payload server operational

**Immediate Priorities:**
1. Extract IP addresses from Victim 2 & 3 to identify additional African victims
2. Report Discord bot token to Discord for immediate revocation
3. Coordinate with Tunisian ANSI for victim notification
4. Monitor C2 infrastructure for additional victims
5. Track threat actors via Discord IDs and clan affiliations

---

**Report Compiled By:** OSINT Investigation Team  
**Classification:** TLP:AMBER (Limited Distribution)  
**Distribution:** Law Enforcement, Security Researchers, Affected Organizations  
**Last Updated:** 2025-01-19
