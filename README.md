# antidoomscroll-dist

Public update channel of **Anti-DoomScroll** (a personal Android app). The source code is private;
this repository only carries what the installed app downloads:

| Path | What |
|---|---|
| [Releases](../../releases) | One signed APK per version (`antidoomscroll-<versionCode>.apk`). |
| `manifest.json` | Latest version: `{versionCode, versionName, apkUrl, sha256, changelog}`. The app installs an update only if the APK's SHA-256 matches. |
| `selectors.json` | Instagram screen selectors; the app applies them only when they validate. |
| `decks/index.json` | List of quiz deck files in `decks/` (format: deck v3 with short cards). |
| `decks/*.json` | Quiz decks. |

Served by Vercel from `main` (auto-deploy on push): `https://antidoomscroll-dist.vercel.app/`.
`vercel.json` sends `Cache-Control: no-cache` for the JSON files, so a push is visible within
seconds of the deploy. Everything here is published with `tools/publish.ps1` from the private
source repo.

Nothing secret belongs here: no keystores, passwords, configs or personal data.
