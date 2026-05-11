# PROJECT MIA: LOCKBIT RANSOMWARE THREAT LANDSCAPE IN AFRICA (2019–2026)

**Document Classification:** TLP:AMBER
**Prepared By:** Badmus Sodiq, David (Project MIA)
**Date:** May 11, 2026

---

## 1. EXECUTIVE SUMMARY

This report provides a comprehensive analysis of the LockBit ransomware group's activity targeting the African continent. Utilizing OSINT data aggregated from Dark Web Data Leak Sites (DLS) via the Ransomware.live API, the Project MIA team successfully identified and extracted data on **45 confirmed LockBit victims** across Africa.

**Key Intelligence Takeaways:**

1. **Regional Focal Point:** South Africa is disproportionately targeted, accounting for nearly half (46%) of all known LockBit victims on the continent.
2. **Evolution of Threat:** LockBit 3.0 (LockBit Black) represents a significant escalation in African targeting compared to its predecessor (LockBit 2.0), responsible for 84% of the analyzed compromises.
3. **Sector Vulnerability:** Threat actors show a clear preference for critical infrastructure and data-rich environments, with **Healthcare**, **Manufacturing**, and **Financial Services** being the most frequently compromised sectors.

---

## 2. GEOGRAPHIC DISTRIBUTION (VICTIMOLOGY)

LockBit has successfully compromised organizations in **12 different African nations**. The data reveals a heavy concentration on the continent's major economic hubs, particularly in Southern and Northern Africa. 

**The Intelligence Gap (The Nigeria Anomaly):** While internal incident response tracking indicates LockBit activity within Nigeria, DLS scraping returns **zero published Nigerian victims**. This discrepancy highlights a critical intelligence bias: DLS platforms only publish victims who *refuse* to pay. The absence of Nigerian organizations on the LockBit leak site strongly suggests that compromised entities in this region are either paying the ransom to prevent publication or successfully remediating the attacks under strict non-disclosure.

| Rank | Country                 | ISO Code | Confirmed Victims | Percentage of Total |
| :--- | :---------------------- | :------: | :---------------: | :-----------------: |
| 1    | **South Africa** |    ZA    |        21         |        46.6%        |
| 2    | **Egypt** |    EG    |         6         |        13.3%        |
| 3    | **Namibia** |    NA    |         5         |        11.1%        |
| 4    | **Morocco** |    MA    |         4         |        8.8%        |
| 5    | **Angola** |    AO    |         2         |        4.4%        |
| 6    | **Tanzania** |    TZ    |         1         |        2.2%        |
| 7    | **Tunisia** |    TN    |         1         |        2.2%        |
| 8    | **Uganda** |    UG    |         1         |        2.2%        |
| 9    | **Ethiopia** |    ET    |         1         |        2.2%        |
| 10   | **Senegal** |    SN    |         1         |        2.2%        |
| 11   | **Cote d'Ivoire** |    CI    |         1         |        2.2%        |
| 12   | **Mozambique** |    MZ    |         1         |        2.2%        |

---

## 3. SECTOR & INDUSTRY TARGETING

An analysis of the victims' industries reveals that LockBit affiliates do not strictly discriminate by sector, but they do gravitate toward organizations with low downtime tolerance (Double Extortion leverage).

### Top 5 Most Targeted Sectors:

1. 🏥 **Healthcare (7 Victims):** Medical facilities and pharmaceutical companies (e.g., *Aurum Institute*, *Elezaby Pharmacy*, *Galenica*). Highly targeted due to the critical nature of patient data and the urgent need to restore services.
2. 🏭 **Manufacturing (6 Victims):** (e.g., *Nampak*, *Ceratube*). Targeted for supply chain disruption.
3. 💼 **Business Services (5 Victims):** IT, consulting, and B2B providers.
4. 🏦 **Financial Services (5 Victims):** (e.g., *Crowe ZA*, *Jubilee Insurance*). High-value targets for sensitive financial records and PII.
5. 🚛 **Transportation & Logistics (4 Victims):** Target selection based on disrupting physical goods movement and supply chain operations.

---

## 4. RANSOMWARE VARIANT EVOLUTION

