# Before Loss — Prevention Checklist

> Last Updated: 2026-06-01

## Overview

This checklist covers the essential proactive steps every smartphone user should complete to minimize the impact of a future loss or theft event. These items apply to both Android and iOS devices.

Complete these items now, before any incident occurs.

---

## Section 1: Device Security Fundamentals

- [ ] **Enable device encryption**
  - Android: Automatically enabled when a PIN/password is set on Android 6+. Verify at: Settings > Security > Encryption & Credentials
  - iOS: Automatically enabled when a passcode is set on iOS 8+. No separate configuration needed.

- [ ] **Set a strong PIN or passphrase (not a 4-digit PIN)**
  - Minimum: 6-digit PIN
  - Better: 8+ digit PIN
  - Best: Alphanumeric passphrase (e.g., "blue-mountain-4-sunrise")
  - Android: Settings > Security > Screen lock
  - iOS: Settings > Face ID & Passcode > Change Passcode > Passcode Options > Custom Alphanumeric Code

- [ ] **Set screen lock timeout to 30 seconds or less**
  - Android: Settings > Display > Screen timeout
  - iOS: Settings > Display & Brightness > Auto-Lock

- [ ] **Enable biometric authentication (fingerprint or face)**
  - Android: Settings > Security > Fingerprint / Face recognition
  - iOS: Settings > Face ID & Passcode / Touch ID & Passcode

- [ ] **Disable "Show notifications on lock screen" for sensitive apps**
  - Android: Settings > Notifications > [App] > On Lock Screen: Don't show
  - iOS: Settings > Notifications > [App] > Show Previews: When Unlocked

- [ ] **Enable "Erase after 10 failed attempts"**
  - Android: Settings > Security > Automatically lock (varies by manufacturer)
  - iOS: Settings > Face ID & Passcode > Erase Data: Toggle On

---

## Section 2: Enable Remote Tracking and Wipe

- [ ] **Enable Find Hub (Android)**
  - Settings > Security > Find My Device > Enable
  - Verify at: https://android.com/find

- [ ] **Enable Find My (iOS)**
  - Settings > [Your Name] > Find My > Find My iPhone > Enable
  - Enable "Enable Offline Finding" and "Send Last Location"
  - Verify at: https://icloud.com/find

- [ ] **Test remote access to your device tracking**
  - Log in to Find Hub or Find My from a different device/browser
  - Confirm your device appears and has a recent location

- [ ] **Enable remote wipe capability**
  - Both Find Hub (Android) and Find My (iOS) support remote wipe when tracking is enabled

---

## Section 3: SIM and Carrier Security

- [ ] **Enable SIM PIN**
  - Android: Settings > Security > SIM card lock > Set up SIM card lock
  - iOS: Settings > Cellular > SIM PIN
  - Use a 6–8 digit PIN distinct from your device PIN

- [ ] **Set up carrier account PIN or passphrase**
  - Call your carrier or log in to their website
  - Set a unique PIN/passcode required for any account changes
  - This defends against SIM swap attacks at the carrier level

- [ ] **Enable port-out lock / number lock with your carrier**
  - Verizon: "Number Lock" (free, via My Verizon app)
  - AT&T: "Extra Security" (free, via AT&T account settings)
  - T-Mobile: "SIM Protection" (free, via T-Mobile app or My T-Mobile)
  - Other carriers: Check carrier's security/account settings

- [ ] **Document your IMEI number**
  - Dial `*#06#` on your device to display IMEI
  - Record in a secure location (not only on the device)
  - Also found at: Android: Settings > About Phone; iOS: Settings > General > About
  - This is required to file a stolen device report with carriers and police

---

## Section 4: Account Security — Google / Apple ID

- [ ] **Enable two-factor authentication on Google Account or Apple ID**
  - Google: https://myaccount.google.com/security > 2-Step Verification
  - Apple: Settings > [Your Name] > Sign-In & Security > Two-Factor Authentication

- [ ] **Use an authenticator app for 2FA — not SMS**
  - Google Authenticator, Microsoft Authenticator, or Authy
  - SMS-based 2FA is vulnerable to SIM swap attacks

