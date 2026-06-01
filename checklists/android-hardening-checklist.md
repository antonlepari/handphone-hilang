# Android Hardening Checklist

> Last Updated: 2026-06-01

This checklist covers 40+ configuration items for hardening an Android device against loss, theft, and unauthorized access. Items are organized by category. Applicable Android version is noted where behavior differs.

---

## Lock Screen and Authentication

- [ ] **Set screen lock type to PIN (6+ digits), password, or alphanumeric passphrase**
  - Settings > Security > Screen lock
  - Avoid: Swipe, Pattern (easily observed), Face unlock alone on lower-security devices

- [ ] **Set screen lock timeout to 30 seconds**
  - Settings > Display > Screen timeout (or Lock screen > Screen lock timeout)

- [ ] **Disable "Show notifications when locked"** for sensitive apps
  - Settings > Notifications > [App] > On Lock Screen > Don't show notifications

- [ ] **Disable "Show notification content on lock screen"** globally
  - Settings > Notifications > Notification privacy > Hide notification content

- [ ] **Enable "Lock network and security" on lock** (prevents Wi-Fi/Bluetooth changes from lock screen)
  - Settings > Security > More security settings > Network security

- [ ] **Disable smart lock features** unless absolutely needed
  - Smart Lock (trusted devices, trusted places) reduces security; disable if not required
  - Settings > Security > More security settings > Smart Lock

- [ ] **Enable "Erase data after failed attempts"**
  - Android: Settings > Security > Automatically lock OR check manufacturer-specific setting

---

## Biometrics

- [ ] **Enroll fingerprint authentication**
  - Settings > Security > Fingerprint

- [ ] **Review and understand biometric fallback**
  - Biometrics fall back to PIN — ensure PIN is strong (see above)
  - Enable Identity Check (Android 15+) to block passcode fallback away from home

- [ ] **Disable "Wake up screen" for face unlock** on low-security devices
  - Face recognition on Android without a secure sensor (IR + depth) can be spoofed with a photo

- [ ] **Re-enroll biometrics after a new OS update** if prompted (ensures calibration accuracy)

---

## Find Hub and Anti-Theft

- [ ] **Enable Find My Device / Find Hub**
  - Settings > Security > Find My Device > Enable
  - Or: Settings > Google > Find My Device

- [ ] **Verify Find Hub works**: log in at https://android.com/find from another device

- [ ] **Enable Offline Device Finding** in Find Hub app
  - Find Hub > Device settings > Store location > With network in all areas

- [ ] **Enable Theft Detection Lock** (Android 10+)
  - Settings > Security > Theft protection > Theft Detection Lock

- [ ] **Enable Offline Device Lock** (Android 10+)
  - Settings > Security > Theft protection > Offline Device Lock

- [ ] **Enable Remote Lock** (Android 10+)
  - Settings > Security > Theft protection > Remote Lock

- [ ] **Enable Identity Check** (Android 15+, Pixel and Samsung Galaxy)
  - Settings > Security & privacy > More security & privacy > Identity Check

---

## Google Account Security

- [ ] **Enable 2-Step Verification on Google Account**
  - https://myaccount.google.com/security > 2-Step Verification > Turn On

- [ ] **Use authenticator app or Google Prompt for 2FA** (not SMS)

- [ ] **Review and remove unknown trusted devices**
  - https://myaccount.google.com/device-activity

- [ ] **Download and store backup codes offline**
  - https://myaccount.google.com/two-step-verification/backup-codes

- [ ] **Set a recovery email that uses a different provider and has its own 2FA**

- [ ] **Complete Google Security Checkup**
  - https://myaccount.google.com/security-checkup

---

## App Permissions Management

- [ ] **Audit location permissions for all apps**
  - Settings > Privacy > Permission manager > Location
  - Change all non-essential apps from "Always" to "Only while using" or "Deny"

- [ ] **Revoke microphone access for apps that don't need it**
  - Settings > Privacy > Permission manager > Microphone

- [ ] **Revoke camera access for apps that don't need it**
  - Settings > Privacy > Permission manager > Camera

- [ ] **Revoke Contacts access for apps that don't need it**
  - Settings > Privacy > Permission manager > Contacts

