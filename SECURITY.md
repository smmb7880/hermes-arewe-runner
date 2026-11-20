
# Security Policy

## Secrets
- Never commit API keys, ADMIN_TOKEN, access tokens, or credentials.
- Store runtime credentials only in GitHub Actions Secrets.
- Never print secrets in workflow logs.
- Never expose secrets in agent prompts, reports, or generated files.
- Do not use real credentials in test fixtures.

## Repository boundaries
- This repository contains deployment and orchestration code only.
- Never commit private AREWE source code, user data, database exports, or private business information.
- Keep Cloudflare credentials and configuration secrets outside source control.
- Do not modify the AREWE application repository.

## Free-only policy
- Use only explicitly approved free inference providers.
- Never configure paid fallbacks, paid upgrades, or automatic billing.
- Stop safely when free quotas or provider limits are reached.
- Never use a payment method or paid service without explicit authorization.

## Agent permissions
- Research, analysis, drafting, and internal planning are allowed.
- Publishing content, sending messages, creating accounts, spending money,
  collecting personal information, changing pricing, or making business
  commitments require explicit human approval.
- Agents must not claim unverified product features, metrics, testimonials,
  or business results as facts.

## Workflow security
- Do not run autonomous agent workflows on untrusted pull requests.
- Use least-privilege GitHub Actions permissions.
- Set execution time limits.
- Validate external input before using it in shell commands or SQL.
- Do not expose private data in public workflow logs.

## Incident response
If a secret is exposed:
1. Revoke or rotate it immediately.
2. Review recent workflow runs and repository history.
3. Replace affected credentials in GitHub Secrets.
4. Do not assume deleting a committed secret removes it from Git history.
