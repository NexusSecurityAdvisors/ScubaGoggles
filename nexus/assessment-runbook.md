# ScubaGoggles Assessment Runbook

Procedure for running ScubaGoggles in a Nexus client engagement. Always check the [upstream documentation](https://github.com/cisagov/ScubaGoggles) for current prerequisites, OAuth/API setup, and commands.

## 0. Before you start

- [ ] Signed SOW and written authorization naming the Google Workspace tenant in scope
- [ ] Client super-admin available to authorize access and later revoke it
- [ ] Evidence folder created: `<Client>/<YYYY-MM-DD>-scubagoggles/`
- [ ] Python environment matching the upstream version requirement

## 1. Access (read-only, least privilege)

- ScubaGoggles reads settings through Google APIs using either user OAuth credentials or a service account with domain-wide delegation. Follow the upstream permissions guide and grant **read-only scopes only**.
- Prefer a dedicated, temporary Google Cloud project for the assessment so it can be deleted afterward.
- Record who authorized access, when, and the planned removal date.

## 2. Prepare

```bash
pip install scubagoggles
scubagoggles setup        # configure output directory and credentials (per upstream docs)
```

Record the ScubaGoggles version installed.

## 3. Run

```bash
scubagoggles gws          # assess all supported Workspace products
```

Use the upstream options to limit products if the scope requires it. Copy the HTML report and JSON results to the client evidence folder and record SHA-256 hashes.

## 4. Triage

1. Start with failed **"shall"** requirements, then "should" requirements.
2. Confirm each failure in the Admin console; document compensating controls (for example, a third-party email gateway or SSO provider).
3. Rate on the Nexus 5×5 likelihood × impact scale.
4. Map to frameworks using [`framework-mapping.md`](framework-mapping.md).
5. Prioritize identity first (2SV, super-admin hygiene, SSO), then Gmail security, then Drive sharing and logging.

## 5. Report and close out

- Complete [`client-report-checklist.md`](client-report-checklist.md).
- Revoke OAuth grants / domain-wide delegation and delete the temporary Cloud project; confirm with the client in writing.
- Schedule the re-assessment (quarterly for vCISO clients).
