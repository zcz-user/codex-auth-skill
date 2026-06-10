<p align="center">
  <img src="https://img.shields.io/badge/🧩%20Codex%20Skill-8A2BE2?style=for-the-badge" alt="Codex Skill">
  <img src="https://img.shields.io/badge/Available%20on%20ClawHub-1a1a2e?style=for-the-badge&logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI2NCIgaGVpZ2h0PSI2NCIgdmlld0JveD0iMCAwIDY0IDY0Ij48cGF0aCBmaWxsPSIjZmZmIiBkPSJNMzIgNEMxNi41IDQgNCAxNi41IDQgMzJzMTIuNSAyOCAyOCAyOCAyOC0xMi41IDI4LTI4UzQ3LjUgNCAzMiA0em0xNCAzOUwxNCAzMmwzMi0xMXYxNXoiLz48L3N2Zz4=" alt="ClawHub"></p>

<h1 align="center">Codex Auth Refresh</h1>

<p align="center">
  <b>🧩 ClawHub Skill for Codex CLI</b><br>
  <sub>Refresh Codex CLI auth.json from your ChatGPT browser session</sub>
</p>

<p align="center">
  <a href="https://clawhub.com/skill/codex-auth-session">
    <img src="https://img.shields.io/badge/Install%20from%20ClawHub-codex--auth--session-8A2BE2?style=flat-square" alt="Install from ClawHub">
  </a>
  <img src="https://img.shields.io/badge/Windows-0078D6?style=flat-square&logo=windows" alt="Windows">
  <img src="https://img.shields.io/badge/Node.js-18%2B-339933?style=flat-square&logo=node.js" alt="Node">
  <img src="https://img.shields.io/badge/Chrome%2FEdge-4285F4?style=flat-square&logo=googlechrome" alt="Chrome/Edge">
</p>

---

## 🧩 What Is This?

This is an **OpenClaw agent skill** that provides Windows tooling to refresh Codex CLI's `auth.json` from a ChatGPT web session.

**Install via ClawHub:**
```bash
clawhub install codex-auth-session
```

**Or clone and use directly:**
```bash
git clone https://github.com/zcz-user/codex-auth-skill.git
cd codex-auth-skill
```

Then refer to [`SKILL.md`](./SKILL.md) for full instructions, or browse the [`scripts/`](./scripts/) directory for PowerShell commands.

## 📁 Structure

```
codex-auth-skill/
├── SKILL.md                     # Skill instructions (for agent)
├── scripts/                     # PowerShell scripts + core JS
│   ├── login-profile.ps1
│   ├── run-refresh.ps1
│   ├── status.ps1
│   ├── install-scheduled-task.ps1
│   ├── create-desktop-toolbox.ps1
│   └── refresh-codex-auth.js
├── references/                  # Full documentation
│   ├── README.md                # English docs
│   ├── README_zh.md             # 中文文档
│   ├── SECURITY.md
│   └── CONTRIBUTING.md
└── .gitignore
```

## 🔗 Links

| Link | What |
|------|------|
| [🐙 Original tool repo](https://github.com/zcz-user/codex-auth-session-refresh) | The standalone tool (Windows setup + docs) |
| [🧩 ClawHub skill](https://clawhub.com/skill/codex-auth-session) | Install via `clawhub install codex-auth-session` |
| [📦 GitHub source](https://github.com/zcz-user/codex-auth-skill) | This repo — skill source files |

---

<p align="center">
  <sub>🧩 Codex Skill — for Codex CLI users who just want auth to work</sub>
</p>
