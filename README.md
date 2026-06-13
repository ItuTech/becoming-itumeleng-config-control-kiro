# Becoming Itumeleng — Kiro Config 💜

This repo contains the full Kiro configuration powering the **Becoming Itumeleng** AI system — custom agents, steering rules, skills, and MCP server setup — managed with [Config Control for Kiro (cckiro)](https://github.com/kirodotdev-labs/config-control-kiro).

These configs are the Kiro side of the full [Becoming Itumeleng](https://github.com/ItuTech/becoming-itumeleng) project, which runs on the Strands Agents SDK and Amazon Bedrock. Same agent, same values, two environments working together.

---

## 🌟 Agents

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

The `steering/` folder contains rules that guide tone, writing style, and content standards across every agent automatically.

| File | Purpose |
|---|---|
| `brand-and-tone.md` | Core identity and voice of the Becoming Itumeleng system — writing rules, platform guidelines, privacy rules, and core philosophy. |

---

## ✨ Skills

Skills are reusable instruction sets that Kiro applies in specific contexts.

| Skill | Purpose |
|---|---|
| `content-creation` | Platform-specific rules for LinkedIn, YouTube, and Medium — hooks, tone, formatting, and what to avoid. |
| `community-building` | Guidance for growing and communicating with The Techie Lounge — events, newsletters, onboarding, and community tone. |

---

## ☁️ MCP Servers

The `settings/mcp.json` file configures Model Context Protocol servers that extend what Kiro agents can do.

| Server | Purpose |
|---|---|
| `aws-docs` | Search and read AWS documentation directly from the agent. |
| `filesystem` | Read files and list directories from allowed local paths. |
| `brave-search` | Web search via Brave (disabled by default — add your API key to enable). |

> **Note:** Replace `YOUR_BRAVE_API_KEY` in `settings/mcp.json` with your actual key if you want to enable web search. The other servers work out of the box with `uvx` installed.

---

## 🛠️ Managing this config with cckiro

The easiest way to explore and edit everything in this repo is [Config Control for Kiro](https://github.com/kirodotdev-labs/config-control-kiro) — a visual UI for agents, MCP servers, steering files, skills, and workspaces.

**Install on macOS (Apple Silicon):**
```bash
curl -L -o cckiro-mac-arm.zip https://github.com/kirodotdev-labs/config-control-kiro/releases/latest/download/cckiro-mac-arm.zip
unzip cckiro-mac-arm.zip
open cckiro.app
```

**Install on macOS (Intel):**
```bash
curl -L -o cckiro-mac-intel.zip https://github.com/kirodotdev-labs/config-control-kiro/releases/latest/download/cckiro-mac-intel.zip
unzip cckiro-mac-intel.zip
open cckiro.app
```

The app opens at `http://127.0.0.1:3030`. Everything stays local — nothing leaves your machine.

> **macOS security note:** If you see a warning on first run, right-click the app → Open → click Open in the dialog. This is macOS blocking unsigned apps, not malware.

---

## 📁 Repo Structure

```
~/.kiro/
├── agents/                        # Custom Kiro agents (JSON)
│   ├── becoming-itumeleng.json    # Lead coordinator
│   ├── brand-guide.json
│   ├── accountability-partner.json
│   ├── consistency-coach.json
│   ├── hype-woman.json
│   └── style-curator.json
├── steering/                      # Always-on instruction files (Markdown)
│   └── brand-and-tone.md
├── skills/                        # Context-specific skill guides
│   ├── content-creation/SKILL.md
│   └── community-building/SKILL.md
└── settings/
    └── mcp.json                   # MCP server configuration
```

---

## 🚀 Getting Started

1. Clone this repo:
```bash
git clone https://github.com/ItuTech/becoming-itumeleng-config-control-kiro.git ~/.kiro-becoming-itumeleng
```

2. Copy the folders you want into your `~/.kiro/` directory:
```bash
cp -r ~/.kiro-becoming-itumeleng/agents ~/.kiro/
cp -r ~/.kiro-becoming-itumeleng/steering ~/.kiro/
cp -r ~/.kiro-becoming-itumeleng/skills ~/.kiro/
cp ~/.kiro-becoming-itumeleng/settings/mcp.json ~/.kiro/settings/mcp.json
```

3. Open Kiro — your agents and skills will be available immediately. The steering file applies automatically to all sessions.

4. Open cckiro to explore and customise everything visually.

---

## 🔗 Related

The full Becoming Itumeleng agent: [ItuTech/becoming-itumeleng](https://github.com/ItuTech/becoming-itumeleng) — runs on the Strands Agents SDK with Amazon Bedrock (Claude Sonnet 4).

---

## 🌍 About

I run a tech community helping people transition from non-technical backgrounds into technology. This system is part of building that journey in public, one consistent day at a time.

> Consistency beats intensity, every time.
