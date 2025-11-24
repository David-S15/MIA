Forensic Report Template (DFIR-style) — filename:
YYYYMMDD_Forensic_Report_<caseid>_DFIR.pdf (or .md)
Template (full, use this exactly):
# Forensic Report — Case <case-id>

**Prepared for:** DigitalFootprints  
**Prepared by:** Tekena (Digital Forensic Investigator)  
**Date:** YYYY-MM-DD

---

## 1. Executive Summary
- Short description of incident/simulation (2–3 lines)
- High-level findings
- Immediate recommendations (2–3 bullets)

## 2. Scope & Objectives
- Scope: systems examined (VM image, memory dump)
- Objective: identify persistence, data theft, timeline reconstruction

## 3. Evidence Acquisition
- Evidence ID: <EVID-xxxx>
- Acquisition date/time: YYYY-MM-DD HH:MM
- Acquisition tool(s): FTK Imager vX, DumpIt.exe vX
- Acquisition method: e.g., "Memory captured using DumpIt.exe on VM snapshot id xyz"
- Evidence storage location: (company encrypted path — do NOT publish)

## 4. Tools Used (analysis)
- Volatility 3 (commands run), Autopsy (modules), Strings, etc.

## 5. Systems Examined
- Hostname / VM name: <name>
- OS and version: e.g., Windows 10 19041
- Snapshot ID: <snapshot>
- Notes (e.g., "sandboxed, host-only network")

## 6. Findings (detailed)
- Finding 1: short title
  - Description: full detail
  - Evidence: file path, offsets, registry keys, timestamps
- Finding 2: ...

(Each finding should include: Description, Evidence reference, Timestamp(s), Confidence)

## 7. Timeline of Activity
- YYYY-MM-DD HH:MM: Event — evidence reference
- e.g., 2025-11-05 14:22 — process dropper.exe created C:\Users\...\temp\payload.exe (file hash: <sha256>)

## 8. Artifacts & IOCs (table)
| Artifact | Type | Location | Notes |
|----------|------|----------|-------|
| <filename> | file | C:\... | sha256: <hash> |

Append a separate attachment with IOCs in CSV (see IOC CSV format below).

## 9. Correlation with Malware Analysis
- Reference Malware Analyst report: `Malware_Analysis/Deep_Reports/YYYYMMDD_deep_<name>.md`
- Briefly state how forensic artifacts confirm the malware behavior (persistence, process injection, etc.)

## 10. Recommended Actions
- Containment steps (immediate)  
- Eradication steps  
- Evidence preservation guidance  
- Hunting queries (for EDR / logs) — short sigma/shell examples if available

## 11. Conclusion
- Summary paragraph and confidence level

## 12. Appendix
- Evidence manifest (list of evidence items with hashes)
- Commands run and their outputs (short)
- Volatility command outputs (attach as text files)
- References (Any.run link, VT link, OSINT references)

**Report Sign-off**
- Analyst signature (name, date)
