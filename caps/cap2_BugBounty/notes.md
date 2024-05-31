# Notes and Remediation

### XSS and Cookie Manipulation

XSS vulnerabilities allow attackers to inject malicious scripts into web pages viewed by other users, often leading to session hijacking through cookie theft. Implementing Content Security Policy (CSP) headers and using HTTP-only cookies are recommended mitigations

### Privilege Escalation

This vulnerability occurs when an application does not adequately enforce access controls, allowing users with lower privileges to elevate their access level. Ensuring strict access controls based on user roles and permissions is crucial.

### Path Traversal

Path traversal attacks enable attackers to navigate the file system hierarchy and access unauthorized files and directories. Effective mitigation involves validating and sanitizing user inputs, using file system permissions to restrict access, and monitoring for suspicious activity.

## Remediation

* Use security headers, validate and sanitize all user inputs, apply the principle of least privilege, and regularly update and patch software components.
* Monitoring and Auditing: Conduct regular security audits and monitor web server logs for signs of suspicious activity to detect and respond to vulnerabilities promptly.