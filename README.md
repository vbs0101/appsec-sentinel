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
# 🚀 Installation

## Claude Code

### Personal Installation

Install AppSec Sentinel as a personal Claude Code Skill:

```bash
mkdir -p ~/.claude/skills

git clone https://github.com/vbs0101/appsec-sentinel.git \
~/.claude/skills/appsec-sentinel
```

Your installation should look like:

```text
~/.claude/skills/
└── appsec-sentinel/
    ├── SKILL.md
    ├── modules/
    ├── checklists/
    ├── workflows/
    ├── templates/
    └── examples/
```

Restart Claude Code after installation.

---

## Project Installation

To make AppSec Sentinel available only inside a specific project:

```bash
mkdir -p .claude/skills

git clone https://github.com/vbs0101/appsec-sentinel.git \
.claude/skills/appsec-sentinel
```

The project structure will be:

```text
your-project/
├── .claude/
│   └── skills/
│       └── appsec-sentinel/
│           ├── SKILL.md
│           ├── modules/
│           ├── checklists/
│           ├── workflows/
│           ├── templates/
│           └── examples/
│
└── your-application/
```

---

# 🤖 How to Use

Once installed, start Claude Code:

```bash
claude
```

Then describe the authorized security assessment you want to perform.

## Web Application Example

```text
Use AppSec Sentinel to perform an authorized security assessment.

Target Type: Web Application

Authorization: Confirmed

Environment: Staging

Scope:
- Authentication
- User functionality
- File uploads
- Administrative functionality

Restrictions:
- No destructive testing
- No denial-of-service testing

Assess the application using the relevant OWASP methodology and generate a structured security assessment report.
```

---

## API Example

```text
Use AppSec Sentinel to perform an authorized API security assessment.

Target Type: REST API

Authorization: Confirmed

Environment: Staging

Scope:
- Authentication endpoints
- User endpoints
- Administrative endpoints
- Object-level authorization

Restrictions:
- No destructive testing
- No denial-of-service testing

Assess the API using the OWASP API Security methodology.
Track testing coverage and validate all findings before reporting them.
```

---

## Mobile Application Example

```text
Use AppSec Sentinel to perform an authorized mobile application security assessment.

Platform: Android

Authorization: Confirmed

Scope:
- Authentication
- Secure storage
- Network security
- Deep links
- WebViews

Restrictions:
- No destructive testing
- Do not unnecessarily access production data

Use the relevant mobile security methodology and generate a structured assessment report.
```

---

# 📊 Reporting

AppSec Sentinel includes templates for security reporting.

### Full Security Assessment

```text
templates/security-assessment-report.md
```

### Individual Vulnerability Report

```text
templates/vulnerability-report.md
```

### Security Coverage Matrix

```text
templates/coverage-matrix.md
```

Example:

```text
Generate the final security assessment report using the AppSec Sentinel reporting templates.
Include testing coverage, confirmed findings, recommendations, and testing limitations.
```

---

# 🔄 Updating the Skill

To update AppSec Sentinel:

```bash
cd ~/.claude/skills/appsec-sentinel

git pull
```

Restart Claude Code after updating.


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

