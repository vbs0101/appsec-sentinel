# API Security Testing Checklist

## Assessment Preparation

* [ ] Authorization confirmed
* [ ] API scope defined
* [ ] Base URLs identified
* [ ] API versions identified
* [ ] Documentation reviewed
* [ ] Authentication mechanisms identified
* [ ] Test accounts available
* [ ] User roles identified
* [ ] Testing restrictions documented

---

# API Discovery

* [ ] Endpoints identified
* [ ] HTTP methods identified
* [ ] Request parameters identified
* [ ] Request bodies identified
* [ ] Object identifiers identified
* [ ] Authentication requirements identified
* [ ] Authorization requirements identified
* [ ] Administrative endpoints identified
* [ ] Sensitive business functions identified

---

# API1 — Broken Object Level Authorization

* [ ] Object identifiers identified
* [ ] Cross-user access controls evaluated
* [ ] Object ownership validation reviewed
* [ ] Tenant isolation considered
* [ ] Server-side authorization verified

---

# API2 — Broken Authentication

* [ ] Authentication mechanisms reviewed
* [ ] Token validation reviewed
* [ ] Token expiration reviewed
* [ ] Session handling reviewed
* [ ] Sensitive endpoints protected
* [ ] Authentication consistency reviewed

---

# API3 — Broken Object Property Level Authorization

* [ ] Sensitive response properties reviewed
* [ ] Excessive data exposure considered
* [ ] Unauthorized property modification tested
* [ ] Mass assignment risks considered
* [ ] Property-level authorization reviewed

---

# API4 — Unrestricted Resource Consumption

* [ ] Rate limiting reviewed
* [ ] Pagination reviewed
* [ ] Request size controls reviewed
* [ ] Resource-intensive endpoints identified
* [ ] Upload limits reviewed
* [ ] Query complexity considered

---

# API5 — Broken Function Level Authorization

* [ ] Administrative functions identified
* [ ] Privileged functions identified
* [ ] Role restrictions reviewed
* [ ] Server-side authorization verified
* [ ] Sensitive functions tested

---

# API6 — Unrestricted Access to Sensitive Business Flows

* [ ] Sensitive workflows identified
* [ ] Automation abuse considered
* [ ] Rate controls considered
* [ ] Workflow protections reviewed
* [ ] Business abuse scenarios considered

---

# API7 — Server-Side Request Forgery

* [ ] URL parameters identified
* [ ] Webhook functionality reviewed
* [ ] Remote resource functionality reviewed
* [ ] Destination validation considered

---

# API8 — Security Misconfiguration

* [ ] CORS configuration reviewed
* [ ] Error handling reviewed
* [ ] Debug functionality reviewed
* [ ] HTTP methods reviewed
* [ ] Authentication configuration reviewed
* [ ] Security headers reviewed

---

# API9 — Improper Inventory Management

* [ ] API versions reviewed
* [ ] Deprecated endpoints identified
* [ ] Development endpoints considered
* [ ] Test endpoints considered
* [ ] Undocumented endpoints considered

---

# API10 — Unsafe Consumption of APIs

* [ ] Third-party APIs identified
* [ ] External trust boundaries reviewed
* [ ] Third-party response validation considered
* [ ] External authentication reviewed

---

# Final Validation

* [ ] Findings validated
* [ ] False positives removed
* [ ] Evidence collected
* [ ] Risk ratings assigned
* [ ] Coverage matrix completed
* [ ] Testing limitations documented
* [ ] Final report completed

