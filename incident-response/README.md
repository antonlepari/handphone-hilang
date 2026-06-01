# Incident Response

> Last Updated: 2026-06-01

## Overview

This section provides structured incident response procedures for lost or stolen mobile devices. Procedures are organized by time phase, allowing responders to identify the appropriate actions for their current stage of the incident.

---

## Incident Response Structure

```mermaid
flowchart LR
    A[Device Missing] --> B[First 5 Minutes]
    B --> C[First 30 Minutes]
    C --> D[First Hour]
    D --> E[First 24 Hours]
    E --> F[First Week]
    F --> G[Post-Incident Review]
```

---

## Documents in This Section

| Document | Time Phase | Key Actions |
|---|---|---|
| [Playbook Overview](playbook-overview.md) | Full flow | Complete IR flowchart, decision trees |
| [First 5 Minutes](first-5-minutes.md) | 0–5 min | Locate, lock, log out, alert |
| [First 30 Minutes](first-30-minutes.md) | 5–30 min | Secure accounts, contact carrier, file report |
| [First Hour](first-hour.md) | 30–60 min | IMEI reporting, remote wipe decision, insurance |
| [First 24 Hours](first-24-hours.md) | 1–24 hrs | Full account audit, credit monitoring |
| [First Week](first-week.md) | 1–7 days | New device setup, insurance claim, lessons learned |
| [Corporate Device Response](corporate-device-response.md) | All phases | Enterprise-specific procedures |

---

## Critical Decision: To Wipe or Not to Wipe

One of the most important decisions in a device loss incident is whether to perform a remote wipe. Use this framework:

```
REMOTE WIPE DECISION:

Does the device contain sensitive data?
├── YES: Work emails, client data, credentials, personal finance?
│   └── Is device recovery still possible?
│       ├── YES: Lock first, monitor location, delay wipe
│       └── NO: Wipe immediately
└── NO: Standard personal content only
    └── Is the device insured or replaceable?
        ├── YES: Wipe and claim
        └── NO: Lock and attempt recovery

Corporate devices:
└── Follow MDM/IT policy — do NOT wipe without IT authorization
    (Wiping may destroy forensic evidence needed for investigation)
```

For detailed decision guidance, see [First Hour — Remote Wipe Decision Matrix](first-hour.md).

---

## Terminology

| Term | Definition |
|---|---|
| **Containment** | Limiting the damage from the incident (remote lock, session revocation) |
| **Eradication** | Removing the threat (remote wipe, IMEI blacklisting) |
| **Recovery** | Restoring normal operations (new device, account verification) |
| **Lessons Learned** | Post-incident review to prevent recurrence |

---

## Reporting Requirements

| Scenario | Required Notifications |
|---|---|
| Personal device | None legally required, but inform bank, carrier, and insurance |
| BYOD with work data | Notify employer IT/Security immediately |
| Corporate-owned device | Notify IT Security, manager, and follow organizational IR plan |
| Data breach (personal data of others) | May require regulatory notification (GDPR, CCPA) |
| Healthcare data | HIPAA breach notification may apply |

---

*Last Updated: 2026-06-01*
