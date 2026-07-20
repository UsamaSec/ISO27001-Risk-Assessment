# Statement of Applicability (SoA) — Riverside Family Clinic (Fictional)

Per ISO/IEC 27001, the Statement of Applicability documents which Annex A controls are applicable to the organization, whether they are implemented, and the justification for inclusion or exclusion — directly informed by the risk assessment and treatment plan.

| Control Ref | Control Name | Applicable? | Status | Justification (linked to Risk Register) |
|-------------|----------------|-------------|--------|--------------------------------------------|
| A.5.15 | Access Control | Yes | Planned | Addresses R-02 (unauthorized EHR access) via RBAC implementation |
| A.5.16 | Identity Management | Yes | Planned | Supports enforcement of least privilege across A-01, A-02 |
| A.5.17 | Authentication Information | Yes | Planned | Addresses R-03 via MFA enforcement on billing system |
| A.5.23 | Information Security for Cloud Services | Yes | Planned | Addresses R-08 (scheduling backup storage) |
| A.6.3 | Security Awareness, Education and Training | Yes | Planned | Addresses R-03, R-04 through phishing/social engineering training |
| A.7.4 | Physical Security Monitoring | Yes | Planned | Addresses R-07 (archive room access) |
| A.8.7 | Protection Against Malware | Yes | Planned | Addresses R-01 (ransomware) via endpoint detection |
| A.8.9 | Configuration Management | Yes | Planned | Addresses R-01 (unpatched legacy server) |
| A.8.13 | Information Backup | Yes | Planned | Addresses R-01 via offline/immutable backup implementation |
| A.8.20 | Network Security | Yes | Planned | Addresses R-05 (Wi-Fi segmentation) |
| A.8.24 | Use of Cryptography | Yes | Planned | Addresses R-06 (laptop encryption) |
| A.8.28 | Secure Coding | No | Excluded | Clinic does not develop custom software; no in-house application development |
| A.5.30 | ICT Readiness for Business Continuity | Yes | Planned | Supports resilience of EHR system (A-01) beyond backup alone |

## Exclusion Rationale Summary
One control (A.8.28 — Secure Coding) was excluded as not applicable, since the clinic does not engage in any custom software development and relies entirely on third-party clinical systems. All other reviewed controls were determined applicable given the clinic's handling of sensitive patient data and were mapped directly to identified risks in the risk register.
