# Mobile Application Security Testing Checklist

## Assessment Preparation

* [ ] Authorization confirmed
* [ ] Application identified
* [ ] Platform identified
* [ ] Application version identified
* [ ] Package or bundle identifier identified
* [ ] Scope defined
* [ ] Test accounts available
* [ ] Testing restrictions documented

---

# Attack Surface

* [ ] Authentication mechanisms identified
* [ ] Local storage identified
* [ ] Backend APIs identified
* [ ] Network communication identified
* [ ] Deep links identified
* [ ] URL schemes identified
* [ ] WebViews identified
* [ ] Permissions identified
* [ ] Third-party SDKs identified

---

# Authentication

* [ ] Login functionality reviewed
* [ ] Token storage reviewed
* [ ] Session expiration reviewed
* [ ] Logout behavior reviewed
* [ ] Biometric authentication reviewed
* [ ] Backend authentication enforcement considered

---

# Secure Storage

* [ ] Local databases reviewed
* [ ] Application preferences reviewed
* [ ] Cached data reviewed
* [ ] Application files reviewed
* [ ] Logs reviewed
* [ ] Clipboard usage considered
* [ ] Screenshot exposure considered

---

# Network Security

* [ ] HTTPS enforcement reviewed
* [ ] Cleartext communication considered
* [ ] Certificate validation reviewed
* [ ] TLS configuration reviewed
* [ ] Sensitive data transmission reviewed

---

# Platform Interaction

* [ ] Deep links reviewed
* [ ] URL schemes reviewed
* [ ] Inter-application communication reviewed
* [ ] Exported components reviewed
* [ ] External storage considered

---

# WebView Security

* [ ] WebViews identified
* [ ] JavaScript configuration reviewed
* [ ] URL navigation reviewed
* [ ] Authentication boundaries reviewed
* [ ] Sensitive data exposure considered

---

# Android Security

* [ ] AndroidManifest.xml reviewed
* [ ] Activities reviewed
* [ ] Services reviewed
* [ ] Broadcast receivers reviewed
* [ ] Content providers reviewed
* [ ] Exported components reviewed
* [ ] Backup configuration reviewed
* [ ] Debuggable configuration reviewed
* [ ] Network security configuration reviewed

---

# iOS Security

* [ ] Application Transport Security reviewed
* [ ] Keychain usage reviewed
* [ ] Local storage reviewed
* [ ] URL schemes reviewed
* [ ] Associated domains reviewed
* [ ] Application permissions reviewed

---

# Code and Configuration

* [ ] Hardcoded secrets considered
* [ ] API keys considered
* [ ] Debug functionality reviewed
* [ ] Sensitive logging reviewed
* [ ] Third-party components identified

---

# Final Validation

* [ ] Findings validated
* [ ] False positives removed
* [ ] Evidence collected
* [ ] Risk ratings assigned
* [ ] MASVS coverage completed
* [ ] Testing limitations documented
* [ ] Final report completed

