# Video Intel

Tool by **Loren AI**. Paste a TikTok / Instagram Reel / YouTube link → get transcript, summary, CTA, and a one-click prompt for Claude to build a real skill from the video.

Live: https://video-intel.ai-loren.com

## Stack

- Single-file React app (`index.html`) — deployed via GitHub Pages
- Supabase backend (project: Loren Ai, table: `vi_links`)
- Transcription backend: Python FastAPI service (yt-dlp + OpenAI Whisper) — see `michaelmakabi/video-intel-backend` (deploy on Render)
- Until backend is live: "local mode" — UI generates a PowerShell command, you run it on Windows, paste JSON back

## Local development

Just open `index.html` in a browser. Supabase keys are baked in (anon, RLS-restricted to the `vi_links` table).

## Deploy

GitHub Pages serves `index.html` from `main` branch. CNAME points to `video-intel.ai-loren.com`.

Powered by LOREN AI.
