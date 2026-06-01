# iOS Hardening Checklist

> Last Updated: 2026-06-01

This checklist covers 40+ configuration items for hardening an iPhone against loss, theft, and unauthorized access. Items are organized by category. iOS version requirements are noted where behavior differs.

---

## Face ID / Touch ID

- [ ] **Enroll Face ID or Touch ID**
  - Settings > Face ID & Passcode (or Touch ID & Passcode)

- [ ] **Enable Face ID / Touch ID for**: iPhone Unlock, iTunes & App Store, Apple Pay, Password AutoFill, Wallet & Apple Pay
  - Settings > Face ID & Passcode > check all desired options

- [ ] **Enable Stolen Device Protection (iOS 17.3+)**
  - Settings > Face ID & Passcode > Stolen Device Protection > Turn On Protection
  - See: [Stolen Device Protection](../ios/stolen-device-protection.md)

- [ ] **Enable Significant Locations** (required for Stolen Device Protection)
  - Settings > Privacy & Security > Location Services > System Services > Significant Locations: On

- [ ] **Do not use "Accessibility" attention features bypass** — ensure face attention detection is on
  - Settings > Face ID & Passcode > Require Attention for Face ID: On

---

## Screen Lock and Passcode

- [ ] **Set a strong passcode (6+ digits or alphanumeric)**
  - Settings > Face ID & Passcode > Change Passcode > Passcode Options > Custom Alphanumeric Code

- [ ] **Set Auto-Lock to 30 seconds**
  - Settings > Display & Brightness > Auto-Lock > 30 Seconds

- [ ] **Enable "Erase Data" after 10 failed passcode attempts**
  - Settings > Face ID & Passcode > Erase Data: Toggle On

- [ ] **Disable access to certain features from lock screen** for sensitive items
  - Settings > Face ID & Passcode > Allow Access When Locked:
    - Today View: Off (if widgets show sensitive info)
    - Notification Center: Off (optional — prevents reading notifications)
    - Siri: Off (optional — prevents Siri lock screen queries)
    - Return Missed Calls: evaluate based on personal preference
    - USB Accessories: Off (prevents USB data access without unlock — requires "USB Accessories" to be Off)

- [ ] **Disable USB Accessories access from lock screen**
  - Settings > Face ID & Passcode > USB Accessories: Off
  - Prevents data extraction via USB if device is locked for more than 1 hour

---

## Find My

- [ ] **Enable Find My iPhone**
  - Settings > [Your Name] > Find My > Find My iPhone: On

- [ ] **Enable Offline Finding**
  - Settings > [Your Name] > Find My > Find My iPhone > Enable Offline Finding: On

- [ ] **Enable Send Last Location**
  - Settings > [Your Name] > Find My > Find My iPhone > Send Last Location: On

- [ ] **Verify Find My at https://icloud.com/find** from another device

---

## Apple ID and iCloud Security

- [ ] **Enable Two-Factor Authentication on Apple ID**
  - Settings > [Your Name] > Sign-In & Security > Two-Factor Authentication: Turn On

- [ ] **Set up a Recovery Contact**
  - Settings > [Your Name] > Sign-In & Security > Account Recovery > Recovery Contact

- [ ] **Generate and store a Recovery Key**
  - Settings > [Your Name] > Sign-In & Security > Recovery Key
  - Store key in a physically secure, offline location

- [ ] **Review and remove unknown trusted devices from Apple ID**
  - Settings > [Your Name] > scroll to Devices > review each

- [ ] **Review trusted phone numbers** for 2FA
  - Settings > [Your Name] > Sign-In & Security > Trusted Phone Numbers

- [ ] **Enable iCloud Backup** (daily, automatic)
  - Settings > [Your Name] > iCloud > iCloud Backup > Back Up Now / enable automatic

- [ ] **Review which apps have iCloud access**
  - Settings > [Your Name] > iCloud > [App list] — disable sync for sensitive apps if desired

---

## App Permissions

- [ ] **Audit Location permissions for all apps**
  - Settings > Privacy & Security > Location Services > review each app
  - Change "Always" to "While Using" for apps that don't need background location

- [ ] **Review Microphone access**
  - Settings > Privacy & Security > Microphone — remove access from unused apps

- [ ] **Review Camera access**
  - Settings > Privacy & Security > Camera — remove access from unused apps

- [ ] **Review Contacts access**
  - Settings > Privacy & Security > Contacts — limit to apps that genuinely need it

