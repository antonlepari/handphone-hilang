# Mobile Device Loss & Theft Response Playbook

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Platform: Android](https://img.shields.io/badge/Platform-Android-green.svg)
![Platform: iOS](https://img.shields.io/badge/Platform-iOS-blue.svg)
![Last Updated](https://img.shields.io/badge/Last%20Updated-2026--06--01-brightgreen)
![OWASP](https://img.shields.io/badge/References-OWASP%20%7C%20NIST%20%7C%20CISA-red)

> **The most comprehensive open-source playbook for responding to lost or stolen smartphones — covering mitigation, prevention, incident response, recovery, and security hardening for Android and iOS.**

---

## Who This Repository Is For

| Audience | How to Use This Repository |
|---|---|
| **General Users** | Start with the [Emergency Checklist](checklists/emergency-checklist.md) and [Before Loss Prevention](checklists/before-loss-prevention.md) |
| **Security Professionals** | See [Threat Models](threat-models/) and [Incident Response Playbooks](incident-response/) |
| **SOC Analysts** | See [Corporate Device Response](incident-response/corporate-device-response.md) and [Risk Matrix](threat-models/risk-matrix.md) |
| **Digital Forensics Practitioners** | See [Tools](tools/recommended-tools.md) and [Attack Scenarios](threat-models/attack-scenarios.md) |
| **IT Administrators** | See [MDM & Enterprise](hardening/mdm-enterprise.md) and [Android/iOS Hardening Guides](hardening/) |
| **Corporate Teams** | See [Incident Report Template](templates/incident-report-template.md) and [Corporate Device Response](incident-response/corporate-device-response.md) |
| **Students & Researchers** | See [Threat Landscape](docs/threat-landscape.md), [References](references/), and [Terminology](docs/terminology.md) |

---

## Quick-Start Emergency Checklist

> **⚠️ WARNING:** If your device was just lost or stolen, take these 5 actions immediately — in order.

1. **Open Find My Device / Find My** on a computer or another phone and check the last known location
2. **Enable Lost Mode / Remote Lock** to display your contact information and prevent unauthorized access
3. **Log out of all active sessions** from your Google Account or Apple ID via a web browser
4. **Call your mobile carrier** to suspend your SIM card and prevent unauthorized calls, SMS, and data usage
5. **Change your most critical passwords** — email first, then banking — from a trusted device

For the complete emergency procedure, see [Emergency Checklist](checklists/emergency-checklist.md) and [First 5 Minutes](incident-response/first-5-minutes.md).

---

## Repository Purpose & Scope

This repository documents everything you need to know about smartphone security loss events — before they happen, during the event, and after. It covers:

- **Prevention**: Security hardening before a loss event occurs
- **Incident Response**: Step-by-step procedures from the first 5 minutes through the first week
- **Recovery**: Restoring accounts, data, and trust after device loss or theft
- **Threat Intelligence**: Attack scenarios mapped to MITRE ATT&CK Mobile Matrix
- **Enterprise Guidance**: Corporate device policy and MDM considerations
- **Forensics Tools**: Professional tools for digital forensics practitioners

This is a living document maintained with references to official vendor documentation (Apple, Google, Samsung), NIST, OWASP, CISA, ENISA, and MITRE ATT&CK.

---

## Table of Contents

### Documentation
- [Overview](docs/overview.md)
- [Threat Landscape](docs/threat-landscape.md)
- [Terminology](docs/terminology.md)

### Android
- [Android Overview](android/README.md)
- [Find Hub (formerly Find My Device)](android/find-my-device.md)
- [Factory Reset Protection](android/factory-reset-protection.md)
- [Google Account Security](android/google-account-security.md)
- [Play Protect](android/play-protect.md)
- [Identity Check](android/identity-check.md)

### iOS
- [iOS Overview](ios/README.md)
- [Find My](ios/find-my.md)
- [Lost Mode](ios/lost-mode.md)
- [Activation Lock](ios/activation-lock.md)
- [Stolen Device Protection](ios/stolen-device-protection.md)
- [Apple ID Recovery](ios/apple-id-recovery.md)

### Checklists
- [Checklists Overview](checklists/README.md)
- [Before Loss — Prevention Checklist](checklists/before-loss-prevention.md)
- [Android Hardening Checklist](checklists/android-hardening-checklist.md)
- [iOS Hardening Checklist](checklists/ios-hardening-checklist.md)
- [Emergency Checklist](checklists/emergency-checklist.md)

### Incident Response
- [Incident Response Overview](incident-response/README.md)
- [Playbook Overview & Flowchart](incident-response/playbook-overview.md)
- [First 5 Minutes](incident-response/first-5-minutes.md)
- [First 30 Minutes](incident-response/first-30-minutes.md)
- [First Hour](incident-response/first-hour.md)
- [First 24 Hours](incident-response/first-24-hours.md)
- [First Week](incident-response/first-week.md)
- [Corporate Device Response](incident-response/corporate-device-response.md)

### Security Hardening
- [Hardening Overview](hardening/README.md)
- [Android Hardening Guide](hardening/android-hardening.md)
- [iOS Hardening Guide](hardening/ios-hardening.md)
- [SIM Security](hardening/sim-security.md)
- [MDM & Enterprise](hardening/mdm-enterprise.md)

### Threat Models
- [Threat Models Overview](threat-models/README.md)
- [Threat Model Overview](threat-models/threat-model-overview.md)
- [Attack Scenarios](threat-models/attack-scenarios.md)
- [Risk Matrix](threat-models/risk-matrix.md)

### Tools
- [Tools Overview](tools/README.md)
- [Recommended Tools](tools/recommended-tools.md)

### References
- [References Overview](references/README.md)
- [Citations](references/citations.md)

### Templates
- [Templates Overview](templates/README.md)
- [Incident Report Template](templates/incident-report-template.md)
- [Police Report Template](templates/police-report-template.md)
- [Carrier Notification Template](templates/carrier-notification-template.md)

---

## Contributing

Contributions are welcome. To contribute:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-contribution`
3. Make your changes following the existing document structure
4. Ensure all references are from official, authoritative sources
5. Submit a pull request with a clear description

Please do not add unverified statistics, vendor-biased claims, or links to unofficial/unreliable sources.

---

## License

This repository is licensed under the **MIT License**. See [LICENSE](LICENSE) for details.

You are free to use, modify, and distribute this content with attribution.

---

*Last Updated: 2026-06-01 | Maintained by the open-source security community*
