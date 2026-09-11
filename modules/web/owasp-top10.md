# OWASP Top 10 Web Application Security Testing Module

## Purpose

This module provides a structured methodology for assessing authorized web
applications against the OWASP Top 10.

The objective is to identify and validate relevant security weaknesses while
maintaining clear evidence, testing coverage, and scope awareness.

---

# Testing Preparation

Before beginning testing, identify:

* Application URL or URLs
* Testing environment
* Authentication requirements
* Available test accounts
* User roles
* Scope limitations
* Restricted functionality
* Sensitive application areas

Create an initial application inventory before beginning category-specific
testing.

---

# A01 — Broken Access Control

## Objective

Verify that users can access only the resources and functions they are
authorized to access.

## Test Areas

Evaluate:

* Horizontal access control
* Vertical access control
* Object-level authorization
* Direct object references
* Forced browsing
* Administrative functionality
* API-backed application functions

## Testing Questions

Ask:

* Can one user access another user's resources?
* Can a lower-privileged user access privileged functions?
* Is authorization enforced server-side?
* Are object identifiers trusted without authorization checks?
* Are hidden application functions still accessible directly?

## Evidence

Document:

* User role
* Requested resource
* Expected result
* Actual result
* Security impact

---

# A02 — Cryptographic Failures

## Objective

Identify weaknesses involving the protection of sensitive information.

## Test Areas

Review:

* HTTPS usage
* Sensitive data transmission
* Sensitive data exposure
* Password protection
* Session token exposure
* Sensitive information in URLs
* Client-side storage of sensitive data

## Testing Questions

Ask:

* Is sensitive information protected during transmission?
* Is sensitive data unnecessarily exposed?
* Are secrets present in URLs or client-side code?
* Are sensitive responses cached inappropriately?

## Evidence

Document:

* Affected data
* Location of exposure
* Security impact
* Relevant application behavior

Avoid unnecessarily reproducing sensitive information in reports.

---

# A03 — Injection

## Objective

Identify situations where untrusted input may influence commands, queries,
or interpreters.

## Relevant Categories

Consider:

* SQL-related injection
* NoSQL-related injection
* Command injection
* LDAP-related injection
* Template injection

## Testing Approach

1. Identify application inputs.
2. Determine where input is processed.
3. Identify relevant backend technologies where possible.
4. Use controlled validation techniques.
5. Confirm actual security impact before reporting a finding.

## Testing Questions

Ask:

* Is user input safely handled?
* Are queries properly parameterized?
* Are dangerous interpreters exposed to untrusted input?
* Is server-side validation present?

Do not classify unusual error messages alone as confirmed injection
vulnerabilities.

---

# A04 — Insecure Design

## Objective

Identify security weaknesses resulting from missing or insufficient security
controls in application design.

## Test Areas

Evaluate:

* Business logic
* Sensitive workflows
* Abuse cases
* Rate limiting
* Workflow bypass
* Transaction integrity
* Security control assumptions

## Testing Questions

Ask:

* Can a workflow be performed out of sequence?
* Can security checks be bypassed through unexpected application states?
* Are abuse scenarios considered?
* Are sensitive operations protected appropriately?

---

# A05 — Security Misconfiguration

## Objective

Identify insecure application, server, or framework configuration.

## Test Areas

Review:

* Debug functionality
* Error handling
* Default configurations
* Security headers
* Administrative interfaces
* Unnecessary functionality
* Directory exposure

## Testing Questions

Ask:

* Is debug functionality exposed?
* Do error messages reveal unnecessary information?
* Are security headers appropriately configured?
* Are unnecessary services or features accessible?
* Are administrative interfaces sufficiently protected?

---

# A06 — Vulnerable and Outdated Components

## Objective

Identify security risks associated with application dependencies and
components.

## Test Areas

Identify where possible:

* Frameworks
* Libraries
* JavaScript dependencies
* Server software
* Third-party components

## Testing Process

1. Identify the component.
2. Identify the version where possible.
3. Determine whether known security advisories are relevant.
4. Assess whether the vulnerable functionality is actually present.
5. Document realistic impact.

