# MISP Event Request — <shortname>
**Author:** Badmus  
**Date:** YYYY-MM-DD
**Title:** <Event title>
**Description:** Short 2–3 line summary
**Distribution:** Your organization only
**Threat level:** [Low/Medium/High]
**Analysis level:** [0/1/2]

## Attributes to add (paste rows)
indicator,type,category,comment
sha256:<hash>,sha256,Payload,"sample from Any.run, VT detections X"
c2.example[.]com,domain,Network activity,"C2 observed in sandbox run"

## MITRE ATT&CK techniques (TIDs + short justification)
- T1003 – Credential Dumping — sample dumps LSASS memory during runtime
- T1060 – Registry Run Keys — creates HKCU run key

## References
- Sandbox: <any.run link>
- OSINT lead: <path to OSINT MD>
- Forensic appendix: <path to DFIR md>

## Confidence
Medium
