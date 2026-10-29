# ScubaGoggles at Nexus Security Advisors

This is the Nexus Security Advisors fork of [cisagov/ScubaGoggles](https://github.com/cisagov/ScubaGoggles). ScubaGoggles is CISA's tool for assessing Google Workspace tenants against the SCuBA secure configuration baselines (CC0-1.0).

**The upstream code is unchanged.** This `nexus/` folder adds how we use ScubaGoggles in client engagements.

## Why it matters for SMBs

Many startups, nonprofits, schools, and professional-services firms run on Google Workspace. ScubaGoggles checks Gmail, Drive, Meet, Groups, Chat, and admin settings against a **federal baseline**, which gives clients an objective, defensible benchmark.

## How Nexus uses it

| Engagement | Use |
|---|---|
| **Fractional vCISO** | Baseline and quarterly Google Workspace configuration reviews |
| **Compliance readiness** | Evidence for CMMC / 800-171, HIPAA, SOC 2, and cyber-insurance questionnaires (MFA, logging, sharing, email security) |
| **Security posture assessment** | Automated evidence for the Workspace portion of our NIST CSF 2.0 posture review |

## Contents

| File | Purpose |
|---|---|
| [`assessment-runbook.md`](assessment-runbook.md) | Step-by-step client assessment procedure |
| [`framework-mapping.md`](framework-mapping.md) | How ScubaGoggles results map to NIST CSF 2.0, CMMC / 800-171, HIPAA, and SOC 2 |
| [`client-report-checklist.md`](client-report-checklist.md) | Quality gate before a report goes to a client |

## Keeping this fork current

CISA updates the baselines regularly. Sync with upstream before every engagement (**Sync fork**) and record the ScubaGoggles and baseline versions used.

## Disclaimer

Results are a point-in-time view and do not constitute an audit opinion, certification, or legal advice. Not affiliated with or endorsed by CISA.

---

**Nexus Security Advisors** · Fractional CISO and AI governance for SMBs · SDVOSB
[nexussecurityadvisors.com](https://nexussecurityadvisors.com) · [info@nexussecurityadvisors.com](mailto:info@nexussecurityadvisors.com)