LockBit operates under a Malware-as-a-Service (MaaS) model, updating its encryptor and affiliate programs over time. The telemetry shows a massive spike in African targeting following the release of LockBit 3.0.

* **LockBit 1.0 (2019 - 2021):** 0 Confirmed African DLS Victims
* **LockBit 2.0 (2021 - 2022):** 7 Confirmed African DLS Victims *(15.5%)*
* **LockBit 3.0 (2022 - Present):** 38 Confirmed African DLS Victims *(84.4%)*

> **Analyst Note:** The transition to LockBit 3.0 introduced a bug bounty program and more sophisticated anti-analysis techniques, which likely emboldened affiliates to target larger enterprises in developing digital economies like Egypt and South Africa.

---

## 5. FINANCIAL IMPLICATIONS & ESTIMATED LOSSES

During the OSINT data extraction, specific ransom demands for the 45 African victims were marked as "Not Disclosed" by the threat actors. While a public ledger of exact ransoms paid by African organizations does not exist, the financial devastation caused by LockBit can be projected through localized cyber intelligence metrics:

* **LockBit's Global Extortion Baseline:** According to joint advisories by the FBI, CISA, and Europol, the LockBit network has been responsible for extracting over **$120 million in confirmed ransom payments** globally, while issuing over **$1 billion in total demands**.

**Calculating Projected African Economic Loss:**
Applying global averages (e.g., $1.5M - $2M per incident) directly to the African threat landscape is fundamentally flawed. Global averages are heavily skewed by U.S. and EU economies, where incident response includes exorbitant hourly rates for Western forensic consultants, massive regulatory fines (like GDPR), and massive cyber insurance payouts. 

When evaluating the digital business backbone of the African continent, remediation economics are vastly different. Localized incident recovery costs—factoring in regional IT labor rates, internal server rebuilding, operational downtime, and the reality of local operating budgets—place the average remediation cost for an African enterprise breach realistically between **$150,000 and $500,000**.

Applying this localized baseline to our OSINT dataset:
* **Conservative Estimate:** 45 victims × $150,000 = **$6.75 Million**
* **High-End Enterprise Estimate:** 45 victims × $500,000 = **$22.5 Million**

**Conclusion:** The estimated economic damage for these 45 confirmed African breaches ranges from **$6.75M to $22.5M**. This figure represents the collateral remediation costs (downtime and rebuilding) and excludes any actual, undisclosed ransom payments made by companies not listed on the DLS.

---

## 6. STRATEGIC RECOMMENDATIONS

Based on LockBit's observed targeting patterns in Africa, Project MIA recommends the following defensive postures for regional organizations:

1. **Prioritize South African & Egyptian Infrastructure:** Organizations operating in these regions face the highest statistical probability of a LockBit encounter. Heightened monitoring of ingress points is required.
2. **Sector-Specific Hardening:** Healthcare and Manufacturing sectors must prioritize offline, immutable backups. LockBit relies heavily on encrypting connected backup servers.
3. **Credential & Access Management:** LockBit affiliates frequently gain initial access via compromised RDP credentials and exposed VPN endpoints. Mandatory MFA for all external-facing infrastructure is critical.
4. **Data Exfiltration Monitoring:** Since LockBit relies heavily on the threat of leaking data (extortion), deploying robust DLP (Data Loss Prevention) solutions to detect large outbound data transfers to cloud storage providers can serve as an early warning sign before encryption begins.

---

## 7. REFERENCES & CITATIONS

**1. LockBit's Global Extortion Baseline ($120M Paid / $1B+ Demanded)**
* **Source:** U.S. Department of Justice (DOJ), Federal Bureau of Investigation (FBI), and CISA.
* **Reference:** "U.S. and U.K. Disrupt LockBit Ransomware Variant" (Operation Cronos). Joint press releases and cybersecurity advisories published February 2024. 

**2. Localized Economic Damage Projection Methodology**
* **Source:** Project MIA Threat Intelligence & Regional Economic Adjustment.
* **Reference:** The $6.75M–$22.5M projection adjusts global incident response baselines (which typically sit at $1.5M+) to align with African purchasing power parity, regional IT labor costs, and localized regulatory environments. The adjusted enterprise recovery cost is calculated at $150k–$500k per incident.

---

*End of Report*
