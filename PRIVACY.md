# Privacy

_Last updated: October 20, 2026_

Trackage is a website plus a small command-line collector. The full privacy policy is published on the Trackage website at launch; this is the short version.

## What the collector sends

Per agent session: token counts, timestamps, model names, tool names with success or failure, context size, lines added and removed, and a project label you control (or a hash, or nothing). Session and file ids are anonymised with a secret that stays on your computer.

At the **standard** level it also sends command names without arguments (for example `npm test`) and anonymous file ids with only the extension. At the **detailed** level, which is off by default, it adds session titles, short prompt previews and file paths inside the project.

## What is never sent

Full prompts, model replies, code, diffs, file contents, tool inputs and outputs, shell command arguments, absolute paths, branch names, environment variables or secrets. The server rejects any upload that contains free text.

Run `trackage sync --dry-run` to see the exact payload before anything leaves your machine, or read the [collector's source](https://github.com/dadsadadsadad/trackage-cli).

## What we never do

- Sell or share your own data.
- Use advertising or third-party tracking cookies.

If you join a **team**, its owner and admins see your usage numbers for the projects you leave visible, with your name and email; other members see the team's totals. Titles, prompts, files and computers are never shown to a team, and leaving removes your numbers at once.

If you connect **Anthropic or OpenAI** for bill matching, the Admin key is stored encrypted and used only to read the daily cost report; only the total per day is kept. **Phone and browser notifications** are encrypted so the push service can't read them.

Two programs exist only if you opt in: anonymous **community benchmarks** (others see percentiles over the whole group, never your numbers) and an anonymous **research program** that publishes aggregate statistics, only over groups of at least 25 people.

## Your control

Unlink a computer and delete its history, export everything we hold as JSON, or delete your account at any time from Settings.

## The old desktop app

The discontinued AI Manager desktop app ran entirely on your computer and uploaded nothing. Its releases remain available but are no longer updated.

Questions: open an issue at [github.com/dadsadadsadad/trackage-showcase/issues](https://github.com/dadsadadsadad/trackage-showcase/issues).