- [ ] **Set up recovery options for Google Account**
  - Recovery email (different provider, also 2FA-protected)
  - Download and store backup codes offline: https://myaccount.google.com/two-step-verification/backup-codes

- [ ] **Set up Apple ID Recovery**
  - Configure a Recovery Contact: Settings > [Your Name] > Sign-In & Security > Account Recovery > Recovery Contact
  - Generate a Recovery Key: Settings > [Your Name] > Sign-In & Security > Recovery Key
  - Store Recovery Key offline in a physically secure location

- [ ] **Review and remove unused trusted devices**
  - Google: https://myaccount.google.com/device-activity
  - Apple: Settings > [Your Name] > scroll to Devices

---

## Section 5: Backups

- [ ] **Create and verify an encrypted device backup**
  - Android: Settings > Google > Backup > Enable Google Backup
  - iOS: Settings > [Your Name] > iCloud > iCloud Backup > Back Up Now
  - Optional local backup: iTunes/Finder (select "Encrypt local backup")

- [ ] **Test backup restoration**
  - Verify you can restore data from your backup on a test device or during device setup
  - A backup you have never tested may be incomplete or corrupted

- [ ] **Set backup frequency to daily or automatic**
  - Both Android and iOS support automatic daily backups when connected to Wi-Fi and charging

- [ ] **Back up photos separately if they are irreplaceable**
  - Google Photos (Android) or iCloud Photos (iOS) for cloud sync
  - Consider a secondary local backup for photos

---

## Section 6: Password Manager

- [ ] **Install and use a password manager**
  - Options: Bitwarden (open source), 1Password, Google Password Manager (built-in), Apple Passwords (iOS 18+)
  - Store all account credentials in the password manager, not in your browser or notes app

- [ ] **Store the password manager master password somewhere accessible offline**
  - Written down and stored in a physically secure location
  - Do NOT store the master password only on the device being protected

- [ ] **Ensure password manager can be accessed from a backup device**
  - Install the password manager app on a secondary device, or access via web browser

---

## Section 7: Emergency Information

- [ ] **Record the following information and store offline (not only on device):**
  - Device make and model
  - IMEI number (see Section 3)
  - Serial number (Settings > About)
  - Carrier name and account number
  - Carrier customer service number
  - Google Account / Apple ID email address
  - Recovery email address
  - Insurance policy number and contact (if applicable)

- [ ] **Enable Medical ID / Emergency SOS**
  - Android: Settings > Safety & Emergency > Medical Information
  - iOS: Settings > Health > Medical ID > Show When Locked
  - Helps emergency responders and allows "ice" (In Case of Emergency) contact access

---

## Section 8: Advanced / Optional

- [ ] **Enable Stolen Device Protection (iOS 17.3+)**
  - Settings > Face ID & Passcode > Stolen Device Protection
  - See: [Stolen Device Protection](../ios/stolen-device-protection.md)

- [ ] **Enable Identity Check (Android 15+, Pixel/Samsung)**
  - Settings > Security > Identity Check
  - See: [Identity Check](../android/identity-check.md)

- [ ] **Consider purchasing device insurance or enrolling in a protection plan**
  - AppleCare+ includes theft and loss coverage (optional add-on)
  - Carrier insurance plans cover accidental loss

- [ ] **Enable anti-theft features on Samsung devices (Samsung Knox / Find My Mobile)**
  - Settings > Biometrics and security > Find My Mobile
  - Enable Reactivation Lock for additional FRP protection

---

## Review Schedule

Security configurations become outdated. Review this checklist:
- When you get a new device
- When you update to a major OS version
- At minimum: **every 6 months**

---

## Related Documents

- [Android Hardening Checklist](android-hardening-checklist.md)
- [iOS Hardening Checklist](ios-hardening-checklist.md)
- [Emergency Checklist](emergency-checklist.md)
- [SIM Security](../hardening/sim-security.md)

---

*Last Updated: 2026-06-01*
