# Privacy Policy

_Last updated: October 19, 2026_

AI Manager is a desktop app that runs entirely on your computer. This page explains what it reads, what it stores and what it never does.

## What AI Manager reads

- Session logs that **Claude Code** saves in `~/.claude/projects`.
- Session logs that **Codex** saves in `~/.codex/sessions`.
- Any extra folders you add in **Settings → Data & sources**.
- A ChatGPT data export, only if you choose to import one.

These files are read, never modified. They can contain your prompts and code; that content is shown to you in the app and goes nowhere else.

## What AI Manager stores

All in your user profile, on your computer:

- `~/.aimanager/config.json`: your settings, budgets, alert choices and license key.
- `~/.aimanager/archive/`: copies of your logs, only if you turn on **Keep history**.
- `~/.aimanager/imports/`: an imported ChatGPT export, if any.
- Window position and size, in the app's own data folder.

Uninstalling the app leaves `~/.aimanager` in place so you don't lose history; delete that folder to remove everything.

## What AI Manager never does

- It does not upload your data, prompts, code or usage anywhere.
- It has no analytics, telemetry, ads or tracking.
- It does not require an account.
- Its dashboard is served only to your own computer (`127.0.0.1`). Network mode is opt-in and protected by a token.

## Purchases

If you buy AI Manager Pro, the purchase is handled by our payment provider (Lemon Squeezy), which receives the details you give at checkout, under its own privacy policy. We receive your email address and order details so we can send and support your license key. The app checks keys offline and doesn't contact any server to do so.

## Contact

Questions or requests: open an issue at [github.com/dadsadadsadad/ai-manager-showcase/issues](https://github.com/dadsadadsadad/ai-manager-showcase/issues).
