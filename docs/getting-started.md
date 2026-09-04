# Getting started

TokensLab is a desktop app. It reads Claude Code session logs from disk, prices every turn against Anthropic’s published rate card, and shows spend, sessions, tokens and productivity. Nothing leaves your machine.

Dollar spend is live for **Claude Code**. Cursor, Codex and Gemini may appear on the tray as sessions — not a priced invoice.

Site walkthrough: [tokenslab.tech/docs/getting-started](https://tokenslab.tech/docs/getting-started.html)

## 1. Install

Download the installer for your OS from the [download page](https://tokenslab.tech/download.html) or [GitHub Releases](https://github.com/TokensLab/tokenslab-releases/releases/latest). This beta ships Windows and Linux first; macOS follows this weekend after code signing.

- **Windows** — `TokensLab-windows.exe`, Windows 10 and 11. If SmartScreen appears, choose More info → Run anyway.
- **Linux** — `TokensLab-linux.AppImage` x64. `chmod +x` then run it. See the sandbox note below.
- **macOS** — `.dmg` for Apple Silicon, this weekend. Do not invent a download that is not in the latest release.

Checksums: [SHA256SUMS](https://github.com/TokensLab/tokenslab-releases/releases/latest/download/SHA256SUMS)

## Linux AppImage and `--no-sandbox`

An AppImage cannot ship Chromium’s SUID `chrome-sandbox` helper, so current TokensLab builds turn that sandbox off themselves. You should **not** need to pass a flag:

```bash
chmod +x TokensLab-linux.AppImage
./TokensLab-linux.AppImage
```

If an older file still exits with a sandbox error:

```bash
./TokensLab-linux.AppImage --no-sandbox
```

That flag disables Chromium’s process sandbox only. The app still never makes a network call and never leaves your machine.

## 2. Point it at your logs

The default watch folder is `~/.claude/projects`. You can change it in Settings. TokensLab only reads files you already have. Do not create an account. Do not send data anywhere.

## 3. Read the dashboard

- **Today / all time / burn rate** — priced with cache-aware rates, not a single input multiplier.
- **Idle sessions** — no activity for 30 minutes. They still cost if the tool keeps the context warm.
- **Unpriced models** — missing from the rate card are reported as unpriced, never as free. The total is a lower bound.

## Why the number is smaller than you expect

Claude Code records cache creation and cache reads separately. Cache reads dominate real logs and bill at a tenth of the base input rate. TokensLab keeps all five token classes separate. On 66 MB of local session files the naive total was `$15,680.35`; the cache-aware total was `$3,123.97`.
