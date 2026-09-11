# Example: Web Application Security Assessment

## Scenario

An organization wants to perform an authorized security assessment of a web
application hosted in a staging environment.

## User Request

```text
Perform an authorized security assessment of this web application.

Target:
https://staging.example.com

Environment:
Staging

Scope:
- Web application
- Authenticated functionality
- User and administrator roles

Restrictions:
- No denial-of-service testing
- No destructive testing
- Do not test third-party services
```

---

# Expected AppSec Sentinel Workflow

## 1. Scope Confirmation

AppSec Sentinel should identify:

* Target: `https://staging.example.com`
* Environment: Staging
* Target Type: Web Application
* Authentication: Required
* Available Roles: User and Administrator

---

## 2. Attack Surface Mapping

Identify relevant application areas such as:

* Authentication
* User profiles
* Administrative functionality
* File uploads
* Forms and input fields
* Backend APIs

---

## 3. Testing Methodology

Apply:

* OWASP Top 10
* Authentication testing
* Authorization testing
* Business logic testing
* Session management testing

---

## 4. Testing Coverage

Track:

* Tested categories
* Partially tested categories
* Untested categories

---

## 5. Finding Validation

Potential findings must be classified as:

* Confirmed
* Potential
* Informational
* False Positive

---

## Expected Output

The final assessment should include:

1. Executive Summary
2. Scope
3. Attack Surface
4. OWASP Coverage Matrix
5. Confirmed Findings
6. Potential Findings
7. Risk Summary
8. Recommendations
9. Testing Limitations
10. Final Security Posture

