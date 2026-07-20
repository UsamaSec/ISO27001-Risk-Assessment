# Risk Assessment Report - Riverside Family Clinic (Fictional)

## 1. Scope and Context

**Organization:** Riverside Family Clinic (fictional) - a small outpatient healthcare provider with approximately 25 staff, handling electronic patient health records (ePHI), appointment scheduling, and billing.

**Scope of Assessment:** IT systems and data supporting clinical operations, including the electronic health record (EHR) system, front-desk scheduling system, billing/payment processing, and staff email/communication systems.

**Regulatory Context:** As a healthcare provider handling patient data, the clinic is subject to data protection obligations (e.g., HIPAA-equivalent requirements) in addition to pursuing ISO/IEC 27001 alignment for its information security management system (ISMS).

## 2. Asset Inventory

| Asset ID | Asset | Description | Classification |
|----------|-------|--------------|------------------|
| A-01 | EHR System | Stores patient medical records, diagnoses, treatment history | Restricted |
| A-02 | Billing System | Stores patient payment and insurance information | Restricted |
| A-03 | Front-Desk Scheduling System | Patient appointment data, contact information | Confidential |
| A-04 | Staff Email System | Internal and external communications | Confidential |
| A-05 | Clinic Wi-Fi Network | Network infrastructure supporting all systems | Internal |
| A-06 | Staff Laptops/Workstations | Endpoint devices used to access clinical systems | Confidential |
| A-07 | Physical Patient Files (archived) | Legacy paper records in storage | Restricted |

## 3. Risk Register

Risk scored as **Likelihood (1-5) × Impact (1-5) = Risk Score**, with Low (1-6), Medium (7-14), High (15-25).

| Risk ID | Asset | Threat | Vulnerability | Likelihood | Impact | Risk Score | Rating |
|---------|-------|--------|-----------------|------------|--------|------------|--------|
| R-01 | A-01 (EHR) | Ransomware attack | No offline backups; unpatched OS on legacy server | 4 | 5 | 20 | High |
| R-02 | A-01 (EHR) | Unauthorized staff access to records outside job need | No role-based access control configured | 3 | 4 | 12 | Medium |
| R-03 | A-02 (Billing) | Phishing leading to payment data theft | No MFA on billing system login | 4 | 4 | 16 | High |
| R-04 | A-04 (Email) | Business email compromise | No email authentication (SPF/DKIM/DMARC) configured | 3 | 3 | 9 | Medium |
| R-05 | A-05 (Wi-Fi) | Unauthorized network access | Guest and staff Wi-Fi not segmented | 3 | 3 | 9 | Medium |
| R-06 | A-06 (Laptops) | Device theft/loss | No full-disk encryption on staff laptops | 3 | 4 | 12 | Medium |
| R-07 | A-07 (Physical files) | Unauthorized physical access | Archive room not locked outside business hours | 2 | 3 | 6 | Low |
| R-08 | A-03 (Scheduling) | Data exposure via misconfigured cloud storage | Scheduling backups stored on unsecured shared drive | 3 | 3 | 9 | Medium |

## 4. Risk Treatment Plan

| Risk ID | Treatment Decision | Recommended Action | Priority |
|---------|----------------------|----------------------|----------|
| R-01 | Mitigate | Implement offline/immutable backups; patch legacy server OS; deploy endpoint detection | Critical |
| R-02 | Mitigate | Implement role-based access control (RBAC) on EHR system, enforce least privilege | High |
| R-03 | Mitigate | Enforce MFA on billing system; conduct phishing awareness training | Critical |
| R-04 | Mitigate | Configure SPF, DKIM, and DMARC on email domain | Medium |
| R-05 | Mitigate | Segment guest Wi-Fi from clinical network via VLAN | Medium |
| R-06 | Mitigate | Enable full-disk encryption (BitLocker/FileVault) on all staff devices | High |
| R-07 | Accept (with monitoring) | Add door lock with access log; review access quarterly | Low |
| R-08 | Mitigate | Move scheduling backups to access-controlled, encrypted storage | Medium |

## 5. Summary
This assessment identified 8 risks across the clinic's core information assets, with 2 rated High, 5 Medium, and 1 Low. The highest-priority risks (R-01, R-03) involve the EHR and billing systems - the clinic's most sensitive assets - and stem from missing backups, unpatched systems, and lack of MFA. Recommended treatments focus primarily on mitigation through technical controls (encryption, access control, MFA) and administrative controls (training, access review), consistent with ISO 27001 Annex A control categories detailed in the accompanying Statement of Applicability.
