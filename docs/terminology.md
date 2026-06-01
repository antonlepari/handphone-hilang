# Terminology

> Last Updated: 2026-06-01

This glossary defines key terms used throughout the Mobile Device Loss & Theft Response Playbook. Terms are listed alphabetically.

---

## A

**Activation Lock**
An Apple security feature that ties an iPhone, iPad, or Apple Watch to its associated Apple ID. Even after a factory reset, the device requires the original Apple ID credentials to be reactivated. Automatically enabled when Find My is turned on.
*See: [Activation Lock](../ios/activation-lock.md)*

**ADB (Android Debug Bridge)**
A command-line tool that allows communication with an Android device. Used in development and forensics. If USB debugging is enabled on a stolen device, ADB can be used to extract data.
*Reference: https://developer.android.com/tools/adb*

**Authenticator App**
A software application that generates time-based one-time passwords (TOTP) for two-factor authentication. Examples: Google Authenticator, Microsoft Authenticator, Authy. More secure than SMS-based 2FA for account recovery.

---

## B

**Biometric Authentication**
Authentication using physical characteristics — fingerprint (Touch ID), facial geometry (Face ID), or iris scan. Used on both Android and iOS devices for device unlock and sensitive action authorization.

**BYOD (Bring Your Own Device)**
A policy allowing employees to use their personal smartphones for work purposes. Creates security challenges around data segregation, remote wipe authority, and MDM enrollment.

---

## C

**Carrier Account PIN**
A unique PIN set with a mobile carrier to prevent unauthorized account changes, SIM swaps, or number port-outs. Distinct from the device PIN. Also called an "account passcode."

**COPE (Corporate Owned, Personally Enabled)**
A device ownership model where the organization owns the device but allows personal use. The organization retains full MDM control, including remote wipe.

**CYOD (Choose Your Own Device)**
A model where employees select from a pre-approved list of devices purchased by the organization.

---

## D

**Data at Rest**
Data stored on the device's internal storage or SD card. Modern Android (Android 10+) and iOS (iOS 8+) devices encrypt data at rest by default using AES-256 or equivalent.

**Data in Transit**
Data transmitted over networks (Wi-Fi, cellular, Bluetooth). Should be protected using TLS/HTTPS.

---

## E

**eSIM (Embedded SIM)**
A SIM card that is embedded into the device hardware and cannot be physically removed. Provides enhanced protection against SIM theft-based attacks. Supports multiple carrier profiles.

**Encryption**
The process of encoding data so it can only be read with the correct decryption key. Both Android and iOS encrypt device storage by default when a passcode is set.

---

## F

**Factory Reset Protection (FRP)**
An Android security feature (Android 5.1+) that requires the original Google account credentials after a factory reset performed via recovery mode or hardware buttons. Prevents a thief from wiping and reusing the device.
*See: [Factory Reset Protection](../android/factory-reset-protection.md)*

**Find Hub**
Google's device tracking platform, formerly called "Find My Device." Renamed in May 2025. Uses a crowdsourced network of over one billion Android devices to locate lost phones, tablets, earbuds, and tags via Bluetooth even when offline.
*See: [Find Hub](../android/find-my-device.md)*

**Find My**
Apple's device and item tracking platform for iPhone, iPad, Mac, Apple Watch, and AirTags. Uses end-to-end encrypted crowdsourced Bluetooth signals to locate devices offline.
*See: [Find My](../ios/find-my.md)*

**Forensic Extraction**
The process of extracting digital evidence from a device using specialized tools. Relevant in both criminal investigations and incident response contexts.

---

## G

**Google Account**
The primary identity and authentication mechanism for Android devices. Controls access to Gmail, Google Drive, Play Store, Find Hub, and device backups.

---

## I

**Identity Check**
An Android security feature introduced in January 2025 (Android 15+, Pixel and Samsung Galaxy). Requires biometric authentication (fingerprint or face) — with no passcode fallback — to access sensitive settings when the device is away from trusted locations.
*See: [Identity Check](../android/identity-check.md)*

**IMEI (International Mobile Equipment Identity)**
A unique 15-digit number assigned to every mobile device. Used to identify a specific device on a cellular network. Carriers can block a stolen device using its IMEI. Find this in Settings > About Phone, or by dialing `*#06#`.

**IMSI (International Mobile Subscriber Identity)**
A unique identifier stored on a SIM card that identifies the subscriber on a cellular network. Distinct from IMEI.

**Incident Response (IR)**
A structured methodology for managing the aftermath of a security breach or compromise. In the context of device loss, IR covers containment, eradication, recovery, and lessons learned.

**IOC (Indicator of Compromise)**
Forensic artifacts — file hashes, IP addresses, domains, behavioral patterns — that indicate a system has been compromised. Used by tools like MVT to detect spyware.

---

## L