- [ ] **Review Notification access** — only grant to trusted apps
  - Settings > Privacy > Permission manager > Notifications

- [ ] **Review "Display over other apps" permission** — remove from non-trusted apps
  - Settings > Apps > Special app access > Display over other apps

- [ ] **Review "Install unknown apps" permission** — all should be disabled unless necessary
  - Settings > Apps > Special app access > Install unknown apps

---

## Network Security

- [ ] **Disable "Connect to open networks" / auto-connect to public Wi-Fi**
  - Settings > Network & internet > Wi-Fi > Wi-Fi preferences > Connect to public networks: Off

- [ ] **Set Wi-Fi MAC address to randomized** (per-network) to prevent location tracking
  - Settings > Network & internet > Wi-Fi > [Network] > Privacy > Use randomized MAC (Android 10+)

- [ ] **Install and use a reputable VPN** for public Wi-Fi usage
  - Options: Mullvad, ProtonVPN (no-log, audited providers)

- [ ] **Enable Private DNS**
  - Settings > Network & internet > Private DNS > Automatic or set to dns.google or 1dot1dot1dot1.cloudflare-dns.com

- [ ] **Disable Bluetooth when not in use**
  - Quick Settings or Settings > Bluetooth

---

## Play Protect and App Security

- [ ] **Verify Play Protect is enabled and up to date**
  - Play Store > Profile > Play Protect > Status should show "No harmful apps found"

- [ ] **Run a manual Play Protect scan**
  - Play Store > Profile > Play Protect > Scan

- [ ] **Enable "Improve harmful app detection"**
  - Play Store > Profile > Play Protect > Settings > Improve harmful app detection

- [ ] **Remove apps you don't use or recognize**
  - Settings > Apps > See all apps > uninstall unused apps

- [ ] **Do not install apps from outside the Play Store** unless absolutely necessary

- [ ] **Review apps that have Device Administrator access**
  - Settings > Security > Device admin apps > Remove any you don't recognize

---

## Developer Options (Disable Unless You Are a Developer)

- [ ] **Disable USB debugging**
  - Settings > System > Developer options > USB debugging: Off
  - If Developer options is not visible, it is disabled by default (preferred)

- [ ] **Disable "OEM unlocking"**
  - Settings > System > Developer options > OEM unlocking: Off
  - If enabled, allows bootloader unlock which bypasses FRP

- [ ] **Disable "Mock locations"**
  - Settings > System > Developer options > Select mock location app: None

- [ ] **Disable Developer options entirely** if you don't need them
  - Settings > System > Developer options > toggle Off (at top of Developer options screen)

---

## SIM and Factory Reset Protection

- [ ] **Enable SIM PIN**
  - Settings > Security > SIM card lock > Enable

- [ ] **Set carrier account PIN / port-out lock**
  - Contact carrier directly or via carrier app

- [ ] **Verify Google Account is signed in** (activates FRP)
  - Settings > Accounts > Google

- [ ] **For Samsung: Enable Reactivation Lock**
  - Settings > Biometrics and security > Find My Mobile > Reactivation lock: Enable

---

## Backup

- [ ] **Enable Google Backup**
  - Settings > Google > Backup > Back up to Google Drive: Enable

- [ ] **Verify backup is current**
  - Settings > Google > Backup > Last backup: check timestamp

- [ ] **Enable Google Photos backup for photos and videos**
  - Google Photos > Profile > Google Photos settings > Backup: Enable

- [ ] **For sensitive data: test restoration**
  - Initiate a backup restore on a test device or factory-reset device to verify completeness

---

## Physical Security

- [ ] **Do not use the device where the screen is visible to strangers** when entering PIN
- [ ] **Enable lock immediately after screen off** (not delayed)
  - Settings > Security > Screen lock > Lock after screen timeout: Immediately
- [ ] **Consider a privacy screen protector** to limit screen visibility to on-axis viewing

---

## Related Documents

- [Android Hardening Guide](../hardening/android-hardening.md)
- [Before Loss Prevention](before-loss-prevention.md)
- [Emergency Checklist](emergency-checklist.md)
- [SIM Security](../hardening/sim-security.md)

---

*Last Updated: 2026-06-01*
