# Master Application Security Testing Workflow

## Purpose

This workflow defines the standard methodology used by AppSec Sentinel for
authorized application security assessments.

The workflow applies to:

* Web applications
* APIs
* Mobile applications

The objective is to ensure that security testing is:

* Structured
* Repeatable
* Evidence-based
* Risk-focused
* Properly documented

---

# Phase 1 — Authorization and Scope

Before active testing begins, establish the assessment scope.

Identify:

* Target application
* Target URLs or endpoints
* Environment
* Authorization status
* Available test accounts
* User roles
* Testing window
* Scope boundaries
* Explicit restrictions

Examples of restrictions:

* No denial-of-service testing
* No destructive testing
* No testing of production systems
* No testing of third-party systems
* Rate limitations

## Output

Produce a scope summary.

| Item          | Details             |
| ------------- | ------------------- |
| Target        |                     |
| Environment   |                     |
| Target Type   | Web / API / Mobile  |
| Authorization | Confirmed / Unknown |
| Restrictions  |                     |
| Test Accounts |                     |
| User Roles    |                     |

---

# Phase 2 — Target Classification

Classify the target.

## Web Application

Load the web security module:

```text
modules/web/owasp-top10.md
```

---

## API

Load the API security module:

```text
modules/api/owasp-api-top10.md
```

---

## Mobile Application

Load the mobile security module:

```text
modules/mobile/mobile-security.md
```

---

# Phase 3 — Discovery

Perform structured discovery before detailed security testing.

Identify:

* Application functionality
* Authentication mechanisms
* User roles
* Sensitive workflows
* APIs
* Input points
* File uploads
* Administrative functions
* External integrations

The objective is to understand the application before testing individual
security categories.

---

# Phase 4 — Attack Surface Mapping

Create a structured attack surface inventory.

Document:

* URLs
* Endpoints
* HTTP methods
* Parameters
* Request bodies
* Authentication requirements
* Authorization requirements
* User roles
* Sensitive functionality

Example:

| Component | Type | Authentication | Role   | Sensitivity |
| --------- | ---- | -------------- | ------ | ----------- |
| Login     | Web  | No             | Public | High        |
| Profile   | Web  | Yes            | User   | High        |
| User API  | API  | Yes            | User   | High        |
| Admin API | API  | Yes            | Admin  | Critical    |

---

# Phase 5 — Testing Plan

Before executing detailed tests, create a testing plan.

The plan should identify:

* Applicable OWASP categories
* Relevant authentication tests
* Relevant authorization tests
* Input validation areas
* Business logic workflows
* Platform-specific testing

Prioritize testing based on:

* Data sensitivity
* Business impact
* Exposure
* Privilege level
* Attack surface

---

# Phase 6 — Security Testing

Execute the relevant testing module.

## Web

Test using:

* OWASP Top 10
* Authentication controls
* Authorization controls
* Session management
* Input validation
* Business logic

---

## API

Test using:

* OWASP API Security Top 10
* Object-level authorization
* Property-level authorization
* Function-level authorization
* Authentication
* Resource controls
* API inventory

---

## Mobile

Test using relevant OWASP MASVS principles.

Evaluate:

* Secure storage
* Authentication
* Network security
* Platform interaction
* Application configuration
* Code security

---

# Phase 7 — Finding Validation

Every potential security issue must be validated before being classified as a
confirmed vulnerability.

For each potential finding:

1. Confirm the behavior is reproducible.
2. Identify the affected component.
3. Confirm the security impact.
4. Determine realistic exploitability.
5. Collect supporting evidence.

Classify results as:

* Confirmed Finding
* Potential Finding
* Informational Observation
* False Positive

Do not report scanner output as a confirmed vulnerability without validation.

---

# Phase 8 — Evidence Collection

Collect appropriate evidence for validated findings.

Evidence may include:

* HTTP requests
* HTTP responses
* Screenshots
* Logs
* Application behavior
* Configuration observations

Evidence should be sufficient for remediation teams to understand and
reproduce the issue safely.

Avoid unnecessarily exposing:

* Passwords
* Authentication tokens
* Personal data
* Production secrets
* Sensitive customer information

---

# Phase 9 — Risk Classification

Classify findings as:

## Critical

A vulnerability with severe potential business or security impact requiring
immediate attention.

## High

A significant vulnerability with serious potential impact.

## Medium

A vulnerability requiring remediation but with more limited impact or
exploitability.

## Low

A lower-risk weakness with limited security impact.

## Informational

A security observation or improvement opportunity without a confirmed
security vulnerability.

Consider:

* Impact
* Exploitability
* Required privileges
* User interaction
* Data sensitivity
* Existing controls

---

# Phase 10 — Remediation Analysis

For each confirmed finding, provide:

* Root cause
* Affected component
* Security impact
* Recommended remediation
* Priority

Recommendations should be:

* Specific
* Practical
* Technically actionable

Avoid generic recommendations such as:

"Improve security."

Instead provide clear guidance appropriate to the affected technology.

---

# Phase 11 — Reporting

Generate a professional security assessment report.

The report should include:

## Executive Summary

Summarize:

* Overall security posture
* Major risks
* Critical findings
* High-priority recommendations

---

## Scope

Document:

* Targets
* Environment
* Testing boundaries
* Restrictions

---

## Methodology

Document:

* Testing methodology
* OWASP standards used
* Modules used

---

## Attack Surface

Summarize the identified application attack surface.

---

## Coverage Matrix

Show:

* Tested areas
* Partially tested areas
* Untested areas

---

## Findings

For each confirmed vulnerability include:

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

---

## Risk Summary

Provide a summary of:

* Critical findings
* High findings
* Medium findings
* Low findings
* Informational observations

---

## Recommendations

Prioritize recommendations.

### Priority 1

Critical vulnerabilities.

### Priority 2

High-risk vulnerabilities.

### Priority 3

Medium-risk vulnerabilities.

### Priority 4

Low-risk improvements.

---

# Phase 12 — Final Security Posture

Provide a concise final assessment.

Include:

* Overall risk level
* Major security strengths
* Major weaknesses
* Remediation priorities
* Important testing limitations

Do not claim that an application is completely secure.

Security testing provides a point-in-time assessment based on the scope and
testing performed.

