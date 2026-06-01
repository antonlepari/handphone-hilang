# Factory Reset Protection (FRP) — Android

> Last Updated: 2026-06-01

## Overview

**Factory Reset Protection (FRP)** is an Android security feature introduced in Android 5.1 (Lollipop) that prevents a factory-reset device from being set up without the original owner's Google Account credentials. It is specifically designed to deter device theft by making stolen phones unusable unless the thief can authenticate with the original Google Account.

*Reference: https://support.google.com/android/answer/6088432*

---

## How FRP Works

### The Protection Mechanism

FRP ties the device to the Google Account that was active on it. When a factory reset is performed through **unauthorized methods** — such as:

- Recovery mode (Volume + Power button combination)
- ADB commands
- Fastboot commands
- Hardware button combinations

...the device will require the original Google Account email and password during the setup wizard before it can be used.

### Normal vs. Unauthorized Reset

```
AUTHORIZED RESET (via Settings menu):
  Settings > General Management > Reset > Factory Data Reset
  → User is authenticated (logged in) when initiating
  → Google Account is properly removed during reset
  → FRP does NOT trigger
  → Device can be set up with any account after reset

UNAUTHORIZED RESET (via recovery mode or hardware):
  → Device is reset without authenticated session
  → Google Account information is retained in protected storage
  → FRP TRIGGERS on next setup
  → Device requires original Google Account credentials
```

### Technical Implementation

FRP stores Google Account information in a protected partition that survives a factory reset initiated through unauthorized methods. This partition is only cleared when the user performs a factory reset through the authenticated Settings menu (which first removes the associated Google Account).

---

## Why FRP Matters

Without FRP:
1. A thief steals a device
2. Performs a factory reset using hardware buttons
3. Sets up the device with their own account
4. Sells or uses the device

With FRP:
1. A thief steals a device
2. Attempts factory reset using hardware buttons
3. Device reaches the Google Account verification screen
4. Thief cannot proceed without the original credentials
5. Device remains locked, significantly reducing resale value and incentive for theft

> **ℹ️ NOTE:** FRP is one of the most effective anti-theft features on Android. It directly reduces the economic incentive for device theft by making stolen devices difficult to resell or reuse.

---

## Configuration

### Verifying FRP Is Active

FRP is **automatically active** when:
- A Google Account is signed in to the device
- Android version is 5.1 or higher

No manual configuration is required. To verify:

1. Go to **Settings > Accounts > Google**
2. If a Google Account is listed, FRP is active for that account

### Configuring FRP Before Selling or Giving Away a Device

> **⚠️ WARNING:** If you perform a factory reset through recovery mode without first removing your Google Account, FRP will lock the device for the new owner. Always reset via the Settings menu.

**Correct process before transferring a device:**
1. Go to **Settings > Accounts > Google**
2. Tap your Google Account
3. Tap **Remove account**
4. Then perform factory reset via **Settings > General Management > Reset > Factory Data Reset**

Or simply:
1. Go to **Settings > General Management > Reset > Factory Data Reset**
2. This automatically handles account removal in the authenticated session

---

## Enhanced FRP: The 72-Hour Rule

Some Android manufacturers (including Samsung) implement an enhanced FRP rule: if a Google Account was added to a device within the **last 72 hours** before a factory reset was initiated, the device may apply additional lockout restrictions. This prevents a thief from:
1. Stealing a device
2. Quickly adding a new Google Account
3. Immediately performing a factory reset to "clear" FRP

---

## Enterprise FRP (eFRP)

For enterprise deployments, **Enterprise Factory Reset Protection (eFRP)** extends standard FRP with organizational control:

- IT administrators can specify **which Google Accounts** (or zero accounts) can reactivate a device after reset
- In fully managed (MDM) environments, resets performed through Settings can still be protected
- Useful for corporate-owned devices to prevent unauthorized reuse after employee departure

*Reference: https://support.google.com/work/android/answer/7596562*

---

## FRP Bypass Attempts (Attacker Perspective)

Understanding bypass attempts helps configure defenses:

### Common Bypass Methods

| Method | Description | Effectiveness |
|---|---|---|
| Social Engineering Google | Convincing Google support to remove FRP | Very Low — Google requires identity verification |
| Firmware Flashing | Flashing unsigned firmware to clear FRP partition | Varies by device; most current devices have Verified Boot |
| ADB Bypass Tools | Third-party tools claiming to bypass FRP | Often malware; actual effectiveness varies and decreases with updates |
| Hardware Service Tools | Commercial tools used by repair shops | Limited effectiveness on current Android versions |

> **⚠️ WARNING:** The vast majority of "FRP bypass tools" found online are malware, adware, or scams targeting device owners who have locked themselves out. Do not use them.

### FRP Resistance on Modern Devices

Devices with **Verified Boot** (Android 8+) and **Google Titan M** (Pixel 3+) or equivalent secure elements make FRP significantly more resistant to bypass:

- The secure element stores FRP information in tamper-resistant hardware
- Verified Boot prevents unsigned firmware from running that could clear FRP partitions
- Repeated failed bypass attempts may trigger permanent device lock

---

## FRP and Samsung Knox

Samsung Galaxy devices running **Samsung Knox** implement FRP through a dual-layer system:

1. **Standard Android FRP** — as described above
2. **Samsung Reactivation Lock** — additional layer tied to Samsung Account (separate from Google Account)

To fully protect a Samsung device:
- Enable FRP via Google Account (automatic)
- Enable Samsung Reactivation Lock via **Settings > Biometrics and security > Find My Mobile > Reactivation lock**

*Reference: https://www.samsungknox.com/en/blog/what-is-factory-reset-protection*

---

## What FRP Does NOT Protect Against

FRP is designed to prevent **unauthorized reuse** of the device, not necessarily protect data. Understand these limitations:

| Threat | FRP Protection? | Additional Mitigation Needed |
|---|---|---|
| Data extraction before reset | No | Use strong device encryption + PIN |
| SIM removal and use | No | Enable SIM PIN |
| Reading SD card data | No | Encrypt SD card; avoid storing sensitive data there |
| Physical access to unlocked device | No | Strong PIN, screen timeout, Identity Check |
| Cloud data access via stolen credentials | No | 2FA on Google Account |

---

## Checklist: FRP Best Practices

- [ ] Google Account is signed in on the device (FRP automatically active)
- [ ] Google Account has strong password and 2FA enabled
- [ ] If selling/giving away device: factory reset via Settings menu, not recovery mode
- [ ] For Samsung: enable Samsung Reactivation Lock as additional layer
- [ ] For enterprise: configure eFRP policy via MDM

---

## Related Documents

- [Google Account Security](google-account-security.md)
- [Android Hardening Guide](../hardening/android-hardening.md)
- [MDM Enterprise](../hardening/mdm-enterprise.md)

---

*Last Updated: 2026-06-01 | Source: https://support.google.com/android | https://www.samsungknox.com*
