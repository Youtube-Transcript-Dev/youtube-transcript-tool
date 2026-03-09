# YouTube Transcript Tool

Cursor plugin for extracting and working with YouTube video transcripts. Integrates with YouTubeTranscript.dev to fetch captions, AI transcription, and translations in 100+ languages.

## Installation

```bash
/add-plugin youtube-transcript-tool
```

## Target Users

- Developers building transcript-powered features
- Content creators summarizing or repurposing videos
- Researchers extracting text from educational content

## Setup

1. Get an API key at [youtubetranscript.dev/dashboard](https://www.youtubetranscript.dev/dashboard)
2. Add to your environment: `YOUTUBE_TRANSCRIPT_API_KEY=yt_sk_live_...`

## Components

### Skills

| Skill | Description |
|:------|:------------|
| `fetch-transcript` | Fetch transcript for a YouTube URL (captions or AI transcription) |

### Rules

| Rule | Description |
|:-----|:------------|
| `transcript-conventions` | Conventions for handling transcripts in the project |
| `api-key-setup` | API key configuration for YouTubeTranscript.dev |

### Agents

| Agent | Description |
|:------|:------------|
| `transcript-specialist` | Expert for extracting and working with YouTube transcripts |

### Commands

| Command | Description |
|:--------|:------------|
| `fetch-transcript` | Extract transcript from a YouTube video URL |

## Usage

1. Use `/fetch-transcript` or `/transcript-specialist` with a YouTube URL.
2. Specify format (txt, srt, vtt, json) and language if needed.
3. Rules apply automatically when working with transcript files.

## Links

- [YouTubeTranscript.dev](https://www.youtubetranscript.dev)
- [API docs](https://www.youtubetranscript.dev/api-docs)

## License

MIT
