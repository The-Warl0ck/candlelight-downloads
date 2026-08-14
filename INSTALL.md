# Installation Guide

## Requirements

- Windows 10 or Windows 11 (primary supported platform)  
- [LM Studio](https://lmstudio.ai/) with at least one local model loaded for language features  
- Network access only as required by optional connectors  

Source builds additionally require Git and Node.js for authorized developers with private repository access.

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
| Bridge appears offline | Confirm the process is running and port 8766 is free |
| No model responses | Confirm LM Studio is running and a model is loaded |
| Forge cannot reach Bridge | Verify Bridge URL settings and that Bridge started successfully |

For product issues, open a ticket in [candlelight-ai](https://github.com/The-Warl0ck/candlelight-ai).
