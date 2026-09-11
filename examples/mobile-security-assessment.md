# Example: Mobile Application Security Assessment

## Scenario

An organization wants to perform an authorized security assessment of a mobile
application.

## User Request

```text
Perform an authorized security assessment of this Android application.

Application:
company-app.apk

Platform:
Android

Scope:
- Static analysis
- Dynamic analysis
- Authentication testing
- Local storage testing
- Network security testing

Restrictions:
- No destructive testing
- Backend systems are tested separately
```

---

# Expected AppSec Sentinel Workflow

## 1. Scope Confirmation

Identify:

* Application name
* Platform
* Application version
* Package identifier
* Testing scope
* Restrictions

---

## 2. Mobile Attack Surface Mapping

Identify:

* Authentication
* Local storage
* Network communication
* Deep links
* WebViews
* Permissions
* Third-party SDKs

---

## 3. Testing Methodology

Apply relevant OWASP MASVS-aligned testing principles.

Evaluate:

* Secure storage
* Authentication
* Network security
* Platform interaction
* Application configuration
* Code security

---

## 4. Finding Validation

For every potential issue:

* Confirm reproducibility
* Determine realistic impact
* Collect evidence

Classify as:

* Confirmed
* Potential
* Informational
* False Positive

---

## Expected Output

The final assessment should include:

1. Application Scope
2. Platform Information
3. Mobile Attack Surface
4. Testing Methodology
5. MASVS Coverage
6. Confirmed Findings
7. Potential Findings
8. Risk Summary
9. Recommendations
10. Testing Limitations

