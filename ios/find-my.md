# Find My — iOS

> Last Updated: 2026-06-01

## Overview

**Find My** is Apple's platform for locating lost or stolen iPhones, iPads, Macs, Apple Watches, AirPods, and AirTags. It uses GPS, Wi-Fi positioning, cellular triangulation, and a crowdsourced encrypted Bluetooth network of hundreds of millions of Apple devices to locate items even when they are offline.

Find My is distinct from, but related to, Activation Lock — enabling Find My automatically enables Activation Lock.

*Reference: https://support.apple.com/en-us/104978*

---

## Prerequisites

For Find My to help you recover your device, these must be configured **before** the loss:

- [ ] **Find My** is enabled on the device (Settings > [Your Name] > Find My > Find My iPhone: On)
- [ ] **Enable Offline Finding** is toggled On (allows location even without cellular/Wi-Fi)
- [ ] **Send Last Location** is toggled On (sends location to Apple when battery is critically low)
- [ ] **Two-Factor Authentication** is enabled on your Apple ID
- [ ] You know your Apple ID email and password

> **⚠️ WARNING:** Find My cannot be turned on remotely. It must be enabled before the device is lost. If Stolen Device Protection is enabled, Find My cannot be turned off without biometric authentication.

---

## How to Enable Find My

1. Open **Settings**
2. Tap your name at the top (Apple ID)
3. Tap **Find My**
4. Tap **Find My iPhone**
5. Enable **Find My iPhone**: Toggle to **On**
6. Enable **Enable Offline Finding**: Toggle to **On**
7. Enable **Send Last Location**: Toggle to **On**

![Find My Settings](../images/ios-find-my-settings.png)
*Figure 1: Find My settings in iOS — Settings > [Your Name] > Find My > Find My iPhone*

---

## Accessing Find My Remotely

### Via iCloud.com

1. Go to **https://www.icloud.com/find**
2. Sign in with your Apple ID
3. Select your device from the map or device list

### Via Find My App (Another Apple Device)

1. Open the **Find My** app on another iPhone, iPad, or Mac
2. Tap the **Devices** tab
3. Select your missing device

### Via Family Sharing

If you are part of a Family Sharing group, trusted family members can see your device location and assist with Find My actions:
1. Open Find My app
2. Tap **People** tab
3. Family members can share location and assist if you have granted permission

---

## Available Remote Actions

### Play Sound

Causes the device to play a loud alert tone for approximately 2 minutes, even when in silent mode. Useful when the device is misplaced nearby.

### Mark as Lost (Lost Mode)

Enables Lost Mode — see [Lost Mode](lost-mode.md) for full details. When you mark a device as lost:
- The device is locked with your passcode
- A custom message and phone number are displayed on the lock screen
- The device begins continuously reporting location updates
- Apple Pay is disabled
- The device cannot be paired with new accessories

### Erase This Device

Performs a complete remote wipe of the device:
- All personal data is deleted
- The device is restored to factory settings
- **Activation Lock remains active** — the device cannot be set up without your Apple ID credentials

> **⚠️ WARNING:** Once you erase a device, you can no longer track its location via Find My. The device will show as "Erased" in Find My once the action completes. Do not erase until you are certain recovery is not possible and data protection takes priority.

---

## Offline Finding

### How It Works

iPhones broadcast an encrypted Bluetooth signal that can be detected by other nearby Apple devices. Those devices silently relay the encrypted location signal to Apple's servers. Only the owner of the device can decrypt and view the location — not Apple, and not the devices relaying the signal.

### Send Last Location

When enabled, the iPhone automatically sends its last known GPS location to Apple's servers when the battery reaches a critically low level, before it shuts down. This last location is visible in Find My.

### Post-Power-Off Tracking

Newer iPhones (iPhone 11 and later) can continue to be located for a period **after the battery dies or the device is turned off**, using a low-power Bluetooth beacon. This requires:
- "Enable Offline Finding" was turned on before power-off
- Another Apple device is within Bluetooth range to relay the signal

---

## iOS 17.5 Repair State

Introduced in **iOS 17.5**, **Repair State** allows you to send an iPhone for service without disabling Find My and Activation Lock:

- Device remains trackable in Find My
- Cannot be erased without the owner's Apple ID password
- Can be placed in Lost Mode so the repair technician sees contact information
- Activation Lock remains active throughout the repair

This prevents unauthorized data access during device servicing.

*Source: https://support.apple.com/en-us/105092*

---

## Family Sharing and Find My

With **Family Sharing**, up to 5 family members can:
- Share their own device locations with each other
- Assist each other with Lost Mode actions
- Track shared AirTags

**Setting up location sharing:**
1. Settings > [Your Name] > Family Sharing
2. Set up or join a Family Sharing group
3. Enable "Share My Location"

---

## AirTag Integration

**AirTags** are small tracking devices that integrate with Find My:
- Attach to keys, wallet, luggage, or bag
- Detectable in Find My even when out of Bluetooth range of your device
- Use Precision Finding (UWB on supported iPhones) for centimeter-level location when nearby

> **ℹ️ NOTE:** AirTags are designed for locating misplaced items, not people. Apple has implemented anti-stalking measures: unknown AirTags traveling with you for an extended period trigger an alert on your iPhone.

---

## Privacy and Security

- All Find My location data is **end-to-end encrypted**
- Apple cannot read the location of your device
- Crowdsourced signals are encrypted with keys only you hold
- Find My network participation is opt-out only for users who disable Find My entirely

---

## Checklist: Find My Configuration

- [ ] Find My iPhone: **Enabled**
- [ ] Enable Offline Finding: **Enabled**
- [ ] Send Last Location: **Enabled**
- [ ] Two-factor authentication on Apple ID: **Enabled**
- [ ] Apple ID password memorized or stored in secure password manager
- [ ] Family sharing with trusted contact who can assist with remote actions

---

## Related Documents

- [Lost Mode](lost-mode.md)
- [Activation Lock](activation-lock.md)
- [Stolen Device Protection](stolen-device-protection.md)
- [Apple ID Recovery](apple-id-recovery.md)
- [First 5 Minutes](../incident-response/first-5-minutes.md)

---

*Last Updated: 2026-06-01 | Source: https://support.apple.com/en-us/104978*
