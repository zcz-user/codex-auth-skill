---
name: codex-auth
description: 🧩 Codex Skill — Refresh Codex CLI auth.json from ChatGPT. Skipphone verification, no overseas number needed. For users behind firewalls, in WSL, or remote desktop.
tags:
  - codex
  - codex-cli
  - auth
  - chatgpt
  - token
  - windows
  - playwright
  - phone-verification
---

# 🧩 Codex Skill: Codex Auth Session Refresh

> **This is an [OpenClaw skill](https://clawhub.com/skill/codex-auth-session) for [Codex CLI](https://github.com/openai/codex).**
> It provides Windows tooling to refresh Codex's `auth.json` with a fresh ChatGPT session token.

📱 **跳过手机验证码 · 不需要外区手机号 · 適用於 Codex**

---

## 🎯 Who Is This For?

**Codex CLI users** stuck with these pain points:

| 😤 Pain | 💥 Why it sucks |
|---------|----------------|
| Codex OAuth won't complete | Proxies, WSL, containers — browser never opens |
| 📱 OpenAI phone verification | SMS code required, no overseas phone number = can't login |
| Re-auth every few hours | Keep entering SMS codes, drives you crazy |
| Forced to use API proxies | Can't get official auth working, settle for third-party |
| Token dies mid-session | Lose context, workflow destroyed |

## What This Does

Extracts a fresh `access_token` from your existing ChatGPT browser session and writes it directly to Codex's `~/.codex/auth.json`.

**核心价值：** 只要你的 ChatGPT 浏览器还在登录状态，就不需要再收验证码。一次登录，Codex 永久续命。

## Installation via ClawHub

```bash
clawhub install codex-auth-session
```

## Quick Install (Windows)

```powershell
git clone https://github.com/zcz-user/codex-auth-session-refresh.git
cd codex-auth-session-refresh
npm install
.\login-profile.ps1        # Login ChatGPT → press Enter
.\status.ps1               # Check Codex auth state
.\install-scheduled-task.ps1  # Auto-refresh, never re-auth again
```

## Commands

| Command | What it does |
|---------|-------------|
| `login-profile.ps1` | First login / re-login into ChatGPT |
| `run-refresh.ps1` | Refresh Codex's access token now |
| `status.ps1` | Check Codex auth.json status |
| `install-scheduled-task.ps1` | Auto-refresh every N hours |
| `create-desktop-toolbox.ps1` | Desktop shortcuts |

## Environment Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `CODEX_AUTH_PATH` | `~/.codex/auth.json` | Codex auth file target |
| `CODEX_AUTH_REFRESH_BROWSER` | auto-detect | Chrome/Edge path override |
| `CODEX_AUTH_REFRESH_PROFILE` | `./browser-profile` | Browser profile storage |
| `CODEX_AUTH_REFRESH_BACKUP` | `./backups` | Auth file backup dir |
| `CODEX_AUTH_REFRESH_LOG` | `./logs` | Operation log dir |

## Security

- Token values are **never** written to logs (`delete safe.token` before write)
- `auth.json` backed up with timestamp before every update
- `browser-profile/`, `logs/`, `backups/`, `auth.json` all excluded via `.gitignore`

## Requirements

- **OS:** Windows 10/11
- **Runtime:** Node.js 18+
- **Browser:** Chrome or Microsoft Edge
- **Target:** [Codex CLI](https://github.com/openai/codex) by OpenAI
