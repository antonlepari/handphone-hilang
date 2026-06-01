# iOS Security & Loss Response

> Last Updated: 2026-06-01

## Overview

This section covers iOS-specific security features, configurations, and loss response procedures for iPhone. Apple's iOS platform is designed with privacy and security as foundational principles, and it includes several powerful anti-theft features that, when properly configured, make a stolen iPhone significantly less useful to an attacker.

---

## iOS Security Architecture

```
┌──────────────────────────────────────────────────────────────┐
│                      USER DATA LAYER                         │
│          Apps, Photos, Health, Messages, Contacts            │
├──────────────────────────────────────────────────────────────┤
│                   APPLICATION LAYER                          │
│           App Store, iCloud, Third-Party Apps                │
├──────────────────────────────────────────────────────────────┤
│                   APPLE SERVICES LAYER                       │
│   Find My, Stolen Device Protection, Apple ID, iCloud        │
├──────────────────────────────────────────────────────────────┤
│                      iOS LAYER                               │
│   Secure Enclave, Data Protection Classes, Gatekeeper        │
├──────────────────────────────────────────────────────────────┤
│                    HARDWARE LAYER                            │
│   Secure Enclave Processor (SEP), Face ID / Touch ID        │
└──────────────────────────────────────────────────────────────┘
```

---

## Section Contents

| Document | Description |
|---|---|
| [Find My](find-my.md) | Apple's device tracking and recovery platform |
| [Lost Mode](lost-mode.md) | Locking and messaging a lost iPhone |
| [Activation Lock](activation-lock.md) | Preventing unauthorized use after factory reset |
| [Stolen Device Protection](stolen-device-protection.md) | iOS 17.3+ protection against passcode-observed theft |
| [Apple ID Recovery](apple-id-recovery.md) | Regaining account access after loss |

---

## iOS Anti-Theft Features at a Glance

| Feature | iOS Version | Description |
|---|---|---|
| Activation Lock | iOS 7+ | Requires Apple ID after factory reset when Find My is on |
| Find My | iOS 8+ | Track, lock, and erase device remotely |
| Lost Mode | iOS 6+ | Lock device and display contact info |
| Stolen Device Protection | iOS 17.3+ | Biometric-only access; 1-hour delay for critical changes away from familiar locations |
| Lockdown Mode | iOS 16+ | Extreme hardening for high-risk users (journalists, activists) |

---

## Version Support Notes

> **⚠️ WARNING:** Devices that cannot be updated to at least iOS 16 no longer receive security patches. Apple regularly discovers and patches critical vulnerabilities. Running an outdated iOS version leaves you exposed to known exploits.

| Device | Latest Supported iOS |
|---|---|
| iPhone 16 series | iOS 18+ |
| iPhone 15 series | iOS 18+ |
| iPhone 14 series | iOS 18+ |
| iPhone 13 series | iOS 18+ |
| iPhone 12 series | iOS 18+ |
| iPhone 11 series | iOS 18+ |
| iPhone XS / XS Max | iOS 18+ |
| iPhone XR | iOS 18+ |
| iPhone X | iOS 16 (end of support) |
| iPhone 8 / 8 Plus | iOS 16 (end of support) |
| iPhone 7 / 7 Plus | iOS 15 (end of support) |

---

## Quick Actions for Lost iPhone

1. Open **Find My** app on another Apple device, or go to **https://icloud.com/find**
2. Sign in with your Apple ID
3. Select the missing iPhone
4. Tap **Mark as Lost** to enable Lost Mode
5. Add a phone number and message to display on the lock screen
6. If recovery is impossible: tap **Erase This Device**

For step-by-step instructions, see [First 5 Minutes](../incident-response/first-5-minutes.md).

---

## Related Sections

- [iOS Hardening Guide](../hardening/ios-hardening.md)
- [iOS Hardening Checklist](../checklists/ios-hardening-checklist.md)
- [SIM Security](../hardening/sim-security.md)

---

*Last Updated: 2026-06-01 | References: https://support.apple.com | https://developer.apple.com/security*
