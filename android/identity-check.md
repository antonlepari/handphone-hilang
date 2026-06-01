# Identity Check — Android

> Last Updated: 2026-06-01

## Overview

**Identity Check** is an Android security feature that requires **biometric authentication** (fingerprint or face scan) — with no passcode or PIN fallback — to access sensitive device settings and data when the device is **outside of trusted locations** (such as your home or office).

Identity Check was introduced by Google in January 2025 and initially rolled out to **Pixel devices running Android 15** and **Samsung Galaxy devices running One UI 7**. Broader Android availability was announced for later in 2025.

> **ℹ️ NOTE:** Identity Check is conceptually similar to Apple's Stolen Device Protection (iOS 17.3+). Both features prevent thieves who have stolen a device along with the observed passcode from making critical security changes.

*Reference: https://support.google.com/pixelphone/answer/9463625*

---

## Why Identity Check Matters

### The Passcode Theft Attack Chain

Before Identity Check, the following attack was possible:

1. Attacker observes victim entering PIN in public (shoulder surfing)
2. Attacker steals the unlocked or locked device
3. Attacker uses the observed PIN to unlock the device
4. Attacker navigates to Settings and changes biometrics to their own face/fingerprint
5. Attacker disables Find My Device
6. Attacker accesses Google Password Manager and exports all credentials
7. Attacker uses credentials to take over email, banking, and other accounts

**Identity Check breaks step 4 and steps 6-7**: outside of trusted locations, the PIN is no longer sufficient — biometrics are required with no fallback. A thief who has the PIN but not the owner's fingerprint or face cannot change security settings or access passwords.

---

## How Identity Check Works

### Trusted Locations

Identity Check uses the device's location to determine context:

- **Trusted locations** (defined by the user): Home, office, or other familiar places where the user regularly uses the device. Relaxed security applies — PIN can be used as normal.
- **Untrusted/unfamiliar locations** (everywhere else): Enhanced security applies — biometrics required for sensitive actions, no passcode fallback.

### What Requires Biometrics Away from Trusted Locations

When Identity Check is enabled and the device is outside trusted locations, **explicit biometric authentication** is required for:

| Protected Action | Details |
|---|---|
| Access saved passwords and passkeys | Google Password Manager content |
| Autofill passwords in apps | From Google Password Manager (except Chrome) |
| Change screen lock PIN or password | Prevents PIN change by attacker |
| Change biometrics (fingerprint/face) | Prevents attacker from enrolling their biometrics |
| Factory reset | Prevents data destruction or bypass attempt |
| Turn off Find My Device | Prevents disabling location tracking |
| Turn off any theft protection features | Includes Identity Check itself |

*Source: The Hacker News, January 2025 — https://thehackernews.com/2025/01/androids-new-identity-check-feature.html*

---

## Requirements

To enable Identity Check:

- [ ] Device: Google Pixel running **Android 15** or Samsung Galaxy running **One UI 7** (broader Android availability in 2025)
- [ ] Play Services: Latest stable version installed
- [ ] Biometrics: Face unlock or fingerprint scanner enrolled on the device
- [ ] Screen lock: PIN, password, or pattern configured
- [ ] Location: Location Services enabled (for trusted location detection)
- [ ] Find My Device: Must be enabled

---

## How to Enable Identity Check (Pixel)

1. Open **Settings**
2. Tap **Security & privacy** or **Security**
3. Tap **More security & privacy**
4. Tap **Identity Check**
5. Toggle **Identity Check** to **On**
6. Follow the prompts to confirm your biometric authentication
7. Optionally: Add trusted locations

### Adding Trusted Locations

1. In the Identity Check settings, tap **Add trusted location**
2. The device will use your current location (ensure GPS is accurate)
3. Name the location (e.g., "Home," "Office")
4. Confirm

> **💡 TIP:** Only add locations where you genuinely use the device regularly and where you have a reasonable expectation of security. Adding too many trusted locations reduces the protection value of the feature.

---

## How to Enable Identity Check (Samsung Galaxy)

Samsung Galaxy devices running **One UI 7** have Identity Check under a slightly different path:

1. Go to **Settings**
2. Tap **Security and privacy**
3. Tap **More security settings**
4. Tap **Identity Check**
5. Enable the feature and confirm biometrics

*Reference: Samsung Knox security documentation — https://security.samsungmobile.com*

---

## Android 16 Additions

Devices running **Android 16** gain an additional control:

**Failed Authentication Lock**: The device automatically locks after several failed authentication attempts. A dedicated toggle in Settings allows users to control this behavior. This complements Identity Check by preventing brute-force PIN attempts.

---

## Comparison: Identity Check vs. Stolen Device Protection

| Feature | Identity Check (Android 15+) | Stolen Device Protection (iOS 17.3+) |
|---|---|---|
| Platform | Android (Pixel, Samsung, later broader) | iOS 17.3+ |
| Trigger condition | Outside trusted locations | Away from familiar locations |
| Biometric-only actions | Yes — no passcode fallback | Yes — no passcode fallback |
| Delayed security actions | No (as of 2025) | Yes — 1-hour delay for critical changes |
| Required setup | Biometrics, Location, Find My Device | 2FA, Face/Touch ID, Significant Locations, Find My |
| Blocks biometric changes? | Yes | Yes |
| Blocks Find My Device disable? | Yes | Yes (via delay) |

---

## Limitations and Considerations

| Consideration | Details |
|---|---|
| **Biometric spoofing** | Advanced biometric spoofing attacks could theoretically bypass; keep device updated |
| **Location accuracy** | GPS/Wi-Fi location must be accurate; imprecise location may trigger in wrong context |
| **Emergency access** | Emergency calls and services remain accessible regardless of Identity Check state |
| **Trusted location registration** | Must be done while at the trusted location with accurate GPS |
| **Battery and location drain** | Continuously monitoring location for Identity Check context has minimal but non-zero battery impact |

---

## Related Documents

- [Android Hardening Guide](../hardening/android-hardening.md)
- [Google Account Security](google-account-security.md)
- [Find Hub](find-my-device.md)
- [iOS Stolen Device Protection (comparison)](../ios/stolen-device-protection.md)

---

*Last Updated: 2026-06-01 | Source: https://support.google.com/pixelphone/answer/9463625 | https://thehackernews.com/2025/01/androids-new-identity-check-feature.html*
