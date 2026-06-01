# Stolen Device Protection — iOS 17.3+

> Last Updated: 2026-06-01

## Overview

**Stolen Device Protection** is an iOS security feature introduced in **iOS 17.3** (January 2024) that adds biometric authentication requirements — with no passcode fallback — for certain sensitive actions when your iPhone is in an unfamiliar location. For some critical security changes, a mandatory **one-hour waiting period** is also imposed.

This feature was designed in response to a documented attack pattern where thieves observe iPhone owners entering their passcode in public (shoulder surfing), steal the device, and then use the passcode to take over the Apple ID, disable Find My, and drain financial accounts before the victim can respond.

*Reference: https://support.apple.com/en-us/120340*

---

## The Attack Pattern This Addresses

The Wall Street Journal reported in 2023 on a series of iPhone thefts enabled by passcode observation. The attack chain was:

1. Thief observes victim entering passcode (over-the-shoulder in bar, cafe, public transport)
2. Thief steals the iPhone (pickpocket, snatch)
3. Using the observed passcode, thief:
   - Changes Apple ID password (Settings > Apple ID > Password & Security)
   - Disables Find My, preventing remote tracking
   - Adds their own face/fingerprint as biometrics, locking out the victim
   - Accesses saved passwords in iCloud Keychain
   - Transfers money from banking apps
   - Requests trusted device code sent to the stolen phone (completing Apple ID account takeover)

Stolen Device Protection breaks multiple steps in this chain by requiring biometric authentication that a thief does not possess.

---

## How It Works

### Biometric-Only Actions (No Passcode Fallback)

When Stolen Device Protection is enabled and the iPhone is in an **unfamiliar location**, the following actions require **Face ID or Touch ID** with no passcode alternative:

| Protected Action | Why It Matters |
|---|---|
| View/use stored passwords in iCloud Keychain | Prevents credential theft |
| Use saved payment methods (non-Apple Pay) | Prevents financial access |
| Apply for a new Apple Card | Prevents fraud |
| View Apple Card virtual card number | Prevents card fraud |
| Turn off Lost Mode | Prevents thief from canceling tracking |
| Erase All Content and Settings | Prevents device wipe to bypass tracking |
| Use iPhone to reset Apple ID password on new device | Prevents account takeover |
| Create or access Recovery Key | Prevents permanent account lockout of victim |
| Change trusted phone number | Prevents account recovery mechanism change |

### Security Delay (One-Hour Wait)

For the most critical account security changes, a mandatory **one-hour wait period** is imposed, followed by a second Face ID or Touch ID confirmation:

| Action Subject to Delay | Why the Delay Matters |
|---|---|
| Change Apple ID password | Buys time for victim to respond and remotely lock the device |
| Sign out of Apple ID | Prevents immediate account disconnection |
| Update Apple Account security settings | Prevents rapid account lockdown against the victim |
| Add or remove recovery keys | Preserves account recovery options for victim |
| Add or remove trusted phone numbers | Prevents changing account recovery mechanisms |
| Change iPhone passcode | Prevents locking the victim out of their own device |
| Change Face ID or Touch ID | Prevents attacker from enrolling their own biometrics |
| Turn off Find My | Preserves victim's ability to track and remotely erase |
| Turn off Stolen Device Protection itself | Self-protection |

The one-hour delay means that even if a thief has biometrics (e.g., in a coerced scenario), the victim has at least one hour to use another Apple device to lock or erase the stolen iPhone via Find My.

---

## Requirements

To enable Stolen Device Protection, the following must already be configured:

- [ ] iPhone is running **iOS 17.3 or later**
- [ ] **Two-factor authentication** is enabled for Apple ID
- [ ] **Device passcode** is configured
- [ ] **Face ID or Touch ID** is enrolled
- [ ] **Find My** is turned on
- [ ] **Significant Locations** (Location Services) is enabled
  - Go to: Settings > Privacy & Security > Location Services > System Services > Significant Locations

> **⚠️ WARNING:** Significant Locations must be enabled for the feature to determine "familiar" vs. "unfamiliar" locations. This data is stored encrypted on-device and not shared with Apple.

---

## How to Enable Stolen Device Protection

1. Open **Settings**
2. Tap **Face ID & Passcode** (or **Touch ID & Passcode**)
3. Enter your device passcode
4. Scroll down to **Stolen Device Protection**
5. Tap **Turn On Protection**

![Stolen Device Protection Settings](../images/ios-stolen-device-protection.png)
*Figure 1: Stolen Device Protection toggle in Settings > Face ID & Passcode*

---

## Familiar vs. Unfamiliar Locations

### How Familiar Locations Are Determined

iOS uses **Significant Locations** (under Location Services > System Services) to learn frequently visited places:
- Your home address
- Your workplace
- Places you visit regularly

This data is processed on-device using machine learning and is never sent to Apple's servers.

### When Protections Apply

| Location | Biometric Requirement | Security Delay |
|---|---|---|
| Familiar location (home, work) | Passcode allowed as fallback | Not imposed |
| Unfamiliar location (all other places) | Biometrics required, no passcode fallback | Imposed for critical changes |

---

## Comparison: iOS vs. Android Anti-Theft Biometric Protection

| Feature | Stolen Device Protection (iOS 17.3+) | Identity Check (Android 15+) |
|---|---|---|
| Biometric-only sensitive actions | Yes | Yes |
| No passcode fallback away from home | Yes | Yes |
| One-hour security delay | Yes | No (as of 2025) |
| Requires Significant Locations | Yes | Yes (trusted locations) |
| Requires Find My / Find Hub enabled | Yes | Yes |
| Available on all devices | iOS 17.3+, all supported iPhones | Android 15, Pixel + Samsung |

---

## Limitations

| Consideration | Details |
|---|---|
| **Coercion scenarios** | Does not protect against physical coercion ("unlock with your face") |
| **Familiar location accuracy** | In early use, Significant Locations may not have learned all familiar places |
| **One-hour delay inconvenience** | If you are at an unfamiliar location and legitimately need to change these settings, you must wait an hour |
| **Lockdown Mode compatibility** | Lockdown Mode (iOS 16+) provides separate extreme hardening; both can be used together |

---

## Checklist: Stolen Device Protection Configuration

- [ ] iOS 17.3 or later installed
- [ ] Stolen Device Protection: **Enabled** (Settings > Face ID & Passcode > Stolen Device Protection)
- [ ] Face ID / Touch ID: **Enrolled**
- [ ] Find My: **Enabled**
- [ ] Significant Locations: **Enabled** (Settings > Privacy & Security > Location Services > System Services > Significant Locations)
- [ ] Two-factor authentication on Apple ID: **Enabled**

---

## Related Documents

- [Find My](find-my.md)
- [Lost Mode](lost-mode.md)
- [Activation Lock](activation-lock.md)
- [Apple ID Recovery](apple-id-recovery.md)
- [iOS Hardening Guide](../hardening/ios-hardening.md)
- [Android Identity Check (comparison)](../android/identity-check.md)

---

*Last Updated: 2026-06-01 | Source: https://support.apple.com/en-us/120340*
