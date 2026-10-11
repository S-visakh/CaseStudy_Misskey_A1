# Requirement: CH01 — Native Events with RSVP and Reminder Notifications

## Requirement & Problem in Baseline
In the baseline Misskey codebase (commit 5f501341d4), notes support ephemeral polls and generic scheduling, but lack structured event semantics (start/end dates, location/meeting URL, attendee tracking, and proactive event reminders). Users cannot state or query attendance without informal replies or ad-hoc polls.

## Intended Behavior
1. Enable notes to attach structured event entities with start time, optional end time, title, and location.
2. Allow authenticated users to record and modify attendance (RSVP) with states: 'going', 'interested', 'notGoing'.
3. Integrate an 'eventReminder' notification payload to proactively notify users prior to event start.

## Acceptance Criteria
- AC1: Event end date must be strictly after start date if present.
- AC2: Authenticated RSVP endpoint validates and updates state transitions across 'going', 'interested', and 'notGoing'.
- AC3: Notification schema includes strongly-typed 'eventReminder' variant with noteId and recipient mapping.

## Verification
Verified via node:test runner executing unit assertions against date logic, RSVP transition state machine, and notification payload structure.
