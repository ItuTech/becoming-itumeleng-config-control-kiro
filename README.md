# Becoming Itumeleng — Kiro Config 💜

This repo contains the Kiro configuration powering the **Becoming Itumeleng** AI system — custom agents, steering rules, and tone guidelines that show up across every interaction.

These configs are the Kiro side of the full [Becoming Itumeleng](https://github.com/ItuTech/becoming-itumeleng) project, which runs on the Strands Agents SDK and Amazon Bedrock. Same agent, same values, two environments working together.

---

## 🌟 The AI Team

| Agent | Role |
|---|---|
| **Becoming Itumeleng** | Lead coordinator. Knows the full system and routes to the right agent based on what's needed in the moment. |
| **Brand Guide** | Keeps voice and messaging consistent across YouTube, LinkedIn, and Medium. Tone, hooks, visual identity — she knows the playbook. |
| **Accountability Partner** | Tracks goals and checks in on progress. Kind but honest. Won't let me slide. |
| **Consistency Coach** | Builds daily habits and tracks streaks. Because consistency beats intensity, every time. |
| **Hype Woman** | Celebrates wins (big and small), boosts confidence before events or recordings, and reminds me how far I've come. |
| **Style Curator** | Suggests outfits based on occasion, weather, mood, and what's actually in the wardrobe. No more 20 minutes in front of the closet. |

---

## 🧠 Steering

The `steering/` folder contains rules that guide tone, writing style, and content standards across every agent.

`brand-and-tone.md` — the core identity and voice of the Becoming Itumeleng system. Covers writing rules, platform guidelines, privacy rules, and the core philosophy behind everything.

Steering files apply automatically to all Kiro interactions — no manual loading needed.

---

## ☁️ How to use this config

These files work with [Kiro](https://kiro.dev). To use them:

1. Clone this repo into your `~/.kiro/` directory, or copy the `agents/` and `steering/` folders there.
2. Open Kiro — your agents will appear in the agent panel automatically.
3. The steering file applies globally to all sessions.

### Managing this config visually

The easiest way to explore and edit this config is with [Config Control for Kiro](https://github.com/kirodotdev-labs/config-control-kiro) (cckiro) — a desktop app that gives you a visual UI for agents, MCP servers, steering files, and skills.

**macOS (Apple Silicon):**
```bash
curl -L -o cckiro-mac-arm.zip https://github.com/kirodotdev-labs/config-control-kiro/releases/latest/download/cckiro-mac-arm.zip
unzip cckiro-mac-arm.zip
open cckiro.app
```

**macOS (Intel):**
```bash
curl -L -o cckiro-mac-intel.zip https://github.com/kirodotdev-labs/config-control-kiro/releases/latest/download/cckiro-mac-intel.zip
unzip cckiro-mac-intel.zip
open cckiro.app
```

The app opens in your browser at `http://127.0.0.1:3030`. Everything stays local — nothing leaves your machine.

> **Note for macOS users:** If you see a security warning on first run, right-click the app → Open → click Open in the dialog. This is macOS blocking unsigned apps, not a sign of malware.

---

## 🔗 Related

The full Becoming Itumeleng agent lives here: [ItuTech/becoming-itumeleng](https://github.com/ItuTech/becoming-itumeleng)

That project runs the same agent system on the Strands Agents SDK with Amazon Bedrock (Claude Sonnet 4). This repo is the Kiro-native version of the same system — same agents, same values, optimised for the Kiro IDE experience.

---

## 🌍 About

I run a tech community helping people transition from non-technical backgrounds into technology. This system is part of building that journey in public, one consistent day at a time.

> Consistency beats intensity, every time.
