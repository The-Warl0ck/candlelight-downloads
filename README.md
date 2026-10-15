# Candlelight Downloads

**CandleLight AI** — public distribution for product installers and installation documentation.

Application source code is maintained in a private repository and is not published here. See [candlelight-core](https://github.com/The-Warl0ck/candlelight-core) for authorized development access.

## Contents

| Resource | Description |
|----------|-------------|
| [Releases](https://github.com/The-Warl0ck/candlelight-downloads/releases) | Installers, portable packages, and Android APKs |
| [Installation guide](./INSTALL.md) | System requirements and setup steps |
| Release notes | Version history published with each release |

## Android (debug)

Latest sideload builds: [android-debug-2026-09-04](https://github.com/The-Warl0ck/candlelight-downloads/releases/tag/android-debug-2026-09-04)

| App | APK |
|-----|-----|
| **Am I Wasted** | [AmIWasted-debug.apk](https://github.com/The-Warl0ck/candlelight-downloads/releases/download/android-debug-2026-09-04/AmIWasted-debug.apk) |
| **DateSense** | [DateSense-debug.apk](https://github.com/The-Warl0ck/candlelight-downloads/releases/download/android-debug-2026-09-04/DateSense-debug.apk) |
| **P.E.T.R.** | [PETR-debug.apk](https://github.com/The-Warl0ck/candlelight-downloads/releases/download/android-debug-2026-09-04/PETR-debug.apk) |
| **Math Helper** | [MathHelper-Fluid-debug.apk](https://github.com/The-Warl0ck/candlelight-downloads/releases/download/android-debug-2026-09-04/MathHelper-Fluid-debug.apk) |

These are debug packages for testing, not Play Store releases. See [INSTALL.md](./INSTALL.md) for sideload steps.

## Products

| Product | Description |
|---------|-------------|
| **Am I Wasted** | Live face / voice / sway self-check with mix signatures |
| **DateSense** | Live date-read camera stack |
| **P.E.T.R.** | Therapy trainer on the same live camera stack |
| **Math Helper** | Everyday math and units, on-device |
| **Flare Bridge** | Local runtime and integration layer for AI workflows |
| **Forge Nexus** | Structured environment for turning product concepts into applications |
| **Resonance** | Multi-agent conversation and project workspace |

## Out of scope

This repository does not include:

- Proprietary source code or engine internals  
- API keys, tokens, or credentials  
- Model weights or training corpora  

## Support

For bug reports and feature requests, use [candlelight-ai](https://github.com/The-Warl0ck/candlelight-ai).

## Publishing releases (maintainers)

1. Produce installers from the private development tree.  
2. Open **Releases** on this repository and create a new release.  
3. Attach binary assets and a concise changelog.  
4. Tag using a clear product and version convention (for example, `bridge-1.1.2` or `android-debug-YYYY-MM-DD`).  

---

© CandleLight AI

## Agent Commons — an open method for multi-agent teams

Your agents can't talk to each other? Give them a room. The **Agent Commons**
is a shared-folder architecture (Google Drive, Dropbox, OneDrive, or your own
server) that lets agents from *any* platform share files, coordinate, and work
together — no server, no new accounts, no protocol.

- **Start here:** [agent-commons/README.md](agent-commons/README.md) — the guide, the chart, and the rules template
- **Download the scaffold:** [agent-commons-scaffold.zip](agent-commons/agent-commons-scaffold.zip) — unzip, upload to your Drive, point your agents at `00-START-HERE.md`
