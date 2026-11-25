# Publishing checklist

The profile README, the portfolio and every landing page link to the addresses below.
**Use these exact repository names and installer file names**, or the download buttons will 404.

## 1. This profile

Create a public repo named **`qub-official`** (same as the username) and push this folder.
GitHub shows its `README.md` on https://github.com/qub-official.

## 2. Apps

| App | Local folder | Repo name | Pages source | Release asset (exact name) |
|---|---|---|---|---|
| Loom | `loom` | `loom` | `main` /docs | any (built by `.github/workflows/release.yml`) |
| Moa | `mediadown` | `moa` | `main` /docs | `Moa-Setup.exe` |
| YouTown Player | `youtown/github-upload` | `youtown` | `main` /docs | `YouTown-Player-Setup.exe` |
| Jamgeum | `passmanage/github-upload` | `jamgeum` | `main` /docs | `Jamgeum-Setup.exe` |
| Haneul Bible | `mybible` | `haneul-bible` | `main` /docs | `HaneulBible-Setup.exe` |
| MyRecord | `myrecord` | `myrecord` | `main` /docs | `MyRecord-Setup.exe` |
| MyProperties | `myproperties` | `myproperties` | GitHub Actions (`pages.yml`) | any `*Setup*.exe` |
| myTraffic | `myTraffic` | `myTraffic` | `main` / (root) | any (page links to the releases list) |
| Coredit | `coredit/github-upload` | `coredit` | later: still in development | `Coredit-Setup-x64.exe` |
| CopyCut Studio | `copycut` | `copycut` | later: still in development | |

For each app:

1. Create the repo at https://github.com/new as **Public**, with no README, license or .gitignore (they're already in the folder).
2. Push the folder. `brag-output/` is already in each `.gitignore`. Also check that `node_modules/`, `dist/`, `build/` outputs and `vendor/` binaries are not included.
3. **Releases → Draft a new release**, tag `v1.0.0`, attach the installer from the folder's `dist\` with the exact name above, then publish.
4. **Settings → Pages**: set the source from the table. The site appears at `https://qub-official.github.io/<repo>/`.

## 3. Later: Coredit and CopyCut

Both are still being improved. The profile and portfolio show them as "coming soon". Coredit's landing page and links are already set up for `qub-official/coredit`.

CopyCut still needs, before publishing:

- No `LICENSE` file yet (all the other apps use MIT).
- No `.gitignore`. It needs to exclude `node_modules/`, `dist/`, `vendor/` (301 MB of FFmpeg, Whisper and yt-dlp binaries) and `brag-output/`.
- The folder contains YouTube tutorial transcripts (`*.txt`). Those are other people's content; keep them out of the repo.
- No landing page in `docs/` yet. The profile shows it as "coming soon" until then.

## Not listed on the profile

- `youtube2transcription`: a script, not an app. It ships Tor binaries and scraped transcripts.
- `animatedWallpaper`: empty folder.
- `branding`: notes only.
