# LogSentinel: Cybersecurity Capstone Project

A client-side, defensive log analyzer. It parses Apache/Nginx combined access logs and SSH `auth.log` lines and flags SQL injection, XSS, path traversal, sensitive-file probes, scanner user-agents, brute-force logins and directory enumeration. Each alert maps to an OWASP Top 10 or MITRE ATT&CK reference.

**Privacy:** logs never leave the browser. There is no backend, database or third-party script.

## Run locally
    npx serve .        # or: python3 -m http.server 8000
Open http://localhost:8000 and click "Load sample log".

## Tests
    node test.js

## Deploy to Netlify
- Drag and drop this folder (or the zip contents) at https://app.netlify.com/drop, or
- Push to GitHub, then "Add new site > Import from Git". Build command: none. Publish directory: `.`

`netlify.toml` applies a strict Content-Security-Policy and other security headers.

## Docs
- `docs/ARCHITECTURE.md`: security architecture and threat model
- `docs/TESTING_REPORT.md`: test results
- `docs/SUBMISSION.md`: demo video script and LinkedIn post draft

## Scope and ethics
Defensive analysis only. Use it on logs from systems you own or are authorized to review. The sample log contains synthetic data using reserved documentation IP ranges.
