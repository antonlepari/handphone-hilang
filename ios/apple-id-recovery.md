# Apple ID Recovery

> Last Updated: 2026-06-01

## Overview

If your iPhone is stolen and the thief manages to change your Apple ID password, or if you lose access to your Apple ID for any reason, you need a recovery pathway to regain control. Apple provides several account recovery mechanisms, which must be configured **before** a loss event to be useful.

*Reference: https://support.apple.com/en-us/111573*

---

## Apple ID Recovery Mechanisms

### 1. Two-Factor Authentication (Primary Defense)

Two-factor authentication (2FA) is the foundational security layer. With 2FA enabled:
- Signing in requires your password + a verification code from a trusted device or phone number
- A thief with only your password cannot sign in without access to a trusted device

**Enabling 2FA:**
1. Settings > [Your Name] > Sign-In & Security
2. Tap **Two-Factor Authentication**
3. Tap **Turn On Two-Factor Authentication**
4. Enter a trusted phone number

> **⚠️ WARNING:** The trusted phone number should not be the number on the stolen device (the thief can receive SMS codes). Add a secondary trusted number (family member's phone, second phone number) or remove SMS entirely and use hardware keys.

### 2. Recovery Key

A **Recovery Key** is a 28-character alphanumeric key that replaces the standard account recovery process. When you set up a Recovery Key:
- Standard account recovery (via Apple's servers and identity verification) is disabled
- The Recovery Key becomes the only way to recover your account if you lose access to trusted devices and your trusted phone number
- **If you lose both your devices AND your Recovery Key, your account cannot be recovered**

**Setting up a Recovery Key:**
1. Settings > [Your Name] > Sign-In & Security
2. Tap **Recovery Key**
3. Toggle Recovery Key to **On**
4. Enter your device passcode
5. Write down the 28-character key
6. Confirm the key by typing it in
7. Store the key **offline and securely** — not in a cloud service, not on the stolen device

> **⚠️ WARNING:** The Recovery Key provides strong protection but also removes Apple's ability to help you regain access if you lose all trusted devices. Store it in a physical safe, with a trusted person, or in a printed sealed envelope.

### 3. Recovery Contact

A **Recovery Contact** is a trusted person (friend, family member) who can provide you with a recovery code to regain account access. Unlike account sharing, a Recovery Contact does not gain any access to your account data — they simply receive a code to hand to you.

**Setting up a Recovery Contact:**
1. Settings > [Your Name] > Sign-In & Security
2. Tap **Account Recovery**
3. Tap **Add Recovery Contact**
4. Select the contact (must be in your contacts and have an Apple device)
5. The contact receives a request and must accept

**How it works:**
- If you are locked out, go to https://iforgot.apple.com
- Select "Recovery Contact"
- Your designated Recovery Contact receives a code on their Apple device
- They share the code with you
- You use the code to regain access

> **💡 TIP:** Choose a Recovery Contact who:
> - You trust completely with account access procedures
> - Has their own Apple device with 2FA enabled
> - Is easily reachable by phone or in person

---

## What to Do After Theft: Apple ID Recovery Steps

### If the Thief Has NOT Changed Your Apple ID Password

You still have control — act immediately:

1. **From another device or computer:**
   - Go to https://www.icloud.com/find
   - Lock the stolen device via Find My > Mark as Lost
   - OR erase it if recovery is impossible

2. **Change your Apple ID password:**
   - Go to https://appleid.apple.com
   - Sign in
   - Go to **Sign-In & Security > Password**
   - Change the password
   - Choose a strong, unique password not used elsewhere

3. **Review trusted devices:**
   - Go to https://appleid.apple.com
   - Scroll down to "Devices"
   - Remove the stolen device from trusted devices

4. **Review trusted phone numbers:**
   - Under Sign-In & Security > Trusted Phone Numbers
   - Remove any phone numbers on the stolen device if that number may be compromised

### If the Thief HAS Changed Your Apple ID Password (Account Takeover)

This is a more severe scenario. Options depend on what recovery mechanisms were set up:

**Option A: Recovery Key**
1. Go to https://iforgot.apple.com
2. Enter your Apple ID
3. Select "Use Recovery Key"
4. Enter the 28-character Recovery Key
5. Enter a trusted phone number verification code
6. Reset your password

**Option B: Recovery Contact**
1. Go to https://iforgot.apple.com
2. Enter your Apple ID
3. Select "Get help from a recovery contact"
4. Notify your Recovery Contact
5. They receive a code on their Apple device
6. Use the code + their guidance to recover

**Option C: Account Recovery Request (Slow — 24 hours to several days)**
If no Recovery Key or Recovery Contact was set up:
1. Go to https://iforgot.apple.com
2. Enter your Apple ID
3. Apple initiates an **Account Recovery** process
4. This involves identity verification and may take 1–7 days
5. If a thief has recently changed trusted devices/numbers, Apple imposes a waiting period

> **⚠️ WARNING:** The Account Recovery Request process can be delayed if someone recently changed security settings on the account (i.e., the attacker may have already initiated recovery changes). This is why Recovery Key and Recovery Contact setup beforehand is critical.

**Option D: Contact Apple Support**
1. Go to https://support.apple.com
2. Select "Apple ID" > "Forgot Apple ID or password"
3. Or visit an Apple Store with government-issued photo ID and proof of purchase
4. Apple Support can verify identity through official documents and remove Activation Lock/restore access in verified ownership cases

---

## Setting Up Recovery BEFORE a Loss Event

### Recovery Checklist

- [ ] Two-Factor Authentication enabled on Apple ID
- [ ] Trusted phone number is NOT solely the stolen device's number (add a backup)
- [ ] Recovery Key generated and stored offline (physical copy, secure location)
- [ ] Recovery Contact designated (trusted person, accepted the invitation)
- [ ] Apple ID password memorized or stored in secure, offline-accessible password manager
- [ ] Apple original purchase receipt saved (email archive or physical copy)

---

## Advanced Data Protection (iCloud)

**Advanced Data Protection** extends end-to-end encryption to additional iCloud data categories (iCloud Backup, iCloud Drive, Photos, Notes, Reminders, and more).

**Requirements for Advanced Data Protection:**
- iPhone (or all Apple devices) must be updated to recent iOS
- A Recovery Key or Recovery Contact must be set up (Apple cannot recover your data if you lose access)

**Enabling:**
1. Settings > [Your Name] > iCloud
2. Tap **Advanced Data Protection**
3. Follow prompts to enable

> **⚠️ WARNING:** With Advanced Data Protection, if you lose access to your account without a Recovery Key or Recovery Contact, your iCloud data is permanently inaccessible. The trade-off is significantly stronger privacy and data security. Only enable if you are confident in your recovery mechanism.

---

## Related Documents

- [Find My](find-my.md)
- [Stolen Device Protection](stolen-device-protection.md)
- [Activation Lock](activation-lock.md)
- [iOS Hardening Guide](../hardening/ios-hardening.md)
- [First 30 Minutes](../incident-response/first-30-minutes.md)

---

*Last Updated: 2026-06-01 | Source: https://support.apple.com/en-us/111573 | https://appleid.apple.com*
