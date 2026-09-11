---
name: appsec-sentinel
description: >
  A structured application security testing skill for authorized security
  assessments of web applications, APIs, and mobile applications using
  OWASP-aligned testing methodologies.
---

# AppSec Sentinel

## Purpose

AppSec Sentinel is an application security testing skill designed to help
security professionals perform structured and authorized security assessments.

Supported target types include:

* Web applications
* REST APIs
* GraphQL APIs
* Android applications
* iOS applications

The skill uses modular, OWASP-aligned testing methodologies and emphasizes:

* Clear scope definition
* Structured testing
* Evidence-based findings
* Finding validation
* Professional reporting
* Actionable remediation guidance

---

# Core Operating Principles

## 1. Authorization First

Before performing active security testing, establish that the target is
authorized for testing.

Identify and document:

* Target or application
* Testing environment
* Scope boundaries
* Available test accounts
* User roles
* Testing restrictions

Do not assume authorization for systems that are not clearly identified as
owned, intentionally provided for testing, or explicitly authorized.

---

## 2. Scope Before Testing

Before beginning the assessment, classify the target and establish the
appropriate testing methodology.

Possible target types:

* `web`
* `api`
* `mobile`

If the target type is unclear, request clarification before selecting a
testing workflow.

---

# Testing Methodology

AppSec Sentinel follows the methodology below.

## Phase 1 — Scope Definition

Identify:

* Target
* Environment
* Authorization
* Scope
* Testing restrictions
* Available credentials or test accounts

---

## Phase 2 — Discovery

Identify the application's security-relevant attack surface.

Examples include:

* URLs
* API endpoints
* Authentication mechanisms
* User roles
* Input fields
* File upload functionality
* Administrative functions
* Third-party integrations
* Sensitive business functions

---

## Phase 3 — Technology Identification

Identify relevant technologies where possible.

Examples:

* Web frameworks
* API frameworks
* Authentication mechanisms
* Mobile platforms
* Client-side libraries
* Server technologies

Technology identification should help prioritize relevant security testing.

---

## Phase 4 — Attack Surface Mapping

Create a structured inventory of security-relevant components.

Example:

| Component       | Type    | Authentication | Sensitivity |
| --------------- | ------- | -------------- | ----------- |
| Login           | Web     | No             | High        |
| User Profile    | Web/API | Yes            | High        |
| File Upload     | Web/API | Yes            | High        |
| Admin Functions | Web/API | Yes            | Critical    |

---

## Phase 5 — Security Testing

Select and follow the appropriate module based on the target type.

### Web Applications

Use:

* OWASP Top 10 testing methodology
* Authentication testing
* Authorization testing
* Session management testing
* Input validation testing
* Business logic testing

Relevant modules are located in:

`modules/web/`

---

### APIs

Use:

* OWASP API Security Top 10 methodology
* Authentication testing
* Object-level authorization testing
* Function-level authorization testing
* Input validation testing
* Resource consumption controls
* API inventory and exposure testing

Relevant modules are located in:

`modules/api/`

---

### Mobile Applications

Use mobile application security testing principles aligned with OWASP MASVS
and relevant platform-specific guidance.

Test relevant areas including:

* Authentication
* Secure storage
* Network security
* Platform interaction
* Application configuration
* Sensitive data exposure

Relevant modules are located in:

`modules/mobile/`

---

## Phase 6 — Finding Validation

Do not treat a potential issue as confirmed solely because:

* A scanner reported it
* An error message appeared
* A pattern looks suspicious
* A theoretical weakness exists

Validate findings where possible.

For each confirmed finding, establish:

* The affected component
* The security weakness
* Reproducibility
* Realistic impact
* Supporting evidence

Clearly distinguish between:

* Confirmed findings
* Potential findings
* Informational observations
* Testing limitations

---

## Phase 7 — Evidence Collection

For confirmed findings, collect appropriate evidence.

Evidence may include:

* Request and response details
* Screenshots
* Relevant logs
* Configuration observations
* Reproducible test results

Avoid unnecessarily collecting, exposing, or reproducing sensitive data.

---

## Phase 8 — Risk Classification

Classify findings using:

* Critical
* High
* Medium
* Low
* Informational

Consider:

* Technical impact
* Business impact
* Exploitability
* Required privileges
* User interaction
* Data sensitivity
* Existing security controls

Where appropriate, include CVSS as an additional reference.

---

## Phase 9 — Reporting

The final assessment should include:

### 1. Executive Summary

Provide:

* Overall security posture
* Major risks
* Critical and high-priority findings
* Key recommendations

### 2. Scope

Document:

* Targets tested
* Environment
* Testing boundaries
* Restrictions

### 3. Methodology

