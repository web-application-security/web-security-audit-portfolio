# Security Headers Review

## Overview

This service focuses on the manual assessment of HTTP security response headers used by web applications.

The purpose is to identify missing, incorrectly configured or potentially ineffective security headers and provide actionable recommendations.

## Scope of Review

The assessment covers the following security controls:

| Security Header | Purpose |
|---|---|
| Content-Security-Policy (CSP) | Restricts the sources from which browsers can load and execute content. |
| Strict-Transport-Security (HSTS) | Instructs browsers to enforce HTTPS connections. |
| X-Content-Type-Options | Helps prevent MIME-type sniffing. |
| Referrer-Policy | Controls the amount of referrer information shared. |
| X-Frame-Options | Helps protect against clickjacking in supported browsers. |
| Permissions-Policy | Controls access to selected browser features. |

The review also considers the CSP `frame-ancestors` directive and whether the selected configurations are appropriate for the application's functionality.

## Assessment Methodology

1. Confirm the authorised scope of the assessment.
2. Collect HTTP response headers from selected application endpoints.
3. Identify missing or potentially insecure configurations.
4. Evaluate findings against relevant security guidance.
5. Document supporting evidence and potential security implications.
6. Provide prioritised remediation recommendations.

## Deliverables

The review report is intended to include:

- Executive summary
- Scope of assessment
- Security header findings
- Supporting technical evidence
- Risk assessment
- Recommended corrective actions

## Limitations

This is a configuration-focused security review, not a comprehensive penetration test.

The presence or absence of a particular header does not automatically establish whether an application is secure or vulnerable. Findings must be assessed in context.

Testing is performed only against systems for which explicit authorisation has been obtained.

## Project Status

Assessment methodology and demonstration reports are under development.

## References

- [OWASP Secure Headers Project](https://owasp.org/www-project-secure-headers/)
- [OWASP HTTP Security Response Headers Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Headers_Cheat_Sheet.html)
