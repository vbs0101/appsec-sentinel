# Web Application Security Testing Checklist

## Assessment Preparation

* [ ] Authorization confirmed
* [ ] Scope defined
* [ ] Target URLs identified
* [ ] Environment identified
* [ ] Test accounts available
* [ ] User roles identified
* [ ] Testing restrictions documented

---

# Discovery and Attack Surface

* [ ] Application functionality mapped
* [ ] Authentication mechanisms identified
* [ ] Authorization model identified
* [ ] User roles identified
* [ ] Input points identified
* [ ] File upload functionality identified
* [ ] Administrative functionality identified
* [ ] Sensitive workflows identified
* [ ] Third-party integrations identified

---

# A01 — Broken Access Control

* [ ] Horizontal authorization evaluated
* [ ] Vertical authorization evaluated
* [ ] Object-level authorization evaluated
* [ ] Direct object references reviewed
* [ ] Forced browsing considered
* [ ] Administrative functionality tested
* [ ] Server-side authorization enforcement verified

---

# A02 — Cryptographic Failures

* [ ] HTTPS usage reviewed
* [ ] Sensitive data transmission reviewed
* [ ] Sensitive data exposure reviewed
* [ ] Sensitive information in URLs reviewed
* [ ] Client-side sensitive data storage reviewed
* [ ] Sensitive caching behavior considered

---

# A03 — Injection

* [ ] Input points identified
* [ ] Server-side validation reviewed
* [ ] Relevant query handling evaluated
* [ ] SQL-related injection risks assessed
* [ ] NoSQL-related injection risks assessed
* [ ] Command execution risks assessed
* [ ] Template processing risks assessed

---

# A04 — Insecure Design

* [ ] Sensitive workflows identified
* [ ] Business logic reviewed
* [ ] Workflow bypass scenarios considered
* [ ] Abuse cases considered
* [ ] Rate controls reviewed
* [ ] Transaction integrity considered

---

# A05 — Security Misconfiguration

* [ ] Error handling reviewed
* [ ] Debug functionality reviewed
* [ ] Security headers reviewed
* [ ] Default configurations reviewed
* [ ] Administrative interfaces reviewed
* [ ] Unnecessary functionality identified
* [ ] Directory exposure considered

---

# A06 — Vulnerable and Outdated Components

* [ ] Frameworks identified
* [ ] Libraries identified
* [ ] Client-side dependencies identified
* [ ] Server components identified
* [ ] Relevant versions documented
* [ ] Relevant security advisories considered

---

# A07 — Identification and Authentication Failures

* [ ] Login functionality reviewed
* [ ] Account enumeration considered
* [ ] Password recovery reviewed
* [ ] Session management reviewed
* [ ] Session expiration reviewed
* [ ] Logout behavior reviewed
* [ ] Multi-factor authentication reviewed
* [ ] Authentication rate controls considered

---

# A08 — Software and Data Integrity Failures

* [ ] Third-party dependencies reviewed
* [ ] Dependency integrity considered
* [ ] Update mechanisms reviewed
* [ ] Trust boundaries identified
* [ ] Data integrity controls considered

---

# A09 — Security Logging and Monitoring Failures

* [ ] Authentication events reviewed
* [ ] Authorization failures reviewed
* [ ] Administrative actions reviewed
* [ ] Sensitive actions reviewed
* [ ] Security event logging considered
* [ ] Sensitive data in logs considered

---

# A10 — Server-Side Request Forgery

* [ ] URL-based functionality identified
* [ ] Webhooks identified
* [ ] Remote resource retrieval identified
* [ ] External integrations reviewed
* [ ] Destination validation considered

---

# Final Validation

* [ ] Findings validated
* [ ] False positives removed
* [ ] Evidence collected
* [ ] Risk ratings assigned
* [ ] Coverage matrix completed
* [ ] Testing limitations documented
* [ ] Final report completed

