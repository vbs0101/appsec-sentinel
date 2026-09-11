# appsec-sentinel
AI-powered application security testing skill for Claude, aligned with OWASP security testing standards.

# 🛡️ AppSec Sentinel

> A structured Claude Skill for authorized Web Application, API, and Mobile Application Security Testing.

AppSec Sentinel provides a repeatable methodology for performing application security assessments using OWASP-aligned security testing principles.

It helps Claude organize security testing into a structured workflow covering:

* 🌐 Web Applications
* 🔌 APIs
* 📱 Mobile Applications
* 📊 Security Reporting
* ✅ Testing Coverage Tracking

---

# 🚀 Features

## 🌐 Web Application Security Testing

Structured testing aligned with:

* OWASP Top 10
* Authentication testing
* Authorization testing
* Session management
* Business logic testing
* Security misconfiguration review

---

## 🔌 API Security Testing

Structured testing aligned with:

* OWASP API Security Top 10
* Object-Level Authorization
* Property-Level Authorization
* Function-Level Authorization
* Authentication
* API inventory management
* Sensitive business flows

---

## 📱 Mobile Application Security Testing

Mobile testing guidance aligned with OWASP MASVS principles.

Supports:

* Android
* iOS
* Secure storage
* Authentication
* Network security
* Deep links
* WebViews
* Platform interaction
* Application configuration

---

## 📋 Structured Testing Workflow

AppSec Sentinel follows a repeatable assessment process:

```text
Authorization & Scope
        ↓
Target Classification
        ↓
Discovery
        ↓
Attack Surface Mapping
        ↓
Testing Plan
        ↓
Security Testing
        ↓
Finding Validation
        ↓
Evidence Collection
        ↓
Risk Classification
        ↓
Reporting
```

---

# 📁 Project Structure

```text
appsec-sentinel/
│
├── SKILL.md
│
├── modules/
│   ├── web/
│   │   └── owasp-top10.md
│   │
│   ├── api/
│   │   └── owasp-api-top10.md
│   │
│   └── mobile/
│       └── mobile-security.md
│
├── workflows/
│   └── security-testing-workflow.md
│
├── checklists/
│   ├── web-checklist.md
│   ├── api-checklist.md
│   └── mobile-checklist.md
│
├── templates/
│   ├── vulnerability-report.md
│   ├── security-assessment-report.md
│   └── coverage-matrix.md
│
├── examples/
│   ├── web-application-assessment.md
│   ├── api-security-assessment.md
│   └── mobile-security-assessment.md
│
├── CONTRIBUTING.md
├── SECURITY.md
└── LICENSE
```

---

# 🎯 How It Works

AppSec Sentinel is designed as a Claude Skill.

The skill should:

1. Identify the target type.
2. Confirm authorization and scope.
3. Load the appropriate security testing module.
4. Map the attack surface.
5. Apply relevant OWASP testing categories.
6. Track testing coverage.
7. Validate potential findings.
8. Collect appropriate evidence.
9. Classify security risk.
10. Generate a professional assessment report.

---

# 🧪 Supported Security Standards

AppSec Sentinel currently provides guidance aligned with:

* OWASP Top 10
* OWASP API Security Top 10
* OWASP MASVS principles

---

# 💻 Example Usage

## Web Application

```text
Perform an authorized security assessment of this web application.

Target:
https://staging.example.com

Environment:
Staging

Scope:
- Authenticated functionality
- User role
- Administrator role

Restrictions:
- No destructive testing
- No denial-of-service testing
```

---

## API

```text
Perform an authorized security assessment of this API.

Target:
https://api-staging.example.com

Environment:
Staging

Authentication:
Bearer token

Scope:
- REST API
- User endpoints
- Administrator endpoints
```

---

## Mobile Application

```text
Perform an authorized security assessment of this Android application.

Application:
company-app.apk

Scope:
- Static analysis
- Dynamic analysis
- Authentication
- Local storage
- Network security
```

---

# 📊 Assessment Output

AppSec Sentinel is designed to produce structured security assessment results including:

* Executive Summary
* Scope
* Testing Methodology
* Attack Surface Summary
* Security Coverage Matrix
* Confirmed Findings
* Potential Findings
* Informational Observations
* Risk Summary
* Remediation Recommendations
* Testing Limitations

---

# ⚠️ Authorization and Responsible Use

AppSec Sentinel is intended **only for authorized security testing**.

Users must ensure they have explicit permission before testing:

* Web applications
* APIs
* Mobile applications
* Backend infrastructure
* Third-party services

Do not use this project to perform unauthorized security testing.

---

# 🗺️ Roadmap

Future improvements may include:

* [ ] Automated testing integrations
* [ ] Burp Suite workflow guidance
* [ ] OWASP ASVS mapping
* [ ] Expanded OWASP MASVS coverage
* [ ] GraphQL-specific testing guidance
* [ ] Authentication testing module
* [ ] Business logic testing module
* [ ] Automated report generation
* [ ] CI/CD security testing workflows

---

# 🤝 Contributing

Contributions are welcome!

Please read:

* `CONTRIBUTING.md`
* `SECURITY.md`

before submitting contributions or reporting security issues.

---

# 📜 License

This project is licensed under the MIT License.

See the `LICENSE` file for details.

---

# ⭐ Support

If you find AppSec Sentinel useful:

⭐ Star the repository

🐛 Report issues

🤝 Contribute improvements

🛡️ Help make application security testing more structured and accessible.

