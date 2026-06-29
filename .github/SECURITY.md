# Security Policy

## Reporting a Vulnerability

Do not open a public GitHub issue, pull request, discussion, or comment for suspected security vulnerabilities.

Report suspected vulnerabilities privately to the Dollar Cone repository owner or repository administrators through the existing private Dollar Cone operating channel. If you already have repository access, use a private repository security advisory or another private maintainer channel.

Include:

- Affected repository, branch, and commit SHA when known
- Clear reproduction steps or proof of concept
- Expected impact and affected users, tenants, stores, or data classes
- Whether any credentials, customer data, payment data, accounting data, or production systems may be involved

If you accidentally disclosed sensitive information publicly, immediately remove the disclosure where possible and notify the repository owner or administrators privately.

## Supported Versions

Dollar Cone repositories receive security fixes on the default branch and currently deployed production versions. Historical branches, archived previews, and local experiment branches are not supported unless a repository explicitly states otherwise.

## Security Handling

- Security reports are triaged privately before public disclosure.
- Fixes should be developed in private branches, private advisories, or restricted maintainer channels when disclosure risk exists.
- Leaked secrets, tokens, connection strings, certificates, payment credentials, accounting credentials, tenant credentials, and production access material must be rotated, not only removed from Git history.
- Customer, staff, payment, accounting, and tenant data must not be copied into public issues, public PRs, logs, screenshots, or test fixtures.
- Production-impacting actions require the appropriate repository owner, provider owner, tenant administrator, billing owner, or operations owner.

## Baseline Controls

- Use GitHub Dependabot and code scanning findings as security work inputs.
- Keep CI/CD secrets in GitHub Actions secrets, environment secrets, OIDC-backed identity, or the repository's established secret-management pattern.
- Do not hardcode secrets or environment-specific credentials in source code, scripts, documentation, or test fixtures.
- Treat files, uploads, generated content, webhook payloads, and external provider responses as untrusted input.
- Preserve least-privilege access for GitHub, cloud, payment, accounting, and operational provider credentials.