# Installation Guide

## Requirements

- Windows 10 or Windows 11 (primary supported platform for desktop products)  
- Android 8+ for the debug APKs  
- [LM Studio](https://lmstudio.ai/) with at least one local model loaded for language features on desktop products  
- Network access only as required by optional connectors  

Source builds additionally require Git and Node.js for authorized developers with private repository access.

## Android APKs (debug)

Download from [Releases](https://github.com/The-Warl0ck/candlelight-downloads/releases/tag/android-debug-2026-09-04):

- [Am I Wasted](https://github.com/The-Warl0ck/candlelight-downloads/releases/download/android-debug-2026-09-04/AmIWasted-debug.apk)  
- [DateSense](https://github.com/The-Warl0ck/candlelight-downloads/releases/download/android-debug-2026-09-04/DateSense-debug.apk)  
- [P.E.T.R.](https://github.com/The-Warl0ck/candlelight-downloads/releases/download/android-debug-2026-09-04/PETR-debug.apk)  
- [Math Helper](https://github.com/The-Warl0ck/candlelight-downloads/releases/download/android-debug-2026-09-04/MathHelper-Fluid-debug.apk)  

1. Copy the APK to the phone (USB, Drive, or download in the phone browser).  
2. Open the file. If Android blocks it, allow installs from that source.  
3. If install fails with a signature conflict, uninstall the previous copy of the same app first.  
4. Grant **camera** and **microphone** when Am I Wasted, DateSense, or P.E.T.R. ask.  

These are debug builds. They are not signed Play Store packages.

## Flare Bridge

1. Download the latest Bridge package from [Releases](https://github.com/The-Warl0ck/candlelight-downloads/releases).  
2. Install or extract the portable package according to the release notes.  
3. Start Flare Bridge and confirm the local service is available at `http://127.0.0.1:8766`.  
4. In LM Studio, load a model and leave the default server at `http://127.0.0.1:1234` unless configured otherwise.  

## Forge Nexus

1. Install and start Flare Bridge first. Forge Nexus is designed to use Bridge as its primary backend.  
2. Download Forge Nexus from [Releases](https://github.com/The-Warl0ck/candlelight-downloads/releases) when a package is available.  
3. Launch Forge Nexus and use the primary navigation zones: Hub, Forge, Reality, Ship, and Tools.  
4. Use **Ctrl+K** for quick navigation across features (Teleport).  

## Resonance

1. Running Flare Bridge is recommended for full capability.  
2. Install Resonance from Releases.  
3. Configure the Bridge base URL if the application prompts for it.  

## Source builds (authorized developers)

```text
git clone https://github.com/The-Warl0ck/candlelight-core.git
```

Install dependencies with `npm install` in each product directory. See the private repository README for the full development workflow.

## Troubleshooting

| Symptom | Recommended action |
|---------|-------------------|
| Android blocks the APK | Allow install from that source, or open the file from Files |
| Install blocked (signature) | Uninstall the older build of the same app, then retry |
| Camera never starts | Settings → Apps → the app → Permissions → Camera and Mic |
| Bridge appears offline | Confirm the process is running and port 8766 is free |
| No model responses | Confirm LM Studio is running and a model is loaded |
| Forge cannot reach Bridge | Verify Bridge URL settings and that Bridge started successfully |

For product issues, open a ticket in [candlelight-ai](https://github.com/The-Warl0ck/candlelight-ai).