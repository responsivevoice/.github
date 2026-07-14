# Security Policy

## Reporting a vulnerability

Please do not report security vulnerabilities through public GitHub issues, pull requests, or discussions.

Use either of these private channels:

- **GitHub** — open the **Security** tab of the affected repository and choose **Report a vulnerability**. This is the fastest route: the report stays private, and it is where we develop and publish the fix.
- **Email** — [support@responsivevoice.org](mailto:support@responsivevoice.org) with a subject line starting `Security:`, or the [support page](https://responsivevoice.org/support).

Include as much of the following as you can:

- The affected package and version, or the API endpoint.
- What an attacker can achieve, and who is affected.
- Steps to reproduce — a minimal proof of concept is ideal.
- Any mitigation or fix you would suggest.

We will acknowledge your report within 5 business days and keep you informed as we investigate. We will credit you unless you prefer otherwise. Please give us a reasonable opportunity to ship a fix before disclosing publicly.

Fixes ship in a new release of the affected package. We publish a security advisory naming the affected and patched versions, so downstream projects are alerted automatically.

## Scope

In scope: the published `@responsivevoice/*` packages and this organization's public repositories.

The following are **not** vulnerabilities:

- **An API key appearing in client-side code, page source, or network requests.** An API key is a public website identifier, not a credential. Embedding it in a page is the intended design.
- **Example, demo, and sample code.** It exists to illustrate usage, is not production code, and may not receive security fixes.
- **Issues in third-party speech providers** reached with your own provider keys. Please report those to the provider directly.
- **Reports that assume the attacker already holds your API secret or provider keys.** Those are server-side credentials — keep them server-side.

We do not operate a bug bounty program.
