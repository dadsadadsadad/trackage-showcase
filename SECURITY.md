# Security

## What the app can and can't do

- **Reads** the session logs Claude Code (`~/.claude/projects`) and Codex (`~/.codex/sessions`) save, plus any folders you add in Settings. It never modifies them.
- **Writes** only to `~/.aimanager` (settings, an optional log archive, an imported ChatGPT export) and the Electron user-data folder (window position).
- **Network**: serves the dashboard on `127.0.0.1:4317`. It makes no outbound requests of its own; the only outside links are ones you click, which open in your browser.
- **Starts with Windows** only if you tick that in the tray menu.

## Hardening

- Requests must use one of this computer's host names, which blocks DNS rebinding.
- Cross-origin requests and WebSocket connections from other sites are refused, so a web page can't read your dashboard data.
- Any request that changes state must carry an app-specific header, which an HTML form on another site can't add.
- Network mode (`--host 0.0.0.0`) always requires a token, compared in constant time.
- Responses carry a strict Content Security Policy, `X-Frame-Options: DENY`, `nosniff` and `no-referrer`.
- Electron windows use context isolation and the sandbox, can't navigate to other sites or open webviews, and only get notification permission.
- License keys are verified offline with Ed25519; the signing key never ships with the app.

## Reporting a problem

Please report security issues privately through [GitHub's private vulnerability reporting](https://github.com/dadsadadsadad/ai-manager-showcase/security/advisories/new) rather than a public issue.
