# Activation Lock — iOS

> Last Updated: 2026-06-01

## Overview

**Activation Lock** is an iOS security feature that ties an iPhone to its associated Apple ID. When enabled, the device requires the owner's Apple ID email and password before it can be reactivated after a factory reset, erasure, or when being set up for the first time by a new owner.

Activation Lock is **automatically enabled** whenever Find My is turned on. You do not need to manually configure it — it activates as a consequence of enabling Find My.

*Reference: https://support.apple.com/en-us/108794*

---

## How Activation Lock Works

### Activation

Activation Lock activates automatically when:
1. Find My is enabled on the device (Settings > [Your Name] > Find My > Find My iPhone: On)
2. The device is signed in to an Apple ID

No additional configuration is required.

### What It Protects Against

When a thief attempts to reset and reuse a stolen iPhone:

```
WITHOUT Activation Lock:
  Thief steals iPhone
  → Performs factory reset (Settings or iTunes/Finder)
  → Sets up device with their own Apple ID
  → Sells or uses device freely

WITH Activation Lock:
  Thief steals iPhone
  → Attempts factory reset
  → Device reaches Activation Lock screen during setup
  → Requires original Apple ID email + password
  → Thief cannot proceed without credentials
  → Device is unusable for resale or reuse
  → Economic incentive for theft is significantly reduced
```

### The Activation Lock Screen

A device with Activation Lock enabled displays this screen during setup:

```
┌────────────────────────────────────────────┐
│          Activation Lock                   │
│                                            │
│   This iPhone is linked to an Apple ID    │
│                                            │
│   Email: [owner's Apple ID]                │
│   Password: ________                       │
│                                            │
│       [Unlock with Apple ID]               │
│                                            │
└────────────────────────────────────────────┘
```

Even after a complete erasure through iTunes/Finder on a computer, the Activation Lock screen appears during the device setup process.

---

## Checking Activation Lock Status

### Before Buying a Used iPhone

Before purchasing a used iPhone, verify it does not have an active Activation Lock:

**Method 1: Check the device directly**
- If the device boots to the Activation Lock screen, it is locked
- The device cannot be used without the previous owner's Apple ID credentials

**Method 2: Check IMEI online**
1. Get the device's IMEI (dial `*#06#` or check Settings > General > About)
2. Go to: **https://checkcoverage.apple.com**
3. Enter the IMEI or serial number
4. This shows warranty status but does not directly show Activation Lock status

**Method 3: Apple Activation Lock Status Check (for MDM)**
Apple provides an API for MDM administrators to check Activation Lock status by IMEI/serial.

> **⚠️ WARNING:** Do not purchase a used iPhone that boots to the Activation Lock screen. The seller cannot legitimately unlock it without the original Apple ID. Any seller claiming they can remove Activation Lock remotely for a fee is running a scam.

---

## Removing Activation Lock (Legitimate Methods)

### Method 1: Remove via iCloud.com (Remote)

If you no longer have physical access to the device:

1. Go to **https://www.icloud.com/find**
2. Sign in with the Apple ID linked to the device
3. Select the device
4. Click **Erase This Device** (if not already erased)
5. After erasure completes, click **Remove from Account**

This removes Activation Lock remotely, allowing the next person to set up the device.

### Method 2: Sign Out on the Device

Before selling or giving away your iPhone:

1. Open **Settings**
2. Tap your name (Apple ID)
3. Scroll down and tap **Sign Out**
4. Enter your Apple ID password
5. Follow prompts to complete sign-out
6. Then perform a factory reset via Settings > General > Transfer or Reset iPhone > Erase All Content and Settings

### Method 3: At an Apple Store

If you have lost access to your Apple ID and cannot sign in remotely:
- Visit an Apple Store with **proof of purchase** (original receipt, invoice)
- Apple can remove Activation Lock with verified ownership documentation
- Without proof of purchase, Apple cannot remove Activation Lock

> **💡 TIP:** Keep your original device purchase receipt in a secure location (email it to yourself, save it in a secure cloud folder). This is the only documentation that can prove ownership to Apple if you lose Apple ID access.

---

## Activation Lock and MDM (Enterprise)

For corporate devices managed through **Apple Business Manager (ABM)** or **Apple School Manager (ASM)**:

- Devices enrolled in ABM/ASM can have Activation Lock managed by the MDM administrator
- Administrators can disable Activation Lock for organizational devices during enrollment
- When a managed device is wiped, it can be re-enrolled without requiring the previous user's Apple ID
- MDM can also generate a bypass code to unlock Activation Lock on managed devices

*Reference: https://support.apple.com/guide/apple-business-manager/about-activation-lock*

---

## iOS 17.5 Repair State and Activation Lock

In **iOS 17.5**, Apple introduced **Repair State**:
- iPhone can be sent for service without removing Activation Lock
- Device remains trackable via Find My during repair
- Repair technician cannot erase the device without the owner's Apple ID
- Activation Lock persists throughout the repair process

This prevents unauthorized data access during third-party or Apple repair.

---

## Activation Lock Does NOT Protect Against

| Threat | Activation Lock Protection? | Additional Defense Needed |
|---|---|---|
| Data access from unlocked device | No | Strong PIN, Stolen Device Protection |
| SIM card removal and reuse | No | SIM PIN |
| iCloud data access via stolen credentials | No | Strong Apple ID password + 2FA |
| Physical tampering (chips-off attack) | No | Full disk encryption (AES-256 on iOS) |
| Selling the device at a loss | No | Activation Lock still reduces resale value |

---

## Checklist: Activation Lock Best Practices

- [ ] Find My is enabled on the device (automatically enables Activation Lock)
- [ ] Apple ID has a strong password
- [ ] Apple ID has two-factor authentication enabled
- [ ] Apple ID password is stored in a secure password manager (not only on the device)
- [ ] Original proof of purchase is saved securely
- [ ] When selling device: Sign out of Apple ID before transferring

---

## Related Documents

- [Find My](find-my.md)
- [Lost Mode](lost-mode.md)
- [Stolen Device Protection](stolen-device-protection.md)
- [Apple ID Recovery](apple-id-recovery.md)
- [MDM Enterprise](../hardening/mdm-enterprise.md)

---

*Last Updated: 2026-06-01 | Source: https://support.apple.com/en-us/108794*
