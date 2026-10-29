# Framework Mapping: ScubaGoggles Baselines

How to map ScubaGoggles (Google Workspace SCuBA baseline) results to the frameworks Nexus clients care about. This is a **family-level starting point**; validate each mapping against the specific control text before it goes into a client report.

| SCuBA baseline area | NIST CSF 2.0 | NIST SP 800-171 / CMMC L2 | HIPAA Security Rule | SOC 2 (TSC) |
|---|---|---|---|---|
| **Common controls:** 2-Step Verification, super-admin accounts, session length, SSO | PR.AA | 3.1 Access Control, 3.5 Identification & Authentication | §164.312(a) Access control, §164.312(d) Authentication | CC6.1–CC6.3 |
| **Gmail:** SPF/DKIM/DMARC, auto-forwarding, attachment and link protections | PR.DS, PR.PS | 3.13 System & Communications Protection, 3.14 System & Information Integrity | §164.312(e) Transmission security, §164.308(a)(5)(ii)(B) Malicious software | CC6.7, CC6.8 |
| **Drive & Docs:** external sharing, link defaults, shared drives | PR.DS, PR.AA | 3.1 Access Control (3.1.3 control CUI flow) | §164.312(a) Access control | CC6.1, CC6.7 |
| **Meet / Chat / Groups / Sites / Calendar:** external access and visibility | PR.AA, PR.DS | 3.1 Access Control | §164.312(a) Access control | CC6.1 |
| **Audit and alerting** (common controls, alert center) | DE.CM, DE.AE | 3.3 Audit & Accountability | §164.312(b) Audit controls | CC7.2–CC7.3 |
| **Marketplace / third-party app access** | GV.SC, PR.PS | 3.4 Configuration Management | §164.308(b) Business associate contracts (where apps handle PHI) | CC9.2 |

## Notes

- CMMC Level 2 practices align with NIST SP 800-171 requirements; cite the 800-171 requirement number in reports. Confirm whether the client's Workspace edition and configuration are appropriate for CUI before positioning it as in-scope.
- For HIPAA clients, confirm a signed Google Workspace BAA exists and PHI is limited to covered services.
- HIPAA is risk-based. Present findings as inputs to the client's risk analysis, not as pass/fail compliance.
