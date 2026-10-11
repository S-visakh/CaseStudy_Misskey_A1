# Pattern Effects: CH02

## 1. Extension Object / Data Mapper (TypeORM)
- **Classification**: Extended
- **Participants**: `MiAudioTranscript`, `MiDriveFile`
- **Source Paths**: `packages/backend/src/models/AudioTranscript.ts`
- **Reason**: Introduces an extension entity attached to `MiDriveFile` to decouple transcription metadata from binary storage schemas.

## 2. Template Method (Endpoint Base)
- **Classification**: Extended
- **Participants**: `Endpoint<typeof meta, Params>`, `transcript.ts`
- **Source Paths**: `packages/backend/src/server/api/endpoints/notes/audio/transcript.ts`
- **Reason**: Adheres to Misskey standard endpoint execution pipeline for validation and authorization.
