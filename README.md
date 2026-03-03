# The No-Tracking Web Declaration (draft)
Version 0.1.0

---

## Preamble (Non-Normative)

Most modern websites display a “cookie banner” asking for consent.  

These banners usually appear because the site uses technologies that track users across sessions or across different websites, for example for advertising, marketing, or behavioral analytics.

However, not all cookies are the same.

Originally, cookies were introduced simply to allow websites to function properly, for example to keep a user logged in or to remember temporary state during a visit. These are called *session cookies*, and they disappear when the browser is closed.

Over time, cookies and similar technologies began to be used for persistent identification and cross-site tracking. In response, legal frameworks such as the European Union’s ePrivacy Directive and the General Data Protection Regulation (GDPR) introduced rules requiring user consent for non-essential tracking.

This Declaration describes a different approach:

- Use only what is technically necessary.
- Avoid persistent identifiers.
- Avoid tracking.
- Avoid third-party tracking infrastructure.
- Avoid consent banners by design, not by omission.

A website that complies with this Declaration uses only essential session cookies and minimal server logs for operational purposes. It does not track users across sessions or websites.

This document defines clear technical criteria for that approach.

## 1. Purpose

The Hypertext Transfer Protocol (HTTP) is stateless. Cookies were introduced to enable session continuity, authentication, and basic state management.

Over time, persistent client-side identifiers and third-party resources enabled cross-site tracking and behavioral profiling. Regulatory frameworks such as the ePrivacy Directive and the General Data Protection Regulation (GDPR) established rules governing the use of non-essential cookies and personal data processing.

As a result, many websites deploy consent banners in order to use tracking technologies.

This Declaration defines a minimal web architecture in which:

- no tracking technologies are used,
- no persistent client identifiers are stored,
- and no consent banner is required because no consent-triggering mechanisms are present.

It provides clear, technical criteria that websites may voluntarily adopt and reference.

## 2. Scope

This Declaration applies to publicly accessible websites and web applications that wish to:

- avoid tracking-based architectures,
- avoid persistent client-side identifiers,
- minimize personal data processing,
- eliminate the need for cookie consent banners.

Compliance is self-declared unless otherwise specified.

## 3. Definitions

**Session Cookie**  
A first-party cookie that:
- contains a random session identifier,
- is required for session continuity or authentication,
- expires at the end of the browser session,
- is not repurposed for tracking.

**Persistent Cookie**  
A cookie stored beyond the current browser session.

**First-Party Resource**  
A resource served from the same domain as the website being visited.

**Third-Party Resource**  
A resource served from a different domain that may set or access identifiers.

**Tracking**  
The creation, storage, or reuse of identifiers for the purpose of recognizing a user across sessions, websites, or contexts.

**Cross-Site Tracking**  
Recognition of a user across multiple distinct domains or services.

**Fingerprinting**  
Any technique that derives a probabilistic or unique identifier from device, browser, or network characteristics without explicit user action.

**Server Logs**  
Automatically generated records containing request metadata such as IP address, timestamp, requested URL, referrer, and user agent.

## 4. Core Compliance Requirements

A website complying with this Declaration MUST satisfy all of the following:

### 4.1 Cookies and Client Storage

1. Only first-party session cookies may be used.
2. No persistent cookies may be set.
3. No localStorage, sessionStorage, IndexedDB, or similar mechanisms may be used to create persistent identifiers.
4. Session cookies must not be repurposed for tracking or profiling.

### 4.2 Third-Party Resources

5. No third-party resources may set cookies or identifiers.
6. No third-party tracking scripts, advertising pixels, or marketing tags may be included.
7. Embedded content (e.g., video, fonts, widgets) must not introduce tracking mechanisms.

### 4.3 Tracking and Identification

8. No cross-site tracking mechanisms may be implemented.
9. No fingerprinting techniques may be used.
10. No behavioral profiling may be conducted.

### 4.4 Server Logs

11. Server logs may be collected only for:
    - security,
    - debugging,
    - fraud prevention,
    - abuse mitigation.
12. Logs must not be enriched with external datasets for profiling.
13. A retention period must be defined and documented.
14. Logs must not be used to construct behavioral analytics profiles of identifiable individuals.

### 4.5 Analytics

15. If analytics are used, they must:
    - not rely on persistent identifiers,
    - not track users across sessions,
    - not involve third-party tracking infrastructure,
    - not require consent under applicable law.

If these conditions cannot be met, analytics must be omitted.

## 5. Legal Positioning

This Declaration reflects a technical architecture designed to avoid consent-triggering technologies under the ePrivacy Directive.

Processing of strictly necessary session cookies and limited server logs may rely on legitimate interest under the General Data Protection Regulation (GDPR), provided proportionality and data minimization principles are respected.

This document does not constitute legal advice. Each operator remains responsible for compliance with applicable laws in their jurisdiction.

## 6. What a Compliant Website Does Not Do

A compliant website:

- does not deploy advertising trackers,
- does not use marketing pixels,
- does not conduct behavioral profiling,
- does not use persistent identifiers,
- does not perform hidden fingerprinting,
- does not share user identifiers with third parties.

## 7. Transparency Requirements

A compliant website SHOULD publish a privacy notice explaining:
   - the exclusive use of session cookies,
   - the absence of tracking,
   - the purpose and retention of server logs.

It may include a reference to this Declaration, including version number.

Example statement:

> This website complies with the No-Tracking Web Declaration v1.0.  
> It uses only essential session cookies and does not employ tracking technologies.

## 8. Versioning

This Declaration follows semantic versioning:

- Major versions introduce breaking requirement changes.
- Minor versions clarify or refine requirements.
- Patch versions correct wording without altering requirements.

## 9. Licence

This Declaration is released under the Creative Commons Zero 1.0 Universal (CC0 1.0) Public Domain Dedication.

To the fullest extent permitted by law, the author(s) have dedicated this work to the public domain. Anyone may:

- copy,
- modify,
- distribute,
- fork,
- republish,
- incorporate into other documents,
- or use for any purpose,

without permission, attribution, or restriction.

No endorsement by the original author(s) should be inferred from use of this Declaration.

Websites referencing this Declaration may indicate the version number they rely upon (e.g., “No-Tracking Web Declaration v1.0”).

## 10. Rationale

The objective of this Declaration is not to prohibit cookies as a technology. Cookies were originally introduced for legitimate technical purposes.

Rather, this document defines a minimal and privacy-respecting architecture in which:

- user tracking is absent by design,
- data collection is reduced to operational necessity,
- consent banners are unnecessary because no consent-requiring technologies are deployed.

It encourages clarity, proportionality, and architectural restraint in web development.
