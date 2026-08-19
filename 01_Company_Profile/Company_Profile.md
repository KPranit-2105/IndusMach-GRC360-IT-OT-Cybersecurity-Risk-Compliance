# Company Profile & Architecture Overview — IndusMach Industries Ltd.

> **DISCLAIMER & PORTFOLIO NOTICE**  
> *This document is part of a simulated Cybersecurity GRC & Technology Risk Management case study created for portfolio demonstration purposes. All company details, factory names, architecture diagrams, datasets, and scenarios are fictional models of a large industrial manufacturing enterprise.*

---

## 1. Executive Summary

**IndusMach Industries Ltd.** is a leading multi-facility heavy industrial and discrete manufacturing conglomerate operating six major production facilities across India. With over **8,000 employees**, 48 active production lines, and an annual production volume supporting automotive, aerospace, heavy machinery, and industrial automation sectors, IndusMach relies heavily on tightly integrated Corporate IT and Industrial Operational Technology (OT) infrastructure.

---

## 2. Organization Snapshot

| Attribute | Details |
| :--- | :--- |
| **Company Name** | IndusMach Industries Ltd. |
| **Industry Sector** | Discrete & Process Manufacturing (Automotive, Heavy Machinery, Precision Automation) |
| **Total Workforce** | ~8,000 Direct Employees & ~2,500 Dedicated Third-Party Contractors |
| **Manufacturing Plants** | 6 Plants (Pune, Nagpur, Chennai, Bengaluru, Ahmedabad, Hyderabad) |
| **Active Production Lines**| 48 Automated Lines |
| **Annual Revenue** | ~$1.4 Billion USD (Simulated) |
| **IT/OT Footprint** | Corporate Cloud, Hybrid Data Center, Purdue Level 0–5 Architecture |
| **Primary GRC Mandate** | Centralize IT/OT Risk, Align Security with Production Continuity, Establish Governance Framework |

---

## 3. Factory Inventory Summary

IndusMach operates six geographically distributed manufacturing plants, each with distinct production lines, technology dependencies, and risk postures:

| Factory ID | Factory Name | Location | Primary Business Function / Product | Lines | Critical OT Systems | Risk Rating |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| `FAC-PUN` | **Pune Advanced Manufacturing Plant** | Pune, Maharashtra | Automotive Powertrain & Gearboxes | 10 | Allen-Bradley GuardLogix PLCs, Siemens WinCC HMIs, Gear Shaping CNCs | **CRITICAL** |
| `FAC-NAG` | **Nagpur Industrial Components Plant** | Nagpur, Maharashtra | Stamping & Structural Forging | 8 | Mitsubishi MELSEC PLCs, Wonderware System Platform, Hydraulic Press HMIs | **HIGH** |
| `FAC-CHE` | **Chennai Heavy Engineering Plant** | Chennai, Tamil Nadu | Heavy Industrial Machinery & Engines | 8 | Siemens S7-1500 PLCs, WinCC SCADA, Welding Robot Controllers | **CRITICAL** |
| `FAC-BLR` | **Bengaluru Precision Systems Plant** | Bengaluru, Karnataka | High-Precision Sensors & Robotics | 6 | Beckhoff TwinCAT PLCs, Ignition SCADA, Vision Inspection Sensors | **MEDIUM** |
| `FAC-AMD` | **Ahmedabad Automotive Components Plant**| Ahmedabad, Gujarat | Chassis & Body-in-White Assembly | 9 | Omron NJ Series PLCs, Rockwell FactoryTalk View, Spot Welding HMIs | **HIGH** |
| `FAC-HYD` | **Hyderabad Industrial Automation Plant**| Hyderabad, Telangana | Industrial Motors & Motion Drives | 7 | Schneider Modicon M580 PLCs, Citect SCADA, CNC Lathes | **HIGH** |

---

## 4. IT/OT Technology Landscape & Purdue Model Architecture

IndusMach's architecture follows the **Purdue Model for Industrial Control Systems (IEC 62443 / NIST SP 800-82)**:

```
                      +------------------------------------------+
                      |         ENTERPRISE CLOUD & INTERNET       |
                      +------------------------------------------+
                                           |
                                [ Perimeter Firewall ]
                                           |
Level 5 / Level 4:    +------------------------------------------+
Corporate Enterprise   |  Enterprise IT & Active Directory        |
                      |  ERP (SAP S/4HANA), O365, Data Center    |
                      +------------------------------------------+
                                           |
                                [ Enterprise Firewall ]
                                           |
Level 3.5:            +------------------------------------------+
Industrial DMZ        |  Industrial DMZ (IDMZ)                   |
                      |  Jump Hosts, OT Historian Relays, MFA    |
                      +------------------------------------------+
                                           |
                                  [ OT IDMZ Firewall ]
                                           |
Level 3:              +------------------------------------------+
Operations Management |  Site Operations & Manufacturing Execution|
                      |  MES Servers, Site Historian, EWS        |
                      +------------------------------------------+
                                           |
Level 2:              +------------------------------------------+
Control Systems       |  SCADA & Supervisory Control             |
                      |  WinCC / Ignition SCADA, Factory HMIs    |
                      +------------------------------------------+
                                           |
Level 1:              +------------------------------------------+
Direct Process Control|  Programmable Logic Controllers (PLCs)   |
                      |  Allen-Bradley, Siemens S7, Safety Relays|
                      +------------------------------------------+
                                           |
Level 0:              +------------------------------------------+
Physical Equipment    |  Robots, CNC Machines, Sensors, Actuators|
                      +------------------------------------------+
```

---

## 5. Core Business Problem & GRC Mandate

### The Challenge
Prior to the GRC transformation, IndusMach faced significant alignment gaps between the **Corporate Cybersecurity Team** and **Factory Operations Teams**:
- Security teams issued urgent patch directives (e.g., immediate patching of legacy Windows 7 Embedded workstations controlling CNC machines).
- Plant managers resisted patches due to fear of unannounced production downtime ($50,000–$150,000 per hour of unplanned stoppage per line) or unvalidated software breaking legacy machine interfaces.
- Third-party vendors maintained unmonitored, persistent VPN connections directly into plant PLCs without MFA or session recording.

### The Solution: The GRC Facilitation Model
The Cybersecurity GRC Program bridges **Security, IT, OT Operations, Safety, Compliance, and Finance**. Rather than enforcing raw technical security metrics, GRC evaluates:
$$\text{Cyber Risk Decision} = \text{Threat} \times \text{Vulnerability} \times \text{Asset Criticality} \times \text{Business Impact} \times \text{Safety Impact} - \text{Compensating Controls}$$

This framework enables risk-informed decision-making, formal temporary risk acceptances, robust compensating controls (such as micro-segmentation and virtual patching), and scheduled remediation during annual plant overhaul windows.
