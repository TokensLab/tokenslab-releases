<p align="center">
  <img src="https://tokenslab.tech/assets/images/logo-hex.png" width="72" height="72" alt="TokensLab">
</p>

<h1 align="center">TokensLab</h1>

<p align="center">
  The cost lab for your AI coding sessions.<br>
  Offline. Private. Free to download.
</p>

<p align="center">
  <a href="https://tokenslab.tech/download"><img src="https://img.shields.io/badge/download-beta-6C2BD9?style=for-the-badge" alt="Download beta"></a>
  <a href="https://github.com/lucasbarroos/tokenslab-releases/releases/latest"><img src="https://img.shields.io/github/v/release/lucasbarroos/tokenslab-releases?style=for-the-badge&color=6C2BD9&label=latest" alt="Latest release"></a>
  <a href="https://tokenslab.tech"><img src="https://img.shields.io/badge/site-tokenslab.tech-111827?style=for-the-badge" alt="tokenslab.tech"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Windows-x64-0078D6?logo=windows&logoColor=white" alt="Windows">
  <img src="https://img.shields.io/badge/Linux-AppImage-FCC624?logo=linux&logoColor=black" alt="Linux">
  <img src="https://img.shields.io/badge/macOS-this_weekend-lightgrey?logo=apple&logoColor=white" alt="macOS soon">
</p>

Same Claude Code logs. Two invoices.

| Naive arithmetic | Cache-aware (TokensLab) |
| ---------------- | ----------------------- |
| **$15,680.35**   | **$3,123.97**           |

Cache-read tokens dominate real sessions and bill at 0.1× the input rate. TokensLab prices every token class separately so the dashboard matches the bill, not a 5× overestimate.

## Download

This repository is the public face of TokensLab on GitHub: installers only. The desktop app source stays private.

| Platform | File | Status |
| -------- | ---- | ------ |
| **Windows** 10 / 11 | [TokensLab-windows.exe](https://github.com/lucasbarroos/tokenslab-releases/releases/latest/download/TokensLab-windows.exe) | Public beta |
| **Linux** x64 | [TokensLab-linux.AppImage](https://github.com/lucasbarroos/tokenslab-releases/releases/latest/download/TokensLab-linux.AppImage) | Public beta |
| **macOS** Apple Silicon | `.dmg` | This weekend (code signing) |

Prefer the site: **[tokenslab.tech/download](https://tokenslab.tech/download)**

### After you download

- **Windows** — if SmartScreen appears, choose **More info → Run anyway**. The beta is unsigned.
- **Linux** — `chmod +x TokensLab-linux.AppImage && ./TokensLab-linux.AppImage`
- Point the app at `~/.claude/projects` (or your Cursor / Codex folders). Nothing is uploaded.

## What it does

TokensLab reads session logs already on disk from Claude Code, Cursor, and Codex, then prices every turn against published rate cards.

- Spend, burn rate, and cost by model and project
- Live vs idle sessions — quiet sessions still cost money
- Skills Explorer and Graph Explorer for what the model actually touched
- No account, no telemetry, no network call from the app

## Contributors

The people behind TokensLab. This list is the one users and developers will see here.

<table>
  <tr>
    <td align="center" width="140">
      <a href="https://github.com/lucasbarroos">
        <img src="https://avatars.githubusercontent.com/u/19896970?v=4" width="88" height="88" alt="Lucas Barros"><br>
        <sub><b>Lucas Barros</b></sub>
      </a><br>
      <sub>Founder</sub>
    </td>
  </tr>
</table>

<p align="center">
  <a href="https://github.com/lucasbarroos/tokenslab-releases/graphs/contributors">
    <img src="https://contrib.rocks/image?repo=lucasbarroos/tokenslab-releases" alt="Contributors">
  </a>
</p>

Installer bugs and beta reports: open an [issue](https://github.com/lucasbarroos/tokenslab-releases/issues) or write to [hello@tokenslab.tech](mailto:hello@tokenslab.tech).

## License

Installers are provided as-is for the public beta. Source is not published at launch.
