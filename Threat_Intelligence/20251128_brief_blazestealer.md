# Intel Brief — BlazeStealer RAT (BlazeSquad Malware)

**Date:** 2025-11-28
**Author:** Badmus Sodiq

## Summary

BlazeStealer RAT is a sophisticated Python-based remote access trojan with extensive data theft, ransomware, and system destruction capabilities. The malware uses Discord as C2 infrastructure and has confirmed victims in Tunisia (North Africa), establishing a direct African connection. Two active threat actors (retireed_ and oscaritoxx) are operating the malware with capabilities including cryptocurrency wallet theft, browser credential harvesting, and full remote desktop access.

## Key Findings

• **African Connection Confirmed:** Tunisia victim (IP: 31.215.240.196, MAC: f4:39:09:35:8e:09) with active infection since November 2025
• **Multi-Stage UAC Bypass:** Exploits EventViewer vulnerability (CVE-2017-0213) using malicious XAML payload for privilege escalation
• **Discord C2 Infrastructure:** Uses bot token MTQzODk7NTUzNjMyNzI5OTIwMg.GHmGBc.3RvtEDvgQCsmm1YYbpaoXogAv0GrLnFnDJh_UY for command and control
• **Cryptocurrency Focus:** Targets 10+ wallet types including MetaMask, Exodus, Electrum with browser extension hijacking
• **Advanced Anti-Analysis:** VM detection, debugger evasion, IP blacklisting (19 security researcher IPs), and process termination
• **Destructive Capabilities:** Ransomware encryption, BSOD triggers, boot sector destruction, and system recovery disabling

## Top IOCs

**sha256:** 61a3e046d45038e2ec22791c8cf62e69e176fcb91f2d4c44fa03fe90367bc523
**domain:** discord[.]com, raw.githubusercontent[.]com
**ip:** 173.208.142.174
**c2_token:** MTQzODk3NTUzNjMyNzI5OTIwMg.GHmGBc.3RvtEDvgQCsmm1YYbpaoXogAv0GrLnFnDJh_UY
**file_path:** C:\Windows\System32\Intel
**registry:** HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Run\conhost.exe
**scheduled_task:** conhost_update
**github_repo:** BlazeSquad666/discord-injection

## MITRE ATT&CK Mapping

**T1548.002** – Bypass User Account Control (EventViewer exploit)
**T1555.003** – Credentials from Web Browsers (Chrome, Edge, Brave, Opera)
**T1005** – Data from Local System (Cryptocurrency wallets)
**T1102.002** – Web Service C2 (Discord bot communication)
**T1486** – Data Encrypted for Impact (Ransomware functionality)
**T1497.001** – Virtualization/Sandbox Evasion (VM detection)
**T1562.001** – Impair Defenses (Disable Windows Defender)
**T1547.001** – Boot/Logon Autostart (Registry Run keys, Scheduled tasks)
**T1113** – Screen Capture (Screenshot loops)
**T1056.001** – Input Capture (Keylogging)

## Impact / Targeting

**Region:** Tunisia (North Africa) - Confirmed victim
**Sector:** Individual users, cryptocurrency holders
**Threat Level:** CRITICAL - Active infections with persistent access
**Victim Count:** 3 confirmed active victims
**Data at Risk:** Discord tokens, browser credentials, cryptocurrency wallets, personal files

## Recommended Actions

• **Block C2 infrastructure:** 173.208.142.174, Discord bot token revocation
• **Hunt for persistence:** Search for HKCU Run key "conhost.exe" and scheduled task "conhost_update"
• **Monitor file paths:** C:\Windows\System32\Intel\ directory creation
• **Network monitoring:** Discord API traffic with suspicious bot tokens
• **Wallet security:** Advise cryptocurrency users to check wallet integrity
• **Coordinate with Tunisia ANSI:** Victim notification and incident response

## YARA Detection Rule

```yara
rule BlazeStealer_RAT {
    meta:
        description = "Detects BlazeStealer RAT malware"
        author = "Badmus"
        date = "2025-01-19"
        threat_level = "critical"
      
    strings:
        $discord_token = "MTQzODk3NTUzNjMyNzI5OTIwMg.GHmGBc.3RvtEDvgQCsmm1YYbpaoXogAv0GrLnFnDJh_UY"
        $c2_server = "173.208.142.174:8080"
        $malware_path = "C:\\Windows\\System32\\Intel"
        $registry_key = "conhost.exe"
        $scheduled_task = "conhost_update"
        $author = "BlazeSquad666"
        $uac_bypass = "eventvwr.exe"
        $payload_file = "C:\\Windows\\Tasks\\p4yl0ad"
      
    condition:
        any of them
}
```
