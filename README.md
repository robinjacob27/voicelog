# voicelog
Transcriber made for Meeting minutes
VoiceLog — Meeting Transcriber
A zero-backend meeting transcription and summarization tool. Upload any `.aac` (or other audio) recording and get a full transcript + structured meeting summary.
Features
🎙️ Accurate transcription via Groq Whisper (`whisper-large-v3`) — completely free
📋 Structured summaries via Claude (overview, key points, decisions, action items)
🔀 Large file support — auto-splits recordings longer than 1–2 hours into chunks
🔐 Privacy-first — API keys stay in your browser, never hit any server
🚀 Zero backend — pure static HTML, hostable anywhere
Supported Formats
`.aac`, `.mp3`, `.m4a`, `.wav`, `.webm`, `.ogg`, `.flac`
---
Deploy to GitHub Pages
Fork or clone this repo
Go to repo Settings → Pages
Set source to `main` branch, `/ (root)` folder
Save — your site will be live at `https://<username>.github.io/<repo-name>`
---
Usage
Open the site
Click ⚙ API Keys and enter:
Groq API key (from console.groq.com) — free, no credit card needed
Anthropic API key (from console.anthropic.com) — used for Claude summary
Keys are saved in `localStorage` — you only need to enter them once per browser
Drop your `.aac` file, click Transcribe & Summarize
View the Summary tab for structured insights, or Full Transcript for the raw text
---
How Large Files Are Handled
Groq Whisper has a 25MB per-request limit. VoiceLog automatically splits large files into ≤24MB chunks, transcribes each in sequence, and stitches the results together seamlessly.
---
Tech Stack
Layer	Technology	Cost
Transcription	Groq Whisper (`whisper-large-v3`)	Free
Summarization	Anthropic Claude (`claude-sonnet-4`)	Pay-per-use
Hosting	GitHub Pages (static HTML)	Free
Storage	Browser localStorage (keys only)	Free
No Node.js, no build step, no server. Just one HTML file.
---
Getting a Free Groq Key
Go to console.groq.com
Sign up (no credit card required)
Go to API Keys → Create API Key
Copy the key (starts with `gsk_`)
Groq's free tier gives you 7,200 audio minutes per day — more than enough for meeting recordings.
