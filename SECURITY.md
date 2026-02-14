# Security Policy

## Supported Versions

This project is currently in active development and should be considered **experimental/research software**. Security updates are provided only for the latest version of the repository.

| Version                | Supported     |
| ---------------------- | ------------- |
| Latest (main branch)   | Supported     |
| Older commits/releases | Not Supported |

---

## Reporting a Vulnerability

If you discover a security vulnerability, please report it **privately via GitHub Security Advisories**.

### How to Report

1. Open the repository on GitHub
2. Navigate to the **Security** tab
3. Click **Report a vulnerability**
4. Submit a private advisory with full details

Please **do not open public issues** for security vulnerabilities.

---

## What to Include in a Report

To help us triage and remediate quickly, include:

* Clear description of the vulnerability
* Steps to reproduce (Proof of Concept)
* Potential impact and risk
* Affected components/files
* Suggested remediation (optional)

Reports with a working PoC are highly appreciated.

---

## Coordinated Disclosure Process

We follow a coordinated vulnerability disclosure approach:

1. Acknowledge report within **72 hours**
2. Provide initial assessment within **7 days**
3. Communicate remediation timeline within **14 days**
4. Public disclosure after a fix has been released

We kindly ask researchers to avoid:

* Public disclosure before a patch is available
* Accessing or modifying real user data
* Disrupting service availability
* Performing large-scale automated scanning

Testing must remain **non-destructive**.

---

## Security Considerations for Deployment

This project is intended for **local or controlled deployments** unless additional security controls are implemented.

Before deploying publicly, ensure the following controls are in place.

### Authentication and Authorization

Protect the application using OAuth, SSO, or API keys.

### Rate Limiting

Implement per-user or per-IP rate limiting to prevent abuse and denial-of-service attacks.

### File Upload Security

Enforce strict validation for uploaded files:

* Restrict file types
* Enforce file size limits
* Scan files before processing

### Network Egress Restrictions

Restrict outbound network access to trusted destinations to mitigate SSRF risks.

### Secrets Management

Use a secure secrets manager. Do not store credentials in code or environment files.

### Monitoring and Logging

Enable logging, alerting, and anomaly detection.

### Secure Deployment

Deploy behind HTTPS and a reverse proxy or Web Application Firewall (WAF).

---

## AI / LLM Security Notice

Applications using large language models are susceptible to:

* Prompt injection attacks
* Data exfiltration through prompts
* Jailbreak attempts
* Automated abuse and resource exhaustion

Production deployments should implement:

* Prompt validation and filtering
* Output monitoring and filtering
* Isolation of retrieval pipelines (RAG)
* Usage quotas and monitoring

---

## Dependency Security

Recommended practices:

* Pin dependency versions
* Perform regular vulnerability scanning
* Use trusted package registries

---

## Security Updates

Security fixes will be released as soon as reasonably possible after validation.

---

## Acknowledgement

We appreciate the security research community and responsible disclosure that helps improve the safety and reliability of this project.

---
