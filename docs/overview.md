# Overview

> Last Updated: 2026-06-01

## Purpose

This document provides an introduction to the Mobile Device Loss & Theft Response Playbook — a comprehensive, open-source reference for individuals, security professionals, IT administrators, and corporate teams dealing with lost or stolen smartphones.

Smartphones are no longer just communication devices. They are credential vaults, payment terminals, identity documents, and access keys to corporate systems. The loss of a smartphone — whether accidental or through theft — represents a multi-dimensional security incident that demands structured, time-sensitive response.

---

## Scope

This playbook covers:

- **Devices in scope**: Android smartphones (Android 10 and later), iPhones (iOS 15 and later)
- **User types in scope**: Personal users, bring-your-own-device (BYOD) employees, corporate-managed device users
- **Scenarios in scope**: Accidental loss, opportunistic theft, targeted theft, device seizure, SIM swap attacks
- **Out of scope**: Tablet-only incidents (though much guidance applies), jailbroken/rooted devices in enterprise context

---

## How to Read This Playbook

```
┌───────────────────────────────────────────────────────────────────────────┐
│                     MOBILE DEVICE LOSS PLAYBOOK                           │
├──────────────────┬──────────────────────────┬─────────────────────────────┤
│   BEFORE LOSS    │     DURING INCIDENT      │       AFTER LOSS            │
│                  │                          │                             │
│  Checklists/     │  incident-response/      │  incident-response/         │
│  before-loss     │  first-5-minutes.md      │  first-24-hours.md          │
│  android/        │  first-30-minutes.md     │  first-week.md              │
│  ios/            │  first-hour.md           │  templates/                 │
│  hardening/      │                          │                             │
└──────────────────┴──────────────────────────┴─────────────────────────────┘
```

### If Your Device Was Just Lost or Stolen

Go directly to [Emergency Checklist](../checklists/emergency-checklist.md) or [First 5 Minutes](../incident-response/first-5-minutes.md).

### If You Want to Prevent Future Loss

Read [Before Loss Prevention](../checklists/before-loss-prevention.md), then the platform-specific hardening guide for [Android](../hardening/android-hardening.md) or [iOS](../hardening/ios-hardening.md).

### If You Are Responding to a Corporate Device Incident

See [Corporate Device Response](../incident-response/corporate-device-response.md) and [MDM Enterprise](../hardening/mdm-enterprise.md).

### If You Are a Security Researcher or Forensics Practitioner

See [Threat Landscape](threat-landscape.md), [Attack Scenarios](../threat-models/attack-scenarios.md), and [Recommended Tools](../tools/recommended-tools.md).

---

## Key Concepts

### The Two Phases of Device Security

**Pre-incident hardening** is the most effective mitigation. A properly hardened device — with a strong PIN, biometric authentication, Find My enabled, SIM PIN set, and 2FA on all accounts — dramatically reduces the risk and impact of theft.

**Post-incident response** is time-critical. The first 5–30 minutes after a loss event are the most important window for containment. Delayed response exponentially increases the chance of unauthorized account access, financial fraud, and data exfiltration.

### Platform Differences

Android and iOS take different architectural approaches to device security:

| Feature | Android | iOS |
|---|---|---|
| Device tracking | Find Hub (Google) | Find My (Apple) |
| Remote lock | Find Hub / Theft Protection | Find My / Lost Mode |
| Remote wipe | Find Hub | Find My |
| Anti-theft AI | Theft Detection Lock (Android 10+) | Stolen Device Protection (iOS 17.3+) |
| Account protection | Google Account security | Apple ID security |
| Activation lock | Factory Reset Protection (FRP) | Activation Lock |
| Biometric fallback block | Identity Check (Android 15+) | Stolen Device Protection |

---

## Reference Standards

This playbook references:

- **NIST SP 800-124r2** — Guidelines for Managing the Security of Mobile Devices in the Enterprise (2023)
- **OWASP MASTG** — Mobile Application Security Testing Guide
- **OWASP MASVS** — Mobile Application Security Verification Standard
- **CISA** — Mobile Device Security guidance and alerts
- **ENISA** — Smartphone Security Recommendations
- **MITRE ATT&CK Mobile Matrix** — Threat technique library

See [Citations](../references/citations.md) for full references.

---

*Last Updated: 2026-06-01*
