---
name: security-audit
description: "Analyzes the code for security vulnerabilities: injection, XSS, secret handling, authentication and authorization. Use before a release."
---

# Security Audit

Run a security audit on the following code. Look in particular for:

- SQL/Command/Path injection
- XSS and unsanitized output
- hardcoded secrets (passwords, tokens, API keys)
- authentication and authorization issues
- use of deprecated or insecure dependencies/functions

For each issue, indicate: severity (critical/high/medium/low), the affected line, an explanation and a proposed fix.

```$FILE_EXTENSION
$SELECTION
```
