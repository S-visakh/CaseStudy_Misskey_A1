# Requirement: CH02 — First-Class Audio Posts with Transcription

## Requirement & Problem in Baseline
In the baseline Misskey codebase, audio files uploaded to Drive are treated as generic binary media attachments. There is no dedicated metadata model to store accessible text transcripts, spoken language annotations, or review mechanisms before publishing.

## Intended Behavior
1. Attach structured transcription metadata to Drive files without modifying the legacy binary storage pipeline.
2. Validate audio MIME types to restrict transcription attachments to audio streams.
3. Provide an authorized endpoint allowing users to upload or update verified transcripts.

## Acceptance Criteria
- AC1: Whitelist audio MIME types (audio/*, application/ogg).
- AC2: API endpoint rejects whitespace-only transcripts with EMPTY_TRANSCRIPT error code.
- AC3: Persist transcript records linked 1:1 to drive files with language and generation metadata.

## Verification
Verified via node:test runner validating audio MIME detection, transcript trimming/sanitization, and record structuring.
