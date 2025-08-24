# Security Policy

## Supported Versions

We release patches for security vulnerabilities as soon as possible.  
Only the latest major version of ShieldCert is officially supported.

| Version | Supported          |
| ------- | ------------------ |
| 1.x     | ✅ Yes             |
| < 1.0   | ❌ No              |

---

## Reporting a Vulnerability

If you discover a security issue, please **do not open a public GitHub issue**.  
Instead, report it responsibly by emailing:

📧 support@shieldcert.com

We will investigate promptly and keep you updated on the resolution.

---

## Security Model

- The **SDK is only a client**: all sensitive operations (encryption, validation, signatures) are performed in the ShieldCert SaaS backend.  
- Without valid API credentials, the SDK cannot be used.  
- We recommend keeping your API keys secure and rotating them regularly.  

---

## Responsible Disclosure

We encourage responsible disclosure.  
If you report a valid security issue that impacts our service or SDK, we will credit you accordingly.
