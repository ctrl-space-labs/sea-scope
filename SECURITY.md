# Security

## Reporting vulnerabilities

If you believe you have found a security vulnerability, please report it
responsibly through the project maintainers’ preferred channel (issue tracker
or private security contact), not via public issues with exploit details.

## Secret scanning before release

Maintainers should run a **git-history** secret scanner on the full repository
before making it public, and rotate any credentials that were ever exposed.

Example using [Gitleaks](https://github.com/gitleaks/gitleaks):

```bash
# Install (pick one): https://github.com/gitleaks/gitleaks#installing
# brew install gitleaks

gitleaks detect --source . --verbose
```

## Local configuration

Application builds may use environment variables such as
`NEXT_PUBLIC_GEE_CLIENT_ID` and `NEXT_PUBLIC_GENDOX_URL`. **Never commit**
real API keys, OAuth client secrets, or `.env` files containing them. Use
`.env.example` with placeholder values if you document local setup.
