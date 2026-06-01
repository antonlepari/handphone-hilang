# Lost Mode — iOS

> Last Updated: 2026-06-01

## Overview

**Lost Mode** is an iOS feature activated through Find My that locks your iPhone and displays a custom message with your contact information on the lock screen. It is designed to both protect the device's data and increase the chance of recovery by allowing a finder to contact you without unlocking the phone.

Lost Mode is distinct from a remote erase — it preserves your data while protecting access to it.

*Reference: https://support.apple.com/en-us/105072*

---

## What Lost Mode Does

When you activate Lost Mode on a missing iPhone:

| Action | Effect |
|---|---|
| **Lock screen** | Device is immediately locked with your existing passcode |
| **Custom message** | Your chosen message appears on the lock screen (e.g., "This iPhone is lost. Please call +1-555-XXX-XXXX") |
| **Contact phone** | An optional phone number is displayed that anyone can call directly from the lock screen, without unlocking |
| **Location tracking** | The device continuously reports its GPS location to Find My |
| **Apple Pay / Wallet** | Disabled — cards, transit passes, car keys cannot be used |
| **Accessory pairing** | New accessories (Bluetooth, USB) cannot be paired |
| **Notifications** | Existing app notifications are hidden from the lock screen |
| **Data protection** | All data remains on the device and is protected by the passcode |

> **ℹ️ NOTE:** Lost Mode does **not** delete your data. It locks the device. Data remains intact and will be accessible again when you enter the correct passcode after recovery.

---

## What the Finder or Thief Sees

When someone picks up an iPhone in Lost Mode, they see:

```
┌─────────────────────────────────────────────┐
│                                             │
│                [Lock screen]                │
│                                             │
│   ┌─────────────────────────────────────┐   │
│   │    This iPhone has been lost.       │   │
│   │    Please call +1-555-XXXX          │   │
│   │    if found.                        │   │
│   └─────────────────────────────────────┘   │
│                                             │
│   [Call] button (calls without unlocking)   │
│                                             │
│              Enter Passcode                 │
└─────────────────────────────────────────────┘
```

They cannot:
- Access any apps or data
- Use Apple Pay
- Pair Bluetooth devices
- Clear the Lost Mode message without your Apple ID

---

## How to Enable Lost Mode

### Via iCloud.com

1. Go to **https://www.icloud.com/find**
2. Sign in with your Apple ID
3. Click the missing device on the map or device list
4. Click **Mark as Lost** (or **Activate** under the "Mark as Lost" section)
5. Click **Continue**
6. Enter a phone number where you can be reached
7. Enter a message to display (optional — a default message is shown if left blank)
8. Click **Activate**

### Via Find My App (Another Apple Device)

1. Open **Find My** app
2. Tap **Devices** tab
3. Tap your missing device
4. Scroll down and tap **Mark as Lost**
5. Tap **Continue**
6. Enter a phone number and optional message
7. Tap **Activate**

![Lost Mode Activation](../images/ios-lost-mode-activation.png)
*Figure 1: Activating Lost Mode via iCloud.com — click Mark as Lost, enter contact information*

---

## Lost Mode and Location Tracking

Once Lost Mode is activated, Find My will display:
- **Real-time location** on the map (if device has internet connectivity)
- **Last known location** with timestamp (if device is offline)
- **Location history** showing movement over time

You will receive a notification on other Apple devices when the lost iPhone is located.

---

## Turning Off Lost Mode

When you recover your device:

1. Enter your device passcode on the iPhone — this automatically disables Lost Mode
2. Or, go to Find My app / iCloud.com and select **Turn Off Mark as Lost**

---

## Lost Mode After Battery Dies

If the device battery dies while in Lost Mode:
- Lost Mode remains active — the device does not automatically leave Lost Mode when battery is depleted
- When the device is charged and turned on, it will still be in Lost Mode
- "Send Last Location" (if enabled) will have recorded the last GPS location before shutdown

---

## Lost Mode vs. Remote Erase

Use this decision matrix to choose the appropriate action:

```
DEVICE MISSING — WHICH ACTION?

Is recovery still possible?
├── YES, device is nearby → Play Sound
├── MAYBE, device is somewhere trackable → Mark as Lost
└── NO, or data is highly sensitive → Erase Device

Is this a corporate device?
├── YES → Consult IT / MDM policy before erasing
└── NO → Use personal judgment

Does the device contain irreplaceable data?
├── YES (no backup) → Mark as Lost first; buy time
└── NO (current backup exists) → Erase is safe option
```

> **⚠️ WARNING:** Once you erase a device, you can no longer track it via Find My. Use "Mark as Lost" first to monitor location, then erase if recovery becomes impossible.

---

## Lost Mode Notifications

You can configure notifications for when:
- The device is located
- The device battery is low
- The device connects to a network

These notifications help you monitor the device's status without repeatedly checking Find My.

---

## Related Documents

- [Find My](find-my.md)
- [Activation Lock](activation-lock.md)
- [Stolen Device Protection](stolen-device-protection.md)
- [First 5 Minutes](../incident-response/first-5-minutes.md)
- [Emergency Checklist](../checklists/emergency-checklist.md)

---

*Last Updated: 2026-06-01 | Source: https://support.apple.com/en-us/105072*
