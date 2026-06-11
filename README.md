# Imperium OS

An AI operating system for your company, installed in a day.

Imperium OS turns Claude Code into a system that knows your business, remembers everything you tell it, runs your repeat work through pre-built skills, and gets sharper every week you use it. You talk to it in plain English. It does the technical work.

Built and maintained by **Imperium Growth**.

---

## What's inside

- **44 skills.** Pre-built workflows for content, research, client delivery, strategy, quality control, and more. Each one triggers automatically when you ask for something it covers.
- **A rule layer.** Enforcement rules that keep output quality high: no AI-sounding writing, no invented numbers, research before claims, disagreement before agreement. The system pushes back when you need it to.
- **A memory system.** Everything you tell it lands in the right file, immediately. People, decisions, deadlines, finances, ideas. Nothing lives only in a chat window.
- **Hooks.** Deterministic guardrails that run on every interaction, so the important rules cannot be skipped or forgotten.
- **A self-improvement loop.** A registry of every skill and rule, plus a lint tool that finds drift, dead paths, and stale config. You review, it fixes.
- **Connectors.** Step-by-step guides for plugging in GitHub, Google Workspace, YouTube research, Telegram notifications, and optional extras. Each guide is written for someone who has never opened a terminal.
- **A setup dashboard.** A progress page that updates as you go, so you always know where you are.

## What you need

1. A computer (Windows or Mac).
2. A Claude subscription. Max is recommended; it gives the system room to work all day.
3. About an hour for the first session. You can stop at any point and pick up later.

No coding knowledge. No terminal experience. The system runs every command itself.

## Install

**Step 1. Get the files onto your computer.**
Your Imperium installer will send you this folder, or a link to clone it. If you received a zip, extract it somewhere easy to find, like your Documents folder.

**Step 2. Open it in Claude Code.**
Open the Claude Code app (or Cursor with the Claude Code extension) and open this folder as a project. If you don't have Claude Code yet, follow [docs/connectors/claude-code-install.md](docs/connectors/claude-code-install.md). It takes about ten minutes.

**Step 3. Type this into the chat:**

```
I've just installed this, let's start
```

That's the whole install. The system takes it from there.

## What happens next

The onboarding walks you through eight short phases, one question at a time:

1. **Welcome and tour.** What you're looking at and how to talk to it.
2. **Identity.** Your name, company, and what to keep private.
3. **Business context.** A short interview so the system knows what you do and who you sell to.
4. **Voice.** A few writing samples so everything it drafts sounds like you.
5. **Connections.** Plugging in the tools you already use, one at a time, verified as you go.
6. **First skills.** Turning 3 to 5 of your weekly tasks into automated workflows, and running each one for real.
7. **Cadence and memory.** Deciding what runs on a schedule and seeding your task board.
8. **Health check and graduation.** A baseline score, a week-one plan, and you're running.

Open [docs/setup-status.html](docs/setup-status.html) in your browser at any time to see live progress.

If you get interrupted, just come back and type **"continue onboarding"** or **"where were we"**. It remembers exactly where you stopped.

## The folder, at a glance

| Folder | What it's for |
|---|---|
| `context/` | The one-page truth about your company. Read first, every session. |
| `memory/` | Everything the system learns: people, decisions, tasks, dates. |
| `clients/` | One folder per client engagement. |
| `content-pipeline/` | Drafts, published work, research, and your voice profile. |
| `automations/` | The runtime tools, like YouTube research and notifications. |
| `dashboard/` | The spec for your live company dashboard (built with you on request, once 2+ connectors are live - see dashboard/README.md). |
| `docs/` | Guides, the architecture explainer, and the setup status page. |

Everything else is plumbing. You never need to touch it.

## Support

This system is delivered and supported by Imperium Growth as part of your engagement. First line of support is the chat itself: describe what happened in plain English and it will diagnose and fix most things on its own. For anything it can't solve, contact your Imperium installer.

Five-minute orientation: [docs/START-HERE.md](docs/START-HERE.md)
The visual map of how it all fits together: [docs/system-map.html](docs/system-map.html) (open in your browser)
How it works under the hood: [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md)

---

**Imperium OS · Built by Imperium Growth**
