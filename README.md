<p align="center"><img src="assets/icon.png" width="76" alt=""></p>

<h1 align="center">Trackage</h1>

<p align="center">
  <a href="https://dadsadadsadad.github.io/trackage-showcase/">Website</a> ·
  <a href="PRIVACY.md">Privacy</a> ·
  <a href="SECURITY.md">Security</a> ·
  <a href="https://github.com/dadsadadsadad/trackage-showcase/issues/new/choose">Feedback</a>
</p>

Usage, cost and context analytics for every AI coding agent you run: Claude Code, Codex, Gemini CLI, Qwen Code, OpenCode, ChatGPT exports, and your own apps that call an AI API. Across every computer you work on, in one dashboard.

**The source code is private.** This repo is the public page: what Trackage does, how it treats your data, and where to send feedback.

> Trackage is launching soon as a website. It replaces the AI Manager desktop app, which is discontinued; its old releases stay on this repo for existing users but get no updates.

## Why

Coding agents spend tokens in ways that are hard to see, and most people now use more than one. Trackage answers the questions single-tool trackers can't:

- **Is my subscription worth it?** The API-equivalent value of your usage against what Claude Max, ChatGPT Pro or Google AI Ultra costs you, plan by plan.
- **What would this have cost on another model?** Your exact token mix priced on 12 models from 6 vendors.
- **How do I compare?** Opt-in, anonymous benchmarks: efficiency, cache reuse, cost per prompt, tool failures.
- **What used up my limit?** Every call with its time and tokens, across all your machines.

## What it does

- **Live**: every running agent on every linked computer, with context fill, burn rate and cost per hour.
- **Your dashboard**: drag, resize, add and remove cards; build several dashboards; themes, custom colors, glass or outline cards.
- **Alerts** in the app, by email, or in Slack and Discord: agent finished, context nearly full, tool calls failing, budget or rate limit close.
- **Tasks, sessions, code, tools, models, projects**: where every token went, down to each step.
- **Budgets and forecasts**, a Monday email report, CSV/JSON export, and a usage API.
- **Recap** cards you can share.

## Free and Pro

|                                   | Free             | Pro ($9/mo or $84/yr)   |
| --------------------------------- | ---------------- | ----------------------- |
| Every supported agent             | ✓                | ✓                       |
| Computers                         | 1                | 10                      |
| History                           | 14 days          | unlimited               |
| Live view, dashboard, sessions    | ✓                | ✓                       |
| Subscription value, model what-if | preview          | ✓                       |
| Tasks, code, budgets              |                  | ✓                       |
| Alerts                            | in the app       | + email, Slack, Discord |
| Benchmarks                        | efficiency score | every metric            |
| Weekly report, export, usage API  |                  | ✓                       |

## How your data is handled

A small CLI (`npx trackage`) reads the logs your agents already save and sends **numbers only**: token counts, costs, timings, model and tool names, success or failure. Never prompts, replies, code, diffs, tool output or full paths. `trackage sync --dry-run` prints every byte before anything is sent. Details in [PRIVACY.md](PRIVACY.md).

## License

Trackage is proprietary software. The Free plan is free to use; Pro is a subscription.
