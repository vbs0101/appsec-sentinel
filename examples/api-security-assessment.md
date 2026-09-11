# Example: API Security Assessment

## Scenario

An organization wants to perform an authorized security assessment of a REST
API in a staging environment.

## User Request

```text
Perform an authorized security assessment of this API.

Target:
https://api-staging.example.com

Environment:
Staging

Authentication:
Bearer token authentication

Scope:
- REST API
- Authenticated endpoints
- Standard user and administrator roles

Restrictions:
- No denial-of-service testing
- No destructive testing
- Respect application rate limits
```

---

# Expected AppSec Sentinel Workflow

## 1. Scope Confirmation

Identify:

* API Base URL
* Environment
* Authentication method
* API versions
* User roles
* Testing restrictions

---

## 2. API Inventory

Identify:

* Endpoints
* HTTP methods
* Parameters
* Request bodies
* Object identifiers
* Sensitive functions

---

## 3. Testing Methodology

Apply:

* OWASP API Security Top 10
* Authentication testing
* Object-level authorization testing
* Property-level authorization testing
* Function-level authorization testing

---

## 4. Finding Validation

Validate:

* Reproducibility
* Security impact
* Evidence

Do not classify scanner output alone as a confirmed vulnerability.

---

## Expected Output

The final assessment should include:

1. API Scope
2. API Inventory
3. Authentication Summary
4. Authorization Summary
5. OWASP API Coverage
6. Confirmed Findings
7. Potential Findings
8. Risk Summary
9. Recommendations
10. Testing Limitations

