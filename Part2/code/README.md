# Evolved Misskey Application Source

- Repository Fork: https://github.com/S-visakh/misskey
- Branch: casestudy-ch01-ch02
- Baseline Commit: 5f501341d49d2bc3fa7e817ce7548a82174326eb
- Implementation Commit: 19c68428ad02cb11b9338fbb38a2098d6c7e2311

## Evolved Production Files in this Folder
- packages/backend/src/models/NoteEvent.ts
- packages/backend/src/models/NoteEventRsvp.ts
- packages/backend/src/models/AudioTranscript.ts
- packages/backend/src/models/Notification.ts
- packages/backend/src/server/api/endpoints/notes/events/rsvp.ts
- packages/backend/src/server/api/endpoints/notes/audio/transcript.ts
- packages/backend/test/note-event.test.ts
- packages/backend/test/note-audio-transcript.test.ts

## CLI Test Execution
node --experimental-strip-types --test packages/backend/test/note-event.test.ts
node --experimental-strip-types --test packages/backend/test/note-audio-transcript.test.ts
