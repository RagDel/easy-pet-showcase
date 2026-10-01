# Verification and evidence

**Evidence snapshot: 1 October 2026.** This page summarizes recorded application checks. The portfolio refresh did not rerun the full private application suite, and the counts below are separate checkpoints rather than one combined release result.

## Recorded checkpoints

| Area | Evidence recorded | What it establishes |
|---|---|---|
| Backend and persistence | 233 PostgreSQL-backed application tests passed in the latest recorded backend checkpoint | Tested application behavior, including permissions, records, account controls and existing concurrency regressions |
| Native Android | 89 JVM tests passed; build and lint completed with zero errors and 28 existing warnings | Tested Kotlin behavior and a buildable app; selected emulator and physical-device journeys provide separate runtime evidence |
| Web application | TypeScript/Vite builds and focused browser interaction suites passed | Tested browser behavior and responsive Greek/English layouts, including 320, 390 and 1,360 px viewports for the shared timeline |
| Cross-client journeys | Synthetic-record browser/API and Android checks covered selected shared-care, account and timeline flows | Evidence for the particular journeys exercised, with broader acceptance still to complete |
| Reminder interactions | Scheduling tests and selected device receipt, tap, snooze and dismissal checks were recorded | Evidence for tested integration paths and interactions; no hosted availability or universal delivery claim |
| Portfolio previews | Current web-interface captures use fictional demonstration records | A visual walkthrough of the interface, separate from end-to-end application acceptance |

These checks are complementary. A layout fixture can reveal clipped controls but cannot establish database persistence; a unit test cannot establish how a physical gesture feels.

For this portfolio refresh, six current web captures were visually reviewed across desktop English and phone-width Greek layouts. Capture checks recorded no page errors, unexpected requests, data writes or horizontal page overflow. All demonstration accounts, pets, events and attachments are fictional; the illustrated pet avatars are part of that dataset.

## Behaviors exercised

### Timeline and client parity

Shared-axis checks cover isolated events, two-event overlaps, groups of three or more, mixed pets and dates, long collision chains, birthdays and filtered selections. Browser and Kotlin checks exercise grouping, access changes and reachable group counts while panning.

Recorded browser/API journeys include saved custom gradients and cropped photos, completion persistence, inline group expansion and returning to the saved event. Android checks include shared-palette compatibility and selected native timeline interactions. The Today shortcut was checked after repeated panning while preserving scale and pet filters.

### Shared care and consistency

Recorded journeys cover viewer/editor differences, profile and event changes, leaving a shared pet and preserving the owner's records. Backend checks cover version conflicts, repeated submissions, concurrent operations and migration compatibility. Document checks include uploads, downloads, failed-upload retries and shared storage accounting.

Account journeys include export, session controls, the pending-deletion experience and cancellation. These are functional checks of the user controls; they do not represent a compliance assessment.

### Calendars and reminders

Tests exercise completion-based recurrence, month ends, daylight-saving transitions, preserved existing rules and adjustable calendar clocks. Reminder interaction checks include repeated or reordered actions and cancellation after completion or changed eligibility.

Selected scheduled email and Android notification receipt was confirmed during development. Native checks also exercised notification opening and a short snooze returning as a fresh alert. Longer dismissal intervals were checked through saved scheduling state and controlled time advancement, rather than waiting through every full interval. These results do not imply an active hosted notification service or punctual delivery in every device state.

### Provider discovery

Recorded checks cover distance ordering, pagination, Greek/Latin place lookup, category-specific searches and map-result refresh. Selected Android checks observed changed results after choosing a place, page navigation and grouped pins. Some browser map checks substitute external responses, so those passes establish interface behavior rather than external map-service availability.

The dataset count describes source records, not independently verified businesses or complete geographic coverage.

## Upcoming acceptance

Managed cloud deployment and acceptance in the selected hosting environment are upcoming. Further work includes broader accessibility and native large-text coverage, physical multitouch, interrupted forms, returning sign-in journeys, release installation/update checks and notification behavior under restrictive device power settings.

Professional external messaging, partner booking, commercial billing and iOS are outside the demonstrated delivery scope. No production service-level or comprehensive security claim is made by the test counts.

For a runnable public example, the [completion-recurrence repository](https://github.com/RagDel/completion-recurrence) provides a focused date-only implementation and tests. Its results apply to that sample; the private application's broader behavior is summarized here.

[Product walkthrough](WALKTHROUGH.md) · [Architecture and decisions](ARCHITECTURE.md) · [Agent-assisted development](AGENT_WORKFLOW.md)
