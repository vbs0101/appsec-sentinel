# OWASP API Security Top 10 Testing Module

## Purpose

This module provides a structured methodology for assessing authorized APIs
against the OWASP API Security Top 10.

It supports security testing of:

* REST APIs
* JSON APIs
* GraphQL APIs
* HTTP-based backend services

The objective is to identify security weaknesses through structured,
evidence-based testing.

---

# Testing Preparation

Before beginning API testing, identify:

* Base URL
* API versions
* Available documentation
* Authentication mechanisms
* Test accounts
* User roles
* API environments
* Scope limitations
* Rate-limit restrictions

Create an API inventory before beginning detailed testing.

---

# API Attack Surface Mapping

Identify:

* API endpoints
* HTTP methods
* Request parameters
* Request bodies
* Object identifiers
* Authentication mechanisms
* Authorization requirements
* Sensitive functions
* Administrative functions

Example:

| Endpoint           | Method | Authentication | Role   | Sensitivity |
| ------------------ | ------ | -------------- | ------ | ----------- |
| `/api/auth/login`  | POST   | No             | Public | High        |
| `/api/users/{id}`  | GET    | Yes            | User   | High        |
| `/api/users/{id}`  | PUT    | Yes            | User   | High        |
| `/api/admin/users` | GET    | Yes            | Admin  | Critical    |

---

# API1 — Broken Object Level Authorization

## Objective

Verify that users can access only the objects they are authorized to access.

## Test Areas

Evaluate:

* Object identifiers
* User IDs
* Account IDs
* Order IDs
* Document IDs
* File IDs
* Tenant identifiers

## Testing Questions

Ask:

* Can User A access User B's object?
* Is authorization validated for every object request?
* Does the API trust client-provided identifiers?

Document:

* Authenticated user
* Requested object
* Expected result
* Actual result
* Security impact

---

# API2 — Broken Authentication

## Objective

Evaluate weaknesses in API authentication controls.

## Test Areas

Review:

* Authentication mechanisms
* Token validation
* Token expiration
* Token revocation
* Session handling
* Credential protection
* Authentication consistency

## Testing Questions

Ask:

* Are authentication requirements consistently enforced?
* Are expired credentials rejected?
* Are authentication tokens validated correctly?
* Are sensitive endpoints protected?

---

# API3 — Broken Object Property Level Authorization

## Objective

Verify that users cannot read or modify object properties they are not
authorized to access.

## Test Areas

Evaluate:

* Excessive data exposure
* Sensitive response properties
* Unauthorized property modification
* Mass assignment risks

## Testing Questions

Ask:

* Does the API return unnecessary sensitive properties?
* Can restricted properties be modified?
* Are client-provided properties explicitly controlled?

---

# API4 — Unrestricted Resource Consumption

## Objective

Identify insufficient controls that could allow excessive use of API
resources.

## Test Areas

Evaluate:

* Rate limiting
* Pagination
* Request size controls
* Resource-intensive operations
* Upload limits
* Query complexity

Testing must remain within authorized safety limits.

---

# API5 — Broken Function Level Authorization

## Objective

Verify that users can access only functions appropriate for their role.

## Test Areas

Evaluate:

* Administrative endpoints
* Privileged functions
* Sensitive operations
* Role-restricted actions

## Testing Questions

Ask:

* Can a standard user invoke administrative functions?
* Is authorization enforced server-side?
* Can alternate HTTP methods bypass restrictions?

---

# API6 — Unrestricted Access to Sensitive Business Flows

## Objective

Identify sensitive workflows that can be abused because appropriate controls
are missing.

## Examples

Relevant flows may include:

* Registration
* Payments
* Password recovery
* Booking
* Voting
* Promotions
* Account creation

Evaluate whether:

* Automation controls exist
* Rate controls are appropriate
* Workflow abuse is possible

---

# API7 — Server-Side Request Forgery

## Objective

Identify API functionality that allows user-controlled destinations for
server-side requests.

## Potential Areas

Examples:

* Webhooks
* URL imports
* Remote resource retrieval
* External integrations

Evaluate whether destination validation and restrictions are implemented.

---

# API8 — Security Misconfiguration

## Objective

Identify insecure API configuration.

## Test Areas

Evaluate:

* CORS configuration
* HTTP methods
* Error handling
* Debug functionality
* Security headers
* Authentication configuration

---

# API9 — Improper Inventory Management

## Objective

Identify unmanaged, deprecated, or unnecessarily exposed APIs.

## Test Areas

Identify:

* Old API versions
* Deprecated endpoints
* Test environments
* Development endpoints
* Shadow APIs
* Undocumented functionality

Document confirmed exposure and realistic risk.

---

# API10 — Unsafe Consumption of APIs

## Objective

Evaluate how the application consumes data and services from third-party APIs.

## Test Areas

Evaluate:

* Input validation
* Trust boundaries
* Third-party response handling
* Authentication to external APIs
* Data validation

## Testing Questions

Ask:

* Is third-party data trusted without validation?
* Are external responses handled safely?
* Are trust boundaries clearly enforced?

---

# GraphQL Security Considerations

When testing GraphQL APIs, additionally identify:

* Schema exposure
* Authorization controls
* Object-level authorization
* Query complexity controls
* Depth limitations
* Sensitive fields
* Mutation authorization

GraphQL should be tested according to the same security principles as other APIs.

---

# API Authentication Testing

Evaluate:

* Authentication requirements
* Token handling
* Session handling
* Expiration
* Logout behavior
* Credential protection

---

# API Authorization Testing

Test:

* Object-level authorization
* Property-level authorization
* Function-level authorization
* Tenant isolation
* Role separation

Authorization must be enforced server-side.

---

# API Coverage Matrix

At the end of testing, provide:

| Category                                        | Status                        | Notes |
| ----------------------------------------------- | ----------------------------- | ----- |
| API1 Broken Object Level Authorization          | Not Tested / Partial / Tested |       |
| API2 Broken Authentication                      | Not Tested / Partial / Tested |       |
| API3 Broken Object Property Level Authorization | Not Tested / Partial / Tested |       |
| API4 Unrestricted Resource Consumption          | Not Tested / Partial / Tested |       |
| API5 Broken Function Level Authorization        | Not Tested / Partial / Tested |       |
| API6 Sensitive Business Flows                   | Not Tested / Partial / Tested |       |
| API7 SSRF                                       | Not Tested / Partial / Tested |       |
| API8 Security Misconfiguration                  | Not Tested / Partial / Tested |       |
| API9 Improper Inventory Management              | Not Tested / Partial / Tested |       |
| API10 Unsafe Consumption of APIs                | Not Tested / Partial / Tested |       |

---

# Module Output

When this module is used, provide:

1. API Scope
2. API Inventory
3. Authentication Summary
4. Authorization Summary
5. OWASP API Coverage
6. Confirmed Findings
7. Potential Findings
8. Informational Observations
9. Risk Summary
10. Recommendations
11. Testing Limitations

Clearly distinguish confirmed vulnerabilities from potential issues requiring
additional validation.