**Lost Mode**
An iOS feature that locks a device and displays a custom message (including contact information) on the lock screen. Enables location tracking for the device. Prevents Apple Pay use. Does not erase data.
*See: [Lost Mode](../ios/lost-mode.md)*

---

## M

**MDM (Mobile Device Management)**
Software used by organizations to manage, configure, monitor, and remotely control mobile devices. Examples: Microsoft Intune, Jamf, VMware Workspace ONE.
*See: [MDM Enterprise](../hardening/mdm-enterprise.md)*

**MITRE ATT&CK Mobile Matrix**
A knowledge base of adversary tactics, techniques, and procedures (TTPs) specifically for mobile platforms (Android and iOS). Used to map threat scenarios to known attack patterns.
*Reference: https://attack.mitre.org/matrices/mobile/*

**MVT (Mobile Verification Toolkit)**
An open-source forensics tool developed by Amnesty International Security Lab to detect signs of device compromise, including spyware like Pegasus.
*See: [Recommended Tools](../tools/recommended-tools.md)*

---

## O

**OTP (One-Time Password)**
A temporary, single-use password used for authentication. Can be delivered via SMS, email, or generated by an authenticator app. SMS-based OTPs are vulnerable to SIM swap attacks.

---

## P

**Passkey**
A FIDO2-compliant authentication credential stored on a device. Replaces passwords with cryptographic key pairs. Cannot be phished, reused, or stolen via data breach. Supported on both Android and iOS.

**PIN (Personal Identification Number)**
A numeric code used to unlock a device. Minimum 4 digits (not recommended), ideally 6 digits or more, or replaced with an alphanumeric passphrase.

**Play Protect**
Google's built-in malware scanning service for Android. Scans apps at install time and continuously after installation. Analyzes over 200 billion apps daily across the Play Store and sideloaded apps.
*See: [Play Protect](../android/play-protect.md)*

**Port Freeze / Port-Out Lock**
A carrier security feature that prevents a phone number from being transferred (ported) to another carrier without the account owner's explicit approval. Key defense against SIM swap attacks.

---

## R

**Remote Wipe**
The ability to erase all data on a device remotely, typically via a cloud service (Find Hub or Find My) or MDM platform. Used as a last resort when device recovery is not possible and data protection is the priority.

**Recovery Key (Apple)**
A 28-character key generated when enabling Advanced Data Protection or two-factor authentication for Apple ID. Used to regain account access if locked out. Must be stored securely offline.

**Recovery Contact (Apple)**
A trusted person who can provide a recovery code to help regain access to an Apple ID. The contact does not gain access to the account's data.

---

## S

**SIM Card (Subscriber Identity Module)**
A small card that stores subscriber identity information and provides cellular connectivity. Physical SIMs can be removed from stolen devices; eSIMs cannot.

**SIM PIN**
A separate PIN used to lock the SIM card itself. If enabled, the SIM PIN is required when the SIM is inserted into a new device or after a device restart. Distinct from the device lock PIN.

**SIM Swap Attack**
A social engineering attack where a criminal convinces a carrier to transfer a victim's phone number to a SIM card controlled by the attacker. Enables bypass of SMS-based 2FA.
*See: [SIM Security](../hardening/sim-security.md)*

**Spyware**
Malware designed to monitor and exfiltrate data from a device without the owner's knowledge. Advanced examples include Pegasus (NSO Group), designed to target journalists and activists.

**Stolen Device Protection**
An iOS 17.3+ security feature that adds biometric authentication requirements (with no passcode fallback) for sensitive actions when the iPhone is in an unfamiliar location. Also imposes a one-hour delay before certain critical security changes.
*See: [Stolen Device Protection](../ios/stolen-device-protection.md)*

---

## T

**Theft Detection Lock**
An Android 10+ security feature that uses on-device AI (accelerometer, gyroscope, Wi-Fi, Bluetooth) to detect motion patterns consistent with a snatch theft and automatically lock the device screen.

**TOTP (Time-Based One-Time Password)**
A 2FA mechanism that generates a new 6-8 digit code every 30 seconds using a shared secret and the current time. Used by authenticator apps. More secure than SMS OTPs.

**Trusted Location**
A location (home, office) registered in Android's Identity Check or iOS's Stolen Device Protection where relaxed security requirements apply. Outside trusted locations, stronger authentication is enforced.

---

## U

**USB Debugging**
An Android developer feature that allows a computer to send commands to an Android device via USB using ADB. Should be disabled on non-development devices, as it enables data extraction if left enabled.

**UWB (Ultra-Wideband)**
A short-range wireless technology that provides centimeter-level location precision. Used in Apple's Find My with AirTags and in Android's Find Hub for precise item location. Available on newer Pixel and Samsung devices.

---

## V

**VPN (Virtual Private Network)**
An encrypted tunnel between a device and a server that protects internet traffic from interception. Recommended for use on public Wi-Fi networks.

---

*Last Updated: 2026-06-01*
