---
name: fetch-transcript
description: Fetch transcript for a YouTube video URL. Use captions when available, AI transcription otherwise. Supports formats txt, srt, vtt, json and 100+ languages.
---

# Fetch transcript

## Trigger

User needs the transcript of a YouTube video (by URL or video ID).

## Required Inputs

- YouTube URL or video ID
- Optional: format (txt, srt, vtt, json), language code

## Workflow

1. Extract video ID from URL (e.g. `youtube.com/watch?v=VIDEO_ID` or `youtu.be/VIDEO_ID`).
2. Use YouTubeTranscript.dev API:
   - `POST https://youtubetranscript.dev/api/v2/transcribe`
   - Body: `{ "video": "VIDEO_ID", "language": "en", "source": "auto", "format": { "timestamp": true } }`
   - Headers: `Authorization: Bearer <API_KEY>`, `Content-Type: application/json`
   - API key: user config or `YOUTUBE_TRANSCRIPT_API_KEY` env
3. Return transcript in requested format. Default to plain text if unspecified.
4. If captions unavailable, note that AI transcription may be used (source: `asr`).

## Output

- Transcript text or structured data
- Format and language used
- Any errors (private video, no captions, etc.)