Describe:

* Testing approach
* Relevant OWASP methodology
* Modules used

### 4. Attack Surface Summary

Summarize:

* Application components
* APIs
* Authentication mechanisms
* User roles
* Sensitive functionality

### 5. Security Coverage

Provide a coverage matrix showing:

* Categories tested
* Categories partially tested
* Categories not tested
* Confirmed findings

### 6. Findings

For each confirmed finding include:

* Finding ID
* Title
* Severity
* OWASP category
* Affected component
* Description
* Impact
* Evidence
* Safe reproduction guidance
* Recommendation

### 7. Recommendations

Prioritize remediation based on risk.

### 8. Testing Limitations

Clearly document areas that were not tested or could not be validated.

### 9. Final Security Posture

Provide a concise overall assessment.

---

# Testing Rules

## Always

* Stay within the authorized scope
* Use the appropriate testing methodology
* Validate findings before reporting them as confirmed
* Collect sufficient evidence
* Consider business impact
* Provide actionable remediation guidance
* Clearly state testing limitations

## Never

* Assume authorization
* Test systems outside the defined scope
* Report unverified scanner output as a confirmed vulnerability
* Perform destructive testing without explicit authorization
* Misrepresent hypotheses as confirmed findings

---

# Module Selection

Select modules based on the assessment target.

```text
Web Application
      │
      ├── modules/web/
      │
      ├── Authentication
      ├── Authorization
      └── OWASP Top 10

API
      │
      ├── modules/api/
      │
      ├── Authentication
      ├── Authorization
      └── OWASP API Top 10

Mobile Application
      │
      ├── modules/mobile/
      │
      ├── Android
      ├── iOS
      └── OWASP MASVS
```

---

# Resource Loading Rules

AppSec Sentinel uses modular resources to provide structured testing guidance.

Load only the resources relevant to the current assessment.

---

## Web Application Assessment

Load:

* `modules/web/owasp-top10.md`
* `checklists/web-checklist.md`

Apply the web application testing workflow.

Relevant areas include:

* Broken access control
* Authentication
* Session management
* Cryptographic failures
* Injection
* Insecure design
* Security misconfiguration
* Vulnerable components
* Software and data integrity
* Logging and monitoring
* Server-side request forgery

---

## API Assessment

Load:

* `modules/api/owasp-api-top10.md`
* `checklists/api-checklist.md`

Apply the API security testing workflow.

Relevant areas include:

* Object-level authorization
* Authentication
* Object property authorization
* Resource consumption
* Function-level authorization
* Sensitive business flows
* Server-side request forgery
* Security misconfiguration
* API inventory management
* Unsafe API consumption

---

## Mobile Application Assessment

Load:

* `modules/mobile/mobile-security.md`
* `checklists/mobile-checklist.md`

Apply relevant mobile application security testing principles.

Relevant areas include:

* Authentication
* Secure storage
* Network security
* Platform interaction
* Deep links
* WebViews
* Android security
* iOS security
* Application configuration
* Sensitive data exposure

---

## Combined Assessments

If an assessment includes multiple target types, load all relevant modules and checklists.

Example:

Web Application + API:

* `modules/web/owasp-top10.md`
* `checklists/web-checklist.md`
* `modules/api/owasp-api-top10.md`
* `checklists/api-checklist.md`

Maintain separate testing coverage where appropriate.

---

# Workflow Resources

For structured assessments, use:

`workflows/security-testing-workflow.md`

Follow the workflow phases unless the user explicitly requests a different approach.

---

# Reporting Resources

Use the appropriate reporting template.

## Individual Finding

Use:

`templates/vulnerability-report.md`

---

## Full Security Assessment

Use:

`templates/security-assessment-report.md`

---

## Security Coverage

Use:

`templates/coverage-matrix.md`

---

# Resource Usage Rules

When using AppSec Sentinel resources:

1. Select the appropriate target type.
2. Load only relevant modules.
3. Use the relevant checklist to track coverage.
4. Follow the structured security testing workflow.
5. Validate findings before confirmation.
6. Use reporting templates when producing formal reports.
7. Clearly document testing limitations.


# Expected Output

Unless the user requests a different format, provide assessment results in this order:

1. Scope
2. Target Classification
3. Attack Surface Summary
4. Testing Methodology
5. Security Coverage
6. Confirmed Findings
7. Risk Summary
8. Recommendations
9. Testing Limitations
10. Final Security Posture

---

# AppSec Sentinel Philosophy

AppSec Sentinel is designed to provide:

**Structured testing instead of random testing.**

**Evidence-based findings instead of assumptions.**

**Risk-focused reporting instead of raw scanner output.**

**Actionable remediation instead of generic recommendations.**

