# Android Security & Loss Response

> Last Updated: 2026-06-01

## Overview

This section covers Android-specific security features, configurations, and loss response procedures. Android is the world's most widely deployed mobile operating system, running on devices from Google, Samsung, Motorola, OnePlus, and hundreds of other manufacturers.

---

## Android Security Architecture

Android's security model is built around several interlocking layers:

```
┌──────────────────────────────────────────────────────────┐
│                    USER DATA LAYER                       │
│        Apps, Files, Credentials, Backups                 │
├──────────────────────────────────────────────────────────┤
│                  APPLICATION LAYER                       │
│       Play Store, Sideloaded Apps, MDM Apps              │
├──────────────────────────────────────────────────────────┤
│                GOOGLE SERVICES LAYER                     │
│    Play Protect, Find Hub, Google Account, Identity Check│
├──────────────────────────────────────────────────────────┤
│               ANDROID OS LAYER                           │
│   SELinux, Verified Boot, Encryption, Keystore           │
├──────────────────────────────────────────────────────────┤
│                HARDWARE LAYER                            │
│   Titan M / StrongBox, Secure Enclave, TrustZone        │
└──────────────────────────────────────────────────────────┘
```

---

## Section Contents

| Document | Description |
|---|---|
| [Find Hub (formerly Find My Device)](find-my-device.md) | Tracking, locking, and remotely wiping your Android device |
| [Factory Reset Protection (FRP)](factory-reset-protection.md) | How FRP prevents thieves from wiping and reusing your device |
| [Google Account Security](google-account-security.md) | Securing the Google Account that controls your device |
| [Play Protect](play-protect.md) | Google's on-device malware scanning service |
| [Identity Check](identity-check.md) | Android 15+ biometric lock for sensitive settings outside trusted locations |

---

## Anti-Theft Features at a Glance (Android 10–15+)

| Feature | Android Version | Description |
|---|---|---|
| Factory Reset Protection | 5.1+ | Requires Google account after unauthorized reset |
| Find Hub (Find My Device) | All (via Play Services) | Remote tracking, lock, and wipe |
| Smart Lock | 5.0+ | Trusted places/devices relax screen lock |
| Theft Detection Lock | 10+ | AI detects snatch theft, auto-locks screen |
| Offline Device Lock | 10+ | Auto-locks if device goes offline after theft |
| Remote Lock (without internet) | 10+ | Lock via SMS or cached credentials |
| Identity Check | 15+ (Pixel, Samsung) | Biometric-only access to settings away from trusted location |

---

## Version Support Notes

> **⚠️ WARNING:** Devices running Android 9 or earlier no longer receive security updates from Google. If your device cannot be updated to at least Android 12, consider replacing it. Without security updates, vulnerabilities remain unpatched indefinitely.

- **Android 15+**: Identity Check, enhanced theft protection
- **Android 12+**: Approximate location permissions, Privacy Dashboard
- **Android 10+**: Scoped Storage, enhanced permissions, Theft Detection Lock
- **Android 9 (Pie)**: End of Google security support

---

## Quick Actions for Lost Android Device

1. Go to **https://myaccount.google.com/find-your-phone** or use Find Hub app on another device
2. Select your device
3. Choose **Secure Device** to lock with PIN and display message
4. If recovery is unlikely: choose **Erase Device**

For step-by-step instructions, see [First 5 Minutes](../incident-response/first-5-minutes.md).

---

## Related Sections

- [Android Hardening Guide](../hardening/android-hardening.md)
- [Android Hardening Checklist](../checklists/android-hardening-checklist.md)
- [SIM Security](../hardening/sim-security.md)

---

*Last Updated: 2026-06-01 | References: https://support.google.com/android, https://security.googleblog.com*
