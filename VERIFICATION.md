# What has and has not been verified

Snapshot: 1 October 2026. This is a public summary of project evidence, not a certification or a live service-level claim.

| Area | Evidence available | Boundary |
|---|---|---|
| Backend and persistence | Local API/database tests, authorization and retry/conflict scenarios | No public hosted-environment acceptance |
| Browser | Local journeys and responsive/layout checks | Not a complete accessibility audit |
| Android | Builds, JVM/lint checks and selected Pixel 10 emulator/S24 journeys | Remaining physical gestures, accessibility and power-saving cases |
| Reminders | Development FCM receipt and user-confirmed email/device delivery | Not a production delivery guarantee |
| Recovery | Local backup/restore and deletion-receipt rehearsal | Must be repeated for the actual hosting/storage setup |
| Portfolio screenshots | Actual web build with fictional read-only API fixtures | Visual demonstration only; not end-to-end backend execution |
| Public code sample | Independently runnable calendar-boundary and invariant tests | Date-only sample, not the full reminder engine |

Production hosting, commercial billing, real partner bookings and iOS delivery remain outside the demonstrated scope. This repository intentionally avoids publishing private test logs, account data, credentials and operational configuration.