Do not report a vulnerability solely because a component name appears in an
application.

---

# A07 — Identification and Authentication Failures

## Objective

Evaluate authentication and identity management controls.

## Test Areas

Review:

* Login functionality
* Account recovery
* Password reset
* Multi-factor authentication
* Session management
* Authentication rate limiting
* Account enumeration risks

## Testing Questions

Ask:

* Are authentication failures handled securely?
* Are sessions protected appropriately?
* Are authentication controls consistently enforced?
* Can account recovery be abused?
* Are brute-force protections appropriate?

---

# A08 — Software and Data Integrity Failures

## Objective

Identify weaknesses involving trust in software, updates, dependencies, or
data integrity.

## Test Areas

Evaluate:

* Dependency integrity
* Update mechanisms
* Third-party code
* CI/CD assumptions
* Data integrity controls

## Testing Questions

Ask:

* Are external components trusted without appropriate verification?
* Are updates verified appropriately?
* Can untrusted data influence sensitive application processes?

---

# A09 — Security Logging and Monitoring Failures

## Objective

Determine whether important security events can be detected and investigated.

## Test Areas

Evaluate:

* Authentication events
* Authorization failures
* Administrative actions
* Sensitive operations
* Error monitoring
* Alerting processes where in scope

## Testing Questions

Ask:

* Are important security events recorded?
* Is enough context captured for investigation?
* Are security events distinguishable from normal events?
* Are sensitive values unnecessarily stored in logs?

---

# A10 — Server-Side Request Forgery

## Objective

Identify functionality where the server retrieves or communicates with
resources based on user-controlled input.

## Potential Features

Examples include:

* Webhooks
* URL imports
* Image retrieval
* Link previews
* External integrations
* Remote document retrieval

## Testing Questions

Ask:

* Can users influence server-side destinations?
* Are destination restrictions implemented?
* Are unexpected network locations appropriately blocked?
* Is user input validated before server-side retrieval?

---

# Authentication Testing

Perform authentication testing alongside relevant OWASP categories.

Evaluate:

* Login controls
* Account enumeration
* Password recovery
* Session handling
* Logout behavior
* Multi-factor authentication
* Authentication consistency

---

# Authorization Testing

Perform authorization testing across all sensitive functionality.

Evaluate:

* Horizontal authorization
* Vertical authorization
* Object-level authorization
* Administrative access
* API-backed functionality

Authorization must be enforced server-side.

---

# Business Logic Testing

Analyze important application workflows.

Examples:

* Registration
* Payments
* Approval processes
* Account management
* Role changes
* Discounts
* Transactions

Ask whether users can:

* Skip required steps
* Repeat restricted actions
* Manipulate workflow state
* Abuse application assumptions

---

# Coverage Matrix

At the end of testing, produce a coverage matrix.

| Category                      | Status                        | Notes |
| ----------------------------- | ----------------------------- | ----- |
| A01 Broken Access Control     | Not Tested / Partial / Tested |       |
| A02 Cryptographic Failures    | Not Tested / Partial / Tested |       |
| A03 Injection                 | Not Tested / Partial / Tested |       |
| A04 Insecure Design           | Not Tested / Partial / Tested |       |
| A05 Security Misconfiguration | Not Tested / Partial / Tested |       |
| A06 Vulnerable Components     | Not Tested / Partial / Tested |       |
| A07 Authentication Failures   | Not Tested / Partial / Tested |       |
| A08 Software/Data Integrity   | Not Tested / Partial / Tested |       |
| A09 Logging/Monitoring        | Not Tested / Partial / Tested |       |
| A10 SSRF                      | Not Tested / Partial / Tested |       |

---

# Module Output

When this module is used, provide:

1. Web Application Scope
2. Attack Surface Summary
3. OWASP Top 10 Coverage
4. Confirmed Findings
5. Potential Findings
6. Informational Observations
7. Risk Summary
8. Recommendations
9. Testing Limitations

Clearly distinguish confirmed vulnerabilities from areas requiring additional
validation.

