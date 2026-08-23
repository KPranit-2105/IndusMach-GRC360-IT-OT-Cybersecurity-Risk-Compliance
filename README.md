<div align="center">

# 🏭 IndusMach Industries Ltd. — Enterprise IT/OT Cybersecurity GRC

**Purdue Model Architecture · Legacy System Risk · Technology Risk Management**

![Company](https://img.shields.io/badge/Company-IndusMach%20Industries%20Ltd.-1B2A4A.svg)
![Industry](https://img.shields.io/badge/Industry-Heavy%20Industrial%20Manufacturing-2E7D32.svg)
![Frameworks](https://img.shields.io/badge/Compliance-ISO%2027001%20%7C%20NIST%20CSF%20%7C%20NIST%20800--82%20%7C%20IEC%2062443-FF9900.svg)
![Status](https://img.shields.io/badge/Type-Simulated%20Portfolio%20Case%20Study-6A1B9A.svg)

> **Disclaimer & Portfolio Notice:** This repository is a fully populated, simulated enterprise Cybersecurity GRC & Technology Risk Management case study, designed for portfolio presentation. All company profiles, factory operational data, asset inventories, risk registers, vulnerability datasets, and audit scenarios represent an internally consistent, realistic industrial manufacturing enterprise model.

</div>

---

## 1. Executive Summary & Project Overview

**IndusMach Industries Ltd.** is a simulated **$1.4B heavy industrial manufacturing enterprise** operating **six production facilities** across India with **8,000 employees**, 48 automated production lines, and an integrated IT/OT landscape following the **Purdue Model (Levels 0–5)**.

Before this formal GRC program existed, IndusMach faced a classic industrial conflict: **security recommendations vs. production continuity.** Security teams demanded immediate patching of critical vulnerabilities on legacy operating systems; plant managers resisted, fearing unannounced downtime costing **$50,000–$150,000/hour per production line**, or breaking unvalidated machine control interfaces.

### Core GRC Principle

<p align="center">
  <img src="assets_indusmach/grc_principle.svg" alt="Core GRC Principle Flow — Vulnerability to Resolution" width="1000">
</p>

This project demonstrates how a **Senior Cybersecurity GRC Analyst** acts as a strategic risk facilitator between Security, Plant Operations, EHS (Safety), Finance, and Executive Leadership — turning an impasse into a documented, monitored, time-bound decision.

---

## 2. IT/OT Architecture — The Purdue Model

Every asset, risk, and control in this program is scoped against the industry-standard Purdue Model, so segmentation decisions (like the Industrial DMZ used in the flagship case below) have a clear architectural basis.

<p align="center">
  <img src="assets_indusmach/purdue_model.svg" alt="Purdue Model IT/OT Architecture Levels 0-5" width="700">
</p>

---

## 3. Key Repository Metrics

<p align="center">
  <img src="assets_indusmach/program_scale.svg" alt="IndusMach GRC Program Scale Overview" width="950">
</p>

| Element / Dataset | Total Quantity / Scope | Key Deliverables & Artifacts |
|---|---|---|
| **Manufacturing Plants** | 6 Plants | Pune, Nagpur, Chennai, Bengaluru, Ahmedabad, Hyderabad (`Factory_Inventory.xlsx`) |
| **IT & OT Asset Inventory** | 250 Assets | 125 IT + 125 OT assets across Purdue Levels 0–5 (`IT_OT_Asset_Inventory.xlsx`) |
| **IT/OT Risk Register** | 40 Risks | 20 IT + 20 OT risks, Inherent vs. Residual 5×5 formulas (`IT_OT_Risk_Register.xlsx`) |
| **Vulnerability Register** | 100 Vulnerabilities | Risk-based prioritization, CVSS vs. Production/Safety Impact (`Vulnerability_Register.xlsx`) |
| **Cybersecurity Controls** | 100 Controls | 100 controls across 21 GRC domains, 75 evaluated (`IT_OT_Control_Library.xlsx`) |
| **Access & Remote Access** | 75 Records | 50 privileged accounts + 25 vendor remote access records (`Privileged_Access_Review.xlsx`) |
| **Internal Audit Findings** | 30 Findings | Findings, recommendations & management responses (`Audit_Findings.xlsx`) |
| **Security Exceptions** | 30 Exceptions | Formal exceptions with compensating controls (`Security_Exception_Register.xlsx`) |
| **Compliance Mappings** | 5 Frameworks | ISO 27001:2022, NIST CSF 2.0, NIST SP 800-82 Rev 3, IEC 62443, Gap Analysis (`15_Compliance/`) |
| **Dashboards & KRIs** | 4 Dashboards | Executive GRC, 6-Factory Profile, 5×5 Heatmap, 30 KPIs/KRIs (`16_Dashboard/`) |
| **Interview Preparation** | 100 Q&As / 10 STAR | 30s–5m pitches, Q&As, behavioral stories (`18_Interview_Preparation/`) |

---

## 4. Directory Layout

```
IndusMach-IT-OT-GRC-Project/
├── README.md                                  [Master Recruiter Guide]
├── 01_Company_Profile/Company_Profile.md      [Enterprise & Purdue Level 0-5 Architecture]
├── 02_Factory_Management/                     [Factory Inventories & Comparative Risk Profiles]
├── 03_Asset_Management/                       [250 IT/OT Assets, Multi-Criteria Criticality Model]
├── 04_Risk_Management/                        [40 Risks, Inherent vs Residual 5x5 Scoring Formulas]
├── 05_Vulnerability_Management/               [100 Vulnerabilities, Patch Schedules & Exceptions]
├── 06_Control_Management/                     [100 Controls across 21 Domains, 75 Assessed Controls]
├── 07_Access_Management/                      [50 Privileged Accounts, 25 Vendor Remote Access Logs]
├── 08_Network_Security/                       [OT Purdue Level Segmentation Review & Firewall Risks]
├── 09_Vendor_Risk/                            [15 Critical OT Vendors, Risk Posture Evaluations]
├── 10_Incident_Management/                    [10 Simulated Incidents, Ransomware Tabletop, CAPA]
├── 11_BCP_DR/                                 [10 Process BIAs, RTO/RPO, 7 DR Scenario Tests]
├── 12_Exception_Management/                   [30 Security Exceptions & Deferral Approvals]
├── 13_Change_Management/                      [20 IT/OT Maintenance & CAB Change Requests]
├── 14_Audit/                                  [30 Internal Audit Findings & Retest Actions]
├── 15_Compliance/                             [ISO 27001, NIST CSF, NIST 800-82, IEC 62443 Mappings]
├── 16_Dashboard/                              [Executive GRC, Factory Comparative, 5x5 Heatmaps, KRIs]
├── 17_Documentation/                          [Operating Models, Risk & Vulnerability Methodologies]

```

---

## 5. Flagship Case Study — Legacy Gear Shaping CNC Machine

<p align="center">
  <img src="assets_indusmach/cnc_case_flow.svg" alt="Flagship Case Study Flow — Legacy CNC Machine Risk Decision" width="1000">
</p>

| | |
|---|---|
| **Asset** | `AST-OT-004` — Gear Shaping CNC Machine, Powertrain Line A, Pune Plant |
| **Technical Issue** | Critical Remote Code Execution vulnerability (**CVE-2017-0144 / EternalBlue / MS17-010**) on unsupported **Windows 7 Embedded** |
| **Conflict** | Security demanded immediate patch/upgrade. Operations demonstrated an immediate shutdown would halt Line A for **3 weeks**, costing **$1.2M in downtime** plus OEM contract delivery penalties |
| **GRC Solution** | **Option C — Compensating Controls** under **Risk Acceptance RA-2026-001** |

**Compensating controls enforced:**
1. Micro-segmentation via FortiGate Industrial DMZ Firewall (Purdue Zone 3.5)
2. Physical and software USB port lockdown (`CMP-001`)
3. SMBv1 disabled on perimeter routers; SCADA isolated via read-only OT Historian relay
4. 24/7 SIEM anomaly monitoring via Nozomi Networks OT sensor
5. Full system upgrade deferred to the **Q4 Annual Overhaul Window (November 2026)**

> This is the case that shows the actual job: not "patch everything" or "ignore the risk," but a documented, monitored, time-bound decision that both security and operations could sign off on.

---

## 6. ServiceNow GRC Implementation Architecture

This program is designed for seamless mapping into ServiceNow GRC / IRM.

<p align="center">
  <img src="assets_indusmach/servicenow_mapping.svg" alt="ServiceNow GRC IRM Implementation Architecture" width="750">
</p>

| GRC Concept | ServiceNow Table |
|---|---|
| Risks | `sn_risk_risk` (formula-driven scoring: Likelihood × Impact) |
| Controls | `sn_compliance_control`, `sn_compliance_policy` |
| Vulnerabilities | `sn_vulnerable_item`, `sn_vul_entry` |
| Audit Findings | `sn_grc_issue` |
| Remediations | `sn_grc_task` |
| Vendor Access | `sn_vdr_risk_asmt_vendor_risk_item` |

---

## 7. How to Use This Project for Portfolio Review

1. **Review Executive Summaries** — `01_Company_Profile/Company_Profile.md` and `16_Dashboard/Executive_GRC_Dashboard.xlsx`
2. **Examine Risk & Control Logic** — `04_Risk_Management/IT_OT_Risk_Register.xlsx` for formula-driven 5×5 scoring and Inherent vs. Residual calculations
3. **Deep-Dive the Flagship Scenario** — `18_Interview_Preparation/Legacy_System_Case.md` for the full BIA, security analysis, patch decision, and risk acceptance documentation
4. **Prepare for Technical Interviews** — `18_Interview_Preparation/Interview_Questions.md` (100 Q&As) and `STAR_Stories.md` (10 behavioral scenarios)

---

<div align="center">

**Security doesn't win by demanding a patch. It wins by making the risk visible, time-bound, and monitored** — this project shows that discipline applied to a real $1.2M production conflict.

</div>