- [ ] **Review Health data access**
  - Settings > Privacy & Security > Health — limit to explicitly trusted health apps

- [ ] **Enable App Privacy Report** to monitor actual permission usage
  - Settings > Privacy & Security > App Privacy Report: Turn On

---

## Network Security

- [ ] **Enable "Limit IP Address Tracking"** in Wi-Fi settings
  - Settings > Wi-Fi > [Network] > Limit IP Address Tracking: On

- [ ] **Use Private Wi-Fi Address** for each network
  - Settings > Wi-Fi > [Network] > Private Wi-Fi Address: On

- [ ] **Disable "Auto-Join" for public/untrusted networks**
  - Settings > Wi-Fi > [Network] > Auto-Join: Off for public networks

- [ ] **Use a reputable VPN on untrusted networks**

- [ ] **Enable iCloud Private Relay** (requires iCloud+ subscription)
  - Settings > [Your Name] > iCloud > Private Relay: On

---

## Safari and Browser Security

- [ ] **Enable "Fraudulent Website Warning"** in Safari
  - Settings > Safari > Fraudulent Website Warning: On

- [ ] **Enable "Prevent Cross-Site Tracking"**
  - Settings > Safari > Prevent Cross-Site Tracking: On

- [ ] **Enable "Hide IP Address" in Safari**
  - Settings > Safari > Hide IP Address: From Trackers

- [ ] **Block all cookies from trackers**
  - Settings > Safari > Cross-Site Tracking Prevention is covered by "Prevent Cross-Site Tracking"

- [ ] **Enable Mail Privacy Protection** (iOS 15+)
  - Settings > Mail > Privacy Protection > Protect Mail Activity: On

---

## Siri Privacy

- [ ] **Disable "Allow Siri When Locked"** if you don't need lock-screen Siri
  - Settings > Face ID & Passcode > Siri: Off

- [ ] **Disable "Show Siri Suggestions"** for sensitive app categories
  - Settings > Siri & Search > [App] > Show Siri Suggestions: Off

- [ ] **Review "Hey Siri" — disable if not needed**
  - Settings > Siri & Search > Listen for "Hey Siri": Off (prevents voice activation when device is on a table)

---

## Screen Time and Restrictions

- [ ] **Enable Screen Time with a separate passcode** (different from device passcode)
  - Settings > Screen Time > Use Screen Time Passcode
  - This prevents thieves with the device passcode from disabling restrictions

- [ ] **Enable "Account Changes" restriction** under Content & Privacy Restrictions
  - Settings > Screen Time > Content & Privacy Restrictions > Account Changes: Don't Allow
  - Prevents account email/password changes without Screen Time passcode

- [ ] **Enable "Passcode Changes" restriction** (prevents changing device passcode)
  - Settings > Screen Time > Content & Privacy Restrictions > Passcode Changes: Don't Allow

- [ ] **Enable "Location Services" restriction**
  - Settings > Screen Time > Content & Privacy Restrictions > Privacy > Location Services: Don't Allow Changes

---

## SIM Security

- [ ] **Enable SIM PIN**
  - Settings > Cellular > SIM PIN > Enable

- [ ] **Set carrier account PIN and port-out lock** (see carrier-specific steps)
  - See: [SIM Security](../hardening/sim-security.md)

---

## Additional Hardening

- [ ] **Update iOS to the latest version**
  - Settings > General > Software Update

- [ ] **Enable automatic updates**
  - Settings > General > Software Update > Automatic Updates: On

- [ ] **Review recently installed apps** for anything unfamiliar
  - Settings > General > iPhone Storage > review apps and last used dates

- [ ] **Consider Lockdown Mode** for high-risk users (journalists, executives, activists)
  - Settings > Privacy & Security > Lockdown Mode
  - Dramatically restricts attack surface but limits some device functionality

---

## Recovery Preparation

- [ ] **Apple ID password memorized or in offline-accessible password manager**
- [ ] **Recovery Key stored physically in secure location**
- [ ] **Recovery Contact set up and confirmed**
- [ ] **Device IMEI recorded** (Settings > General > About > IMEI)
- [ ] **Original purchase receipt saved** (in secure email or physical copy)

---

## Related Documents

- [iOS Hardening Guide](../hardening/ios-hardening.md)
- [Before Loss Prevention](before-loss-prevention.md)
- [Emergency Checklist](emergency-checklist.md)
- [SIM Security](../hardening/sim-security.md)
- [Stolen Device Protection](../ios/stolen-device-protection.md)

---

*Last Updated: 2026-06-01*
