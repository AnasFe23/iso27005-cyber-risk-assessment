# 🛡️ Enterprise Cyber Risk Assessment & Management (ISO/IEC 27005 & 27002)

[![Standard](https://img.shields.io/badge/Standard-ISO%2FIEC%2027005-blue.svg)](https://www.iso.org/standard/75281.html)
[![Controls](https://img.shields.io/badge/Controls-ISO%2FIEC%2027002-green.svg)](https://www.iso.org/standard/75652.html)
[![Compliance](https://img.shields.io/badge/Compliance-PDPA%20%7C%20GDPR-orange.svg)]()
[![Report](https://img.shields.io/badge/Report-PDF%20Available-red.svg)](./Computer%20Audit%20Final%20Assessment%20(1).pdf)
[![Status](https://img.shields.io/badge/Audit-Completed%20(Q2%202026)-success.svg)]()

> **Audit Engagement Reference:** ALI-CRA-2026-01  
> **Lead Cyber Risk Auditor:** Anas Faozi Abdullah Al-Abi  
> **Frameworks Applied:** ISO/IEC 27005 (Risk Management) & ISO/IEC 27002 (Information Security Controls)

---

## 📄 Full Assessment Report
- 📥 **[Click Here to View / Download the Complete Audit Report (PDF)](./Computer%20Audit%20Final%20Assessment%20(1).pdf)**

---

## 📌 Executive Summary
This repository presents an end-to-end **Cyber Risk Assessment Report** conducted for a multinational enterprise environment. The assessment follows the **ISO/IEC 27005** lifecycle to evaluate 53 information assets across 5 categories, identify exploitable vulnerabilities, quantify organizational risk using a semi-quantitative $5 \times 5$ matrix, and design a prioritized **Risk Treatment Plan** mapped directly to **ISO/IEC 27002** controls.

---

## 🏗️ In-Scope Network Architecture

```text
                               [ Public Internet ]
                                       │
                         [ Fortinet FortiGate 100F ]
                               (Perimeter Firewall)
                                       │
                               [ Cisco ISR 4321 ]
                                 (Core Router)
                                       │
         ┌─────────────────────────────┴─────────────────────────────┐
         │ (Internal LAN)                                            │ (DMZ Zone)
   [ Cisco 2960 Switch ]                                       [ Cisco 2960 Switch ]
   ├── Cisco RV340W (Wi-Fi) ── Laptops, Phones, Tablets        ├── Apache Web Server (HW-01)
   ├── Workstations & Desktop PCs                              ├── Dell PowerVault Storage (HW-02)
   ├── Cisco IP Telephony (VoIP)                               └── IBM Power S1014 App Server (HW-03)
   └── HP LaserJet Shared Printer
```
## 🔍 Methodology & 6-Phase Risk Lifecycle (ISO/IEC 27005)Context Establishment: 

1. Defined scope across 5 asset tiers (Hardware, Software, Data, Network, Services), evaluated multi-jurisdictional compliance mandates (PDPA, GDPR), and established $5 \times 5$ Likelihood/Impact rating criteria.
2. Risk Identification: Catalogued 12 threat sources, 12 vulnerabilities, and structured 12 comprehensive risk scenarios (RS-01 to RS-12).
3. Risk Analysis: Calculated semi-quantitative risk scores ($1 - 25$) based on threat likelihood, asset criticality, and impact on the CIA Triad
4. Risk Evaluation: Prioritized risks against the organization's risk appetite:
   - Critical (20–25): RS-02 (Phishing / Credential Theft), RS-07 (VPN Credential Compromise)
   - High (15–19): RS-01 (Web Server DDoS), RS-03 (Storage Ransomware), RS-04 (SQL Injection), RS-10 (Router Brute Force)
   - Medium (10–14): RS-05 (Wi-Fi MitM), RS-06 (LAN Malware Spread), RS-08 (Firewall Zero-Day), RS-11 (Social Engineering)
   - Low / Very Low (1–9): RS-09 (VoIP Insider Interception), RS-12 (Printer Document Interception)
5. Risk Treatment: Formulated mitigation strategies combining technical, operational, and organizational controls alongside cyber-insurance transfer.
6. Risk Acceptance & Monitoring: Built an auditable Accepted Risk Register and continuous monitoring cadence.

## 🗓️ 4-Phase Implementation Roadmap

| Phase | Timeline | Target Risks | Key Security Controls & Deliverables | Responsible Team |
| :--- | :--- | :--- | :--- | :--- |
| **Phase 1: Urgent Mitigation** | **Immediate**<br>(0–1 Month) | **RS-07** (VPN Credential Theft)<br>**RS-02** (Phishing / Credential Theft) | • Enforce Multi-Factor Authentication (MFA) across VPN and corporate logins[cite: 1]<br>• Deploy anti-spoofing and strengthened email/web filtering[cite: 1]<br>• Roll out mandatory recurring phishing simulations and awareness training[cite: 1] | Security Operations Team /<br>CISO & IT Security Team[cite: 1] |
| **Phase 2: High-Priority Hardening** | **Short Term**<br>(1–3 Months) | **RS-01** (Web Server DDoS)<br>**RS-03** (Storage Ransomware)<br>**RS-04** (SQL Injection)<br>**RS-10** (Router Management Brute Force) | • Integrate upstream DDoS mitigation/CDN and traffic rate-limiting[cite: 1]<br>• Implement immutable, offline tested backups and Endpoint Detection & Response (EDR)[cite: 1]<br>• Deploy Web Application Firewall (WAF) and enforce parameterized database queries[cite: 1]<br>• Restrict core router management access via Out-of-Band (OOB) ACLs and MFA[cite: 1] | Network Administrator /<br>IT Infrastructure Team /<br>Database Administrator[cite: 1] |
| **Phase 3: Network & Endpoint Controls** | **Medium Term**<br>(3–6 Months) | **RS-05** (Wireless MitM)<br>**RS-06** (LAN Malware Spread)<br>**RS-11** (Social Engineering)<br>**RS-08** (Firewall Zero-Day Exposure) | • Upgrade wireless infrastructure to WPA2/WPA3-Enterprise 802.1X authentication[cite: 1]<br>• Implement internal VLAN network segmentation and Network Access Control (NAC)[cite: 1]<br>• Enforce endpoint software execution policies and formal call-back verification procedures[cite: 1]<br>• Establish strict patch-management cadences and vendor threat-intelligence feeds[cite: 1] | Network Administrator /<br>IT Security Team[cite: 1] |
| **Phase 4: Routine Oversight & Monitoring** | **Routine & Ongoing**<br>(6–12 Months) | **RS-09** (VoIP Telephony Interception)<br>**RS-12** (Shared Printer Interception)<br>All Accepted Residuals | • Segregate VoIP/data VLANs and enable call-access logging[cite: 1]<br>• Isolate shared printer on a dedicated management VLAN with secure/pull printing[cite: 1]<br>• Conduct scheduled semi-annual risk register reviews, quarterly backup-restore tests, and annual penetration testing[cite: 1] | IT Infrastructure Team /<br>System Administrator[cite: 1] |
