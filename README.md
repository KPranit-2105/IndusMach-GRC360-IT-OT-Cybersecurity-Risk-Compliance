# IndusMach Industries Ltd. — Enterprise IT/OT Cybersecurity GRC & Technology Risk Management Project

> **DISCLAIMER & PORTFOLIO NOTICE**  
> *This repository is a fully populated, simulated enterprise Cybersecurity GRC (Governance, Risk, and Compliance) & Technology Risk Management case study designed for portfolio presentation. All company profiles, factory operational data, asset inventories, risk registers, vulnerability datasets, and audit scenarios represent an internally consistent, realistic industrial manufacturing enterprise model.*

---

## 1. Executive Summary & Project Overview

**IndusMach Industries Ltd.** is a simulated $1.4B heavy industrial manufacturing enterprise operating six production facilities across India with **8,000 employees**, 48 automated production lines, and an integrated IT/OT (Information Technology / Operational Technology) landscape following the **Purdue Model (Levels 0–5)**.

Prior to establishing this formal GRC program, IndusMach faced a classic industrial challenge: **The conflict between technical security recommendations and production operational continuity.** Security teams demanded immediate patching of critical vulnerabilities on legacy operating systems, while factory plant managers resisted patches due to unannounced downtime costs ($50,000–$150,000/hour per production line) or fear of breaking unvalidated machine control interfaces.

### Core Learning & GRC Principle
$$\text{Technical Vulnerability} \longrightarrow \text{Business Impact Analysis} \longrightarrow \text{Risk Assessment} \longrightarrow \text{Compensating Controls} \longrightarrow \text{Formal Risk Acceptance} \longrightarrow \text{Monitoring} \longrightarrow \text{Scheduled Overhaul Patching}$$

This project demonstrates how a **Senior Cybersecurity GRC Analyst** acts as a strategic risk facilitator between Security, Plant Operations, EHS (Safety), Finance, and Executive Leadership.

---

## 2. Key Repository Metrics & Structure

| Element / Dataset | Total Quantity / Scope | Key Deliverables & Artifacts |
| :--- | :--- | :--- |
| **Manufacturing Plants** | **6 Plants** | Pune, Nagpur, Chennai, Bengaluru, Ahmedabad, Hyderabad (`Factory_Inventory.xlsx`) |
| **IT & OT Asset Inventory** | **250 Assets** | 125 IT Assets + 125 OT Assets across Purdue Levels 0-5 (`IT_OT_Asset_Inventory.xlsx`) |
| **IT/OT Risk Register** | **40 Risks** | 20 IT Risks + 20 OT Risks with Inherent vs Residual 5x5 Formulas (`IT_OT_Risk_Register.xlsx`) |
| **Vulnerability Register** | **100 Vulnerabilities** | Risk-based prioritization, CVSS vs Production/Safety Impact (`Vulnerability_Register.xlsx`) |
| **Cybersecurity Controls** | **100 Controls** | 100 Controls across 21 GRC Domains, 75 Evaluated Assessments (`IT_OT_Control_Library.xlsx`) |
| **Access & Remote Access** | **75 Records** | 50 Privileged Accounts Reviewed + 25 Vendor Remote Access Records (`Privileged_Access_Review.xlsx`) |
| **Internal Audit Findings** | **30 Findings** | 30 Audit Findings, Recommendations & Management Responses (`Audit_Findings.xlsx`) |
| **Security Exceptions** | **30 Exceptions** | 30 Formal Security Exceptions with Compensating Controls (`Security_Exception_Register.xlsx`) |
| **Compliance Mappings** | **5 Frameworks** | ISO 27001:2022, NIST CSF 2.0, NIST SP 800-82 Rev 3, IEC 62443, Gap Analysis (`15_Compliance/`) |
| **Dashboards & KRIs** | **4 Dashboards** | Executive GRC, 6-Factory Profile, 5x5 Heatmap, 30 KPIs/KRIs (`16_Dashboard/`) |
| **Interview Preparation** | **100 Q&As / 10 STAR** | 30s-5m pitches, 100 Interview Q&As, 10 Behavioral STAR Stories (`18_Interview_Preparation/`) |

---

## 3. Directory Layout

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
└── 18_Interview_Preparation/                  [Pitches, Flagship Legacy Case, 100 Q&As, 10 STAR]
```

---

## 4. Flagship Case Study Summary: Legacy Gear Shaping CNC Machine

- **Asset**: `AST-OT-004` (Gear Shaping CNC Machine on Powertrain Line A in Pune Plant).
- **Technical Issue**: Critical Remote Code Execution vulnerability (**CVE-2017-0144 EternalBlue / MS17-010**) on unsupported **Windows 7 Embedded** OS.
- **Conflict**: Security team demanded immediate patch/upgrade. Operations proved an immediate shutdown would stop Line A for 3 weeks, costing **$1.2 Million in downtime** and OEM contract delivery penalties.
- **GRC Solution**: Formulated **Option C (Compensating Controls)** under **Risk Acceptance RA-2026-001**:
  1. Micro-segmentation via FortiGate Industrial DMZ Firewall (Purdue Zone 3.5).
  2. Physical and software USB port lockdown (`CMP-001`).
  3. Disabling SMBv1 on perimeter routers and isolating SCADA communications via read-only OT Historian relay.
  4. 24/7 SIEM anomaly monitoring via Nozomi Networks OT sensor.
  5. Deferred full system upgrade to the **Q4 Annual Overhaul Window** (November 2026).

---

## 5. ServiceNow GRC Implementation Architecture

This program is designed for seamless mapping into **ServiceNow GRC / IRM**:
- **Risks** $ightarrow$ `sn_risk_risk` (Formula-driven scoring: Likelihood $	imes$ Impact).
- **Controls** $ightarrow$ `sn_compliance_control` & `sn_compliance_policy`.
- **Vulnerabilities** $ightarrow$ `sn_vulnerable_item` & `sn_vul_entry`.
- **Audit Findings** $ightarrow$ `sn_grc_issue`.
- **Remediations** $ightarrow$ `sn_grc_task`.
- **Vendor Access** $ightarrow$ `sn_vdr_risk_asmt_vendor_risk_item`.

---

## 6. How to Use This Project for Portfolio Review

1. **Review Executive Summaries**: Inspect `01_Company_Profile/Company_Profile.md` and `16_Dashboard/Executive_GRC_Dashboard.xlsx`.
2. **Examine Risk & Control Logic**: Open `04_Risk_Management/IT_OT_Risk_Register.xlsx` to review formula-driven 5x5 scoring and Inherent vs Residual calculations.
3. **Deep-Dive Flagship Scenario**: Read `18_Interview_Preparation/Legacy_System_Case.md` for full BIA, Security Analysis, Patch Decision, and Risk Acceptance documentation.
4. **Prepare for Technical Interviews**: Reference `18_Interview_Preparation/Interview_Questions.md` (100 Q&As) and `STAR_Stories.md` (10 Behavioral Scenarios).
