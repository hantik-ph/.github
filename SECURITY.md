# Security policy

Hantik holds other businesses' financial and personal data. Every report is
read and taken seriously.

## Supported versions

Only the latest release of `hantik-ph/hantik` is supported. Releases are tagged
on that repository; the newest tag is the supported line. Older tags receive no
fixes. Upgrade before reporting an issue you can no longer reproduce there.

## Reporting a vulnerability

Do **not** open a public issue, pull request or discussion.

Use GitHub's private vulnerability reporting on the `hantik` repository:
**Security** tab → **Report a vulnerability**. Include what you found, where,
how to reproduce it, and what an attacker could do with it. If it affects
`docs`, report it on `hantik` as well; the same people read both.

## What to expect

- Acknowledgement within **3 business days** (Philippine time).
- The repository owner decides severity, the fix, the timing and any
  disclosure. You will be told what was decided and when it ships.
- Credit in the release notes if you want it.

## Scope

In scope: `hantik-ph/hantik` and `hantik-ph/docs`, and the hosted Hantik
service they build. Tenant isolation, authorization bypass, audit tampering,
secret exposure and money-handling defects are the ones that matter most.

Out of scope: the archived legacy repositories (they are read-only and receive
no fixes), and missing best-practice headers without a demonstrated impact.
