# Google Account Security

> Last Updated: 2026-06-01

## Overview

Your Google Account is the master key to your Android device. It controls:
- Find Hub (device tracking and remote wipe)
- Device backups and restore
- Google Drive, Gmail, Google Photos
- Play Store purchases and app installs
- Chrome sync (saved passwords, bookmarks)
- Factory Reset Protection (FRP)

If an attacker gains access to your Google Account, they can disable Find Hub, perform a remote wipe, access your backups, and recover all saved credentials. **Securing your Google Account is as important as securing the device itself.**

*Reference: https://support.google.com/accounts/answer/46892*

---

## Two-Factor Authentication (2FA)

### Enabling 2FA

1. Go to **https://myaccount.google.com/security**
2. Under "How you sign in to Google," click **2-Step Verification**
3. Click **Get started** and follow the prompts
4. Choose your second factor (see options below)

### 2FA Method Comparison

| Method | Security Level | Resistance to SIM Swap | Recommended? |
|---|---|---|---|
| **Hardware Security Key** (YubiKey, Titan) | Highest | Yes — physical possession required | Strongly recommended |
| **Google Prompt** (device notification) | High | Yes — device possession required | Recommended |
| **Authenticator App** (TOTP) | High | Yes — app seed is offline | Recommended |
| **Backup Codes** | Medium | Yes | For emergency backup only |
| **SMS / Phone Call** | Low | No — vulnerable to SIM swap | Not recommended as primary |

> **⚠️ WARNING:** SMS-based 2FA (receiving a code via text message) is the weakest second factor available. SIM swap attacks can intercept SMS codes. If you use SMS 2FA on your Google Account, a SIM swap attack allows an attacker to take over your account — and therefore your device — remotely.

### Switching Away from SMS 2FA

1. Go to **https://myaccount.google.com/two-step-verification**
2. Enroll a hardware key or authenticator app first
3. Remove SMS as a 2FA method

---

## Recovery Options

Recovery options are the mechanism Google uses to verify your identity if you are locked out. They are also the mechanism an attacker exploits if they are not secured.

### Recovery Email

1. Go to **https://myaccount.google.com/recovery/email**
2. Set a recovery email address that uses a **different email provider**
3. That recovery email must also have 2FA enabled
4. Do not use a recovery email that forwards to the same account being protected

### Recovery Phone Number

- Recovery phone number enables SMS-based account recovery
- If your SIM is compromised, so is SMS recovery
- Consider removing your recovery phone number and relying on recovery codes + hardware key instead
- If you keep a recovery phone, use a separate number not associated with the stolen device

### Recovery Codes

1. Go to **https://myaccount.google.com/two-step-verification/backup-codes**
2. Generate backup codes
3. Print or write them down and store in a secure physical location (not in the cloud or on the device)
4. Each code is single-use; regenerate a new set after using one

---

## Trusted Devices

### Reviewing Trusted Devices

1. Go to **https://myaccount.google.com/device-activity**
2. Review all listed devices
3. Remove any unfamiliar or old devices by clicking the device name and selecting **Sign out**

> **💡 TIP:** After a device is lost or stolen, immediately sign it out from this page. This prevents the device from being used to pass Google account 2FA prompts.

---

## Active Sessions

### Reviewing and Revoking Sessions

1. Go to **https://myaccount.google.com/security**
2. Scroll to "Your devices"
3. Select **Manage all devices**
4. For each unfamiliar or lost device: click it and select **Sign out**

For immediate remote session termination:
1. Go to **https://accounts.google.com/b/0/DisplayUnlockCaptcha**
2. Or use **https://myaccount.google.com/notifications** to review recent activity

---

## Google Password Manager

### Checking for Saved Passwords

If your device is stolen while unlocked, any saved passwords in Chrome or Android autofill are accessible. Immediately:

1. Go to **https://passwords.google.com**
2. Review all saved passwords
3. Export or note any passwords for accounts that also appear in the device's browser history
4. Change critical passwords (email, banking, work accounts) immediately

### Removing Saved Passwords Remotely

Passwords in Google Password Manager are cloud-synced. You cannot remotely delete them from the password manager directly, but you can:
1. Change passwords for critical accounts (making saved versions obsolete)
2. Enable Identity Check (Android 15+) which requires biometrics to access saved passwords

---

## Google Account Activity Monitoring

### Security Checkup

1. Go to **https://myaccount.google.com/security-checkup**
2. Review all items flagged under:
   - Recent security events
   - Sign-in and recovery
   - Third-party access
   - Google apps with account access

### Sign-In Activity Review

1. Go to **https://myaccount.google.com/notifications**
2. Review recent sign-in events, particularly:
   - New device sign-ins
   - Password changes
   - Recovery option changes
   - 2FA method changes

---

## Google Advanced Protection Program

For high-risk users (executives, journalists, politicians, security researchers), consider enrolling in **Google's Advanced Protection Program**:

- Requires a physical hardware security key for sign-in
- Blocks all unauthorized apps from accessing Google Account data
- Provides stronger phishing and account takeover protection
- Restricts account recovery to hardware key only

*Enroll at: https://landing.google.com/advancedprotection/*

---

## Post-Theft Immediate Actions

When a device with your Google Account is lost or stolen:

```
IMMEDIATE (first 5 minutes):
1. Go to https://myaccount.google.com/device-activity
2. Sign out the missing device
3. Go to https://android.com/find
4. Lock or erase the device

WITHIN 30 MINUTES:
5. Change your Google Account password
6. Review and revoke any OAuth app access that seems suspicious
7. Download backup codes and store offline

WITHIN 24 HOURS:
8. Change passwords for all accounts accessible via Gmail
9. Check for any emails received/sent after the theft
10. Review Google Drive for any unexpected file access or sharing
```

---

## Related Documents

- [Find Hub](find-my-device.md)
- [Factory Reset Protection](factory-reset-protection.md)
- [Identity Check](identity-check.md)
- [First 5 Minutes](../incident-response/first-5-minutes.md)

---

*Last Updated: 2026-06-01 | Source: https://support.google.com/accounts | https://myaccount.google.com/security*
