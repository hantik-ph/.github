# Security policy

Hantik holds other businesses' financial and personal data. Every report is taken seriously.

## Reporting

Do **not** open a public issue.

Use GitHub's private vulnerability reporting on the affected repository (**Security → Report a vulnerability**), or email `security@hantik.ph`.

Include: what you found, where, how to reproduce it, and what an attacker could do with it.

## What to expect

- Acknowledgement within 2 working days.
- A fix or mitigation plan within 14 days for anything exposing tenant data, money, authorization or audit.
- Credit in the release notes if you want it.

## Scope

All repositories in `hantik-ph` and the hosted Hantik service. Tenant isolation, authorization bypass, audit tampering, secret exposure and money-handling defects are in scope. Missing best-practice headers without a demonstrated impact are not.
