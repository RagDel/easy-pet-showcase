# Pet-Easy

**One timeline. Every pet. Shared care that stays in sync.**

Pet-Easy brings pet profiles, care events, reminders and caregiver collaboration into a connected web and native Android experience. Greek by default, with an English switch.

A product and engineering case study by **Tilemachos Tragakis**, developed with Codex and scoped AI-agent workflows.

**React · TypeScript · Django REST Framework · PostgreSQL · Kotlin · Jetpack Compose · Docker**

![Pet-Easy shared timeline with fictional pets and care events](assets/timeline.jpg)

[Visual walkthrough](WALKTHROUGH.md) · [Architecture](ARCHITECTURE.md) · [Agents and skills](AGENT_WORKFLOW.md) · [Verification](VERIFICATION.md) · [Runnable Python sample](https://github.com/RagDel/completion-recurrence)

**October 2026:** web and Android features are implemented and undergoing iterative verification. Managed cloud deployment and public release are upcoming milestones. This public repository presents the product and engineering; application source remains private.

## The product

Sharing pet care means coordinating more than dates. An owner needs to know what happened, what comes next, who changed a record and what each caregiver can do. Pet-Easy connects these decisions in one place, while remaining useful for someone caring for a pet alone.

| Capability | What the experience offers |
|---|---|
| **A shared timeline** | One horizontal date axis for every selected pet, circular photo/category markers, pan and zoom, a Today shortcut, and pet/type filters. Crowded events group by overlap and expand in place. |
| **Profiles with personality** | Cropped photos, optional birthdays, age and kg/lb weight, plus 24 actual gradient presets and custom colors shared across clients. |
| **Flexible care records** | Vaccines, antiparasitic care, treatment, grooming, food and species-aware supplies. Optional product details, reusable choices, documents and provider contacts stay with the event. |
| **Caregiver collaboration** | Owner-managed invitations, View only or View & edit access, attributed changes and the ability to leave a shared pet. |
| **Completion-based planning** | Repeat intervals count from actual completion. Reminder preferences, adjustable times and native Android snooze/dismissal behavior support follow-up. |
| **Nearby services** | Nearest-first provider results, grouped map pins, city/area search, relevant business categories and external Google Maps links. Initial coverage uses source-attributed open data for Greece. |
| **Control over records** | Private attachments, data export, session management and distinct pet-profile/account deletion flows with recovery or cancellation periods. |

A separate **professional workspace is in development**, covering clients and pets, practice details and reminder planning. Partner bookings, payments and external professional messaging remain future work.

## Engineering behind the interface

| Challenge | Implemented approach |
|---|---|
| Many pets and overlapping dates on one screen | Zoom-aware collision groups preserve full event counts and open a bounded detail grid. |
| The same data on web and Android | A shared API and behavior contracts, with native interfaces and shared visual presets. |
| Two caregivers change one event | Version-aware updates expose conflicts instead of silently overwriting changes. |
| A completion request is retried | Retry-safe completion avoids generating duplicate successor events. |
| A task is completed late | Calendar recurrence starts from completion, with explicit month-end and leap-year behavior. |
| Access changes while details are open | Clients clear stale views and actions as access changes. |
| A familiar visual feature evolves | Existing solid pet colors remain valid alongside the new two-stop gradients. |

The [architecture case study](ARCHITECTURE.md) explains these decisions. The [standalone recurrence sample](https://github.com/RagDel/completion-recurrence) provides inspectable Python code, a CLI and tests for one scheduling problem from the project.

## How I build with agents

I own product direction, choose the stack and user-facing behavior, and review the experience. I use Codex agents for focused research, implementation, debugging, verification and documentation, with explicit scope and acceptance criteria.

Ten project-specific skills separate product, UX, UI, architecture, backend, browser, Android, database, containers and integration verification. Shared contracts and recorded decisions connect their work; independent reviews check results before integration. [See the workflow and a concrete feature example.](AGENT_WORKFLOW.md)

## Evidence and next steps

Recorded checks include PostgreSQL integration tests, responsive Greek/English browser journeys, Android JVM tests and lint, and selected browser-to-Android persistence checks. The visual walkthrough uses the current web interface and fictional demonstration data. Narrow-screen web captures are labelled as web, and are separate from native Android evidence.

Next milestones are **managed cloud deployment**, release distribution, monitoring, broader physical-device and accessibility testing, and expanded professional workflows. Notification integration and development delivery checks do not establish production delivery reliability. [Verification scope and remaining work](VERIFICATION.md).

Published for portfolio review. No open-source reuse license has been selected for the case-study materials, branding or private application.
