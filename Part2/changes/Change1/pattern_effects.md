# Pattern Effects: CH01

## 1. Domain Entity & Active Record / Data Mapper (TypeORM)
- **Classification**: Extended
- **Participants**: `MiNoteEvent`, `MiNoteEventRsvp`, `MiNote`
- **Source Paths**: `packages/backend/src/models/NoteEvent.ts`, `packages/backend/src/models/NoteEventRsvp.ts`
- **Reason**: Extends Misskey core domain model via 1:1 and 1:N TypeORM entity mappings without disrupting legacy `MiNote` storage.

## 2. Template Method (Endpoint Base)
- **Classification**: Extended
- **Participants**: `Endpoint<typeof meta, Params>`, `rsvp.ts`
- **Source Paths**: `packages/backend/src/server/api/endpoints/notes/events/rsvp.ts`
- **Reason**: Implements Misskey endpoint lifecycle template (metadata declaration, paramDef validation, authentication guard, action execution).

## 3. Observer / Notification Dispatcher
- **Classification**: Extended
- **Participants**: `MiNotification`, `NotificationService`
- **Source Paths**: `packages/backend/src/models/Notification.ts`
- **Reason**: Extends discriminated union notification contract with `eventReminder` payload variant.
