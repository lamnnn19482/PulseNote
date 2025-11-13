# PulseNote ✦ AI Summary

PulseNote ✦ AI Summary is a Chrome extension that captures YouTube transcripts and distills the most useful ~80 % of any video into an actionable recap. The UI mirrors a polished macOS widget: click the toolbar icon, hit **Start Summary**, and PulseNote delivers clean text plus an AI-written digest you can copy anywhere.

> **Need the extension package?** Download the latest release zip from this repository or load the `YouTubeSubtitleExtension` source folder directly via Developer Mode.

## Features

- **Instant transcripts** – Fetches official YouTube captions in multiple languages and lets you download them as `.txt`.
- **AI summary** – PulseNote’s backend condenses the video into a crisp recap, typically covering ~80 % of the important ideas.
- **License-aware limits** – 15 free summaries every 15 days; enter a Gumroad license to unlock unlimited requests.
- **Custom preferences** – Choose transcript language, output language, and optional advanced prompt tuning on the server.
- **Error transparency** – Clear messaging when captions are missing, throttled, or blocked by the video owner.

## Install (Developer Mode)

1. Clone or download the repository that contains `manifest.json`.
2. Open Chrome → `chrome://extensions`.
3. Toggle **Developer mode**.
4. Click **Load unpacked** and select the extension folder.
5. Pin the PulseNote icon and try it on any caption-enabled YouTube video.

## How It Works

1. PulseNote asks YouTube’s caption endpoints for the selected language track.
2. The popup displays and lets you copy or download the transcript.
3. When you click **Start Summary**, the transcript plus your preferences are sent to the PulseNote summary API (`/api/summarize`).
4. The backend uses the `SUMMARY_PROMPT_HINT` template, returns a recap, and decrements the free-credit counter unless a Gumroad license token is active.
5. Responses are cached on the client so you can reopen the popup without re-running the summary.

## Backend Requirements

- HTTPS endpoint exposing `POST /api/summarize` and `POST /api/activate`.
- Handles payload fields: `transcript_language`, `language` (desired output), `preference_signature`, `gumroad_license`.
- Adds CORS headers (`Access-Control-Allow-Origin: *` for testing or your production domain).
- Provides clear error codes so the popup can display retry tips.

## Chrome Web Store Assets

| Asset                   | Path / Naming idea                                | Notes |
| ----------------------- | ------------------------------------------------- | ----- |
| Extension icons         | `icons/icon16.png`, `icon32.png`, `icon48.png`, `icon128.png` | Derived from the orange flower artwork (`Thiết kế ...-21.png`). |
| Small promo tile 440×280| `assets/promo-tile.png` *(create/export via design file)* | Suggested copy: “PulseNote’s AI condenses the most useful 80 % of every video into a crisp summary.” |

Save promo graphics as 24-bit PNG/JPEG (no alpha) before uploading to the Chrome Web Store.

## Development Scripts

```bash
# Resize icons (macOS)
/usr/bin/sips -z 128 128 icons/source.png --out icons/icon128.png
```

See `scripts/generate_icons.py` inside the extension project if you prefer Python automation.

## Support

For bug reports, feature requests, or billing questions please read [`SUPPORT.md`](SUPPORT.md).

## License

TBD – update this section once you decide between MIT, Apache-2.0, or a proprietary license.
