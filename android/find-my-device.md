# Find Hub (formerly Find My Device) — Android

> Last Updated: 2026-06-01

## Overview

**Find Hub** (renamed from "Find My Device" in May 2025) is Google's device tracking and recovery platform for Android. It uses a combination of GPS, Wi-Fi positioning, cellular triangulation, and a crowdsourced Bluetooth network of over one billion Android devices to locate lost or stolen phones, tablets, earbuds, and accessories.

> **ℹ️ NOTE:** The app was officially renamed from "Find My Device" to "Find Hub" in May 2025. Both names refer to the same service. All existing functionality was preserved during the rename.

*Reference: https://android.com/articles/what-is-find-hub-and-how-to-use-it/*

---

## Prerequisites

Before Find Hub can help you recover your device, these must be configured **before** the loss:

- [ ] Find Hub is enabled on the device
- [ ] Device is signed in to a Google Account
- [ ] Location permissions are enabled
- [ ] Device has an active internet connection (or has been near other Android devices for offline location)
- [ ] Device is powered on (or is a supported Pixel for post-power-off tracking)

> **⚠️ WARNING:** If Find Hub is disabled before the device goes missing, you will not be able to track, lock, or erase it remotely. Enable it now.

---

## How to Enable Find Hub

### On Your Android Device

1. Open **Settings**
2. Tap **Security** (or **Security & privacy** on some devices)
3. Tap **Find My Device** or **Find Hub**
4. Toggle **Use Find My Device** to **On**
5. Confirm location is enabled: tap **Location** and ensure it is set to **On**

Alternatively: **Settings > Google > Find My Device > On**

> **💡 TIP:** On Samsung devices, also enable Samsung's own Find My Mobile at: **Settings > Security and privacy > Find My Mobile**. Having both provides redundancy.

![Find Hub Settings](../images/android-find-my-device.png)
*Figure 1: Find Hub settings toggle on Android (Settings > Security > Find My Device)*

---

## Accessing Find Hub Remotely

### Via Web Browser

1. Go to **https://myaccount.google.com/find-your-phone** or **https://android.com/find**
2. Sign in with the Google Account linked to the missing device
3. Select the device from the list

### Via Find Hub App (Another Android Device)

1. Install or open the **Find Hub** app (available on Google Play)
2. Sign in as a **Guest** using the Google Account linked to the missing device

### Via Google Home (Pixel)

Some Pixel devices can be located via the Google Home app when signed in to the same Google Account.

---

## Available Remote Actions

Once you access your device in Find Hub, three primary actions are available:

### 1. Play Sound

Causes the device to ring at maximum volume for 5 minutes, even if it is on silent or vibrate. Useful when the device is lost nearby (dropped behind furniture, left in a car, etc.).

- Does not require the device to be unlocked
- Works over Wi-Fi or cellular

### 2. Secure Device (Remote Lock)

Locks the device with the screen lock PIN/password and optionally:
- Displays a custom message on the lock screen (e.g., "This phone is lost. Call +1-555-XXX-XXXX")
- Adds a phone number that can be called from the lock screen without unlocking
- Signs the device out of the Google Account

> **⚠️ WARNING:** Once "Secure Device" signs out the Google Account, Find Hub can no longer access the device. Use this action only after confirming recovery is not immediately possible, or use it **without** the "Sign out of Google Account" option first.

### 3. Erase Device

Performs a complete factory reset of the device, deleting all data including:
- Photos and files
- Installed apps
- Account credentials
- Google Wallet cards and keys

> **⚠️ WARNING:** Erasing the device is **irreversible**. Once erased, you cannot track the device unless it was set up with a Google Account after the erase (in which case Factory Reset Protection will engage). Use this only when:
> - Recovery of the device is confirmed impossible
> - The device contains sensitive data that must not be accessed by an attacker
> - You have a current backup of your data

---

## Offline Device Tracking

Find Hub supports locating devices even when they are offline (no Wi-Fi or cellular):

### How It Works

Android devices in the Find Hub network periodically broadcast an encrypted Bluetooth signal. Other nearby Android devices — even those belonging to strangers — silently detect this signal and report the encrypted location to Google. Only the device owner can decrypt and view this location.

### Enabling Offline Location Sharing

1. Open the **Find Hub** app on your device
2. Tap your device name
3. Go to **Settings**
4. Enable **Store location** or **Find offline devices**
5. Select **With network in all areas** for maximum coverage, or **With network in high-traffic areas only** for a privacy-preserving option

### Post-Power-Off Location (Pixel 8 and Newer)

Google Pixel 8, 8a, and subsequent Pixel models can be located for **several hours after the battery has been depleted**, provided the "find offline devices" setting was previously enabled.

---

## 2025 Feature Additions

Google expanded Find Hub capabilities in 2025 with:

**Ultra-Wideband (UWB) Support**
Provides centimeter-level precision for locating items when in close proximity. Supported on compatible Pixel and Motorola devices with UWB hardware.

**Satellite Connectivity**
Allows device location reporting via satellite when cellular and Wi-Fi are unavailable. Rolling out through 2025.

**Airline Baggage Integration**
Bluetooth tracker tags can share location with select airlines (Aer Lingus, British Airways, Cathay Pacific, Iberia, Singapore Airlines) to locate checked luggage.

**Third-Party Tracker Support**
Compatible with Chipolo, Pebblebee, Motorola tags, and luggage from brands like Mokobara, July, and Peak.

*Source: Google Blog, May 2025 — https://security.googleblog.com*

---

## Security and Privacy

- All location data in Find Hub is **end-to-end encrypted**
- Only the account owner can view the device's location
- Crowdsourced location signals are encrypted; participating devices in the network cannot read the location data they relay

---

## Theft Protection Features (Android 10+)

In addition to Find Hub, Android includes on-device theft protection:

### Theft Detection Lock

Uses on-device AI (accelerometer, gyroscope, Wi-Fi, and Bluetooth) to detect motion patterns consistent with a snatch theft — sudden jerks, rapid movement, running, cycling. If detected, the screen automatically locks before the thief can disable tracking.

*Reference: https://security.googleblog.com/2024/10/android-theft-protection.html*

### Offline Device Lock

If the device goes offline (internet disabled) while unlocked after being stolen, it automatically locks its screen after a short period. This prevents a thief from disabling Find Hub tracking by turning off Wi-Fi.

### Remote Lock (Without Internet)

Android 10+ allows locking the device even without an internet connection using a stored PIN or via an SMS-based challenge.

---

## Step-by-Step: What To Do Right Now

```
DEVICE MISSING? Follow these steps:

Step 1: Go to https://android.com/find
Step 2: Sign in with your Google Account
Step 3: Select your device
Step 4: Choose "Play Sound" — if nearby
Step 5: Choose "Secure Device" — to lock and display contact info
Step 6: (If recovery impossible) — Choose "Erase Device"
```

---

## Related Documents

- [Factory Reset Protection](factory-reset-protection.md)
- [Google Account Security](google-account-security.md)
- [Identity Check](identity-check.md)
- [First 5 Minutes](../incident-response/first-5-minutes.md)
- [Emergency Checklist](../checklists/emergency-checklist.md)

---

*Last Updated: 2026-06-01 | Source: https://support.google.com/android | https://android.com/articles/what-is-find-hub-and-how-to-use-it/*
