# Install overview (public)

## Requirements (typical)

- Windows 10/11 (primary target today)  
- [LM Studio](https://lmstudio.ai/) with a local model loaded for chat  
- Optional: Git, Node.js if running from source (private repo)  

## Flare Bridge

1. Download the latest Bridge installer from [Releases](https://github.com/The-Warl0ck/candlelight-downloads/releases) (when published).  
2. Run installer / portable package.  
3. Start Bridge → confirm HTTP `http://127.0.0.1:8766` is up.  
4. Load a model in LM Studio (default `http://127.0.0.1:1234`).  

## Forge Nexus

1. Install Bridge first (Forge prefers Bridge as the brain).  
2. Download Forge Nexus from Releases when available.  
3. Start Forge → HUD: Hub / Forge / Reality / Ship / Tools.  
4. **Ctrl+K** Teleport (same idea as Bridge).  

## Resonance

1. Bridge running helps full features.  
2. Install Resonance from Releases.  
3. Connect to Bridge URL if prompted.  

## Source builds

Full source is **private**. Team members with access:

```text
git clone https://github.com/The-Warl0ck/candlelight-core.git
```

Then `npm install` per product folder (see private README).
