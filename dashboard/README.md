# Dashboard (build on demand)

This folder is a SPEC, not an app. The dashboard gets built by the OS, with the owner, in chat, once there is real data to show. Building it earlier produces an empty shell that decays; building it on demand produces something the owner actually opens.

## Purpose

One screen of live company truth for {{COMPANY_NAME}}: where the pipeline stands, what the money says, what content is moving, what's due. The OS's files (kanban, STATUS.md, finances) stay the source of truth; the dashboard is a read-only window onto them plus whatever connectors are live.

## When to build it

After onboarding is complete AND at least 2 data connectors are live (for example: a finance source the scripts can reconcile, plus the clients/ folder in active use, or a content pipeline with real publishing history). Until then, the answer to "how's the business doing" is a chat question, and that's fine.

## What it shows (v1 scope, 4 widgets max)

- **Pipeline:** clients and prospects with stage + next step, read from `clients/*/STATUS.md`
- **Finances:** the key figures from `memory/finances.md`, each rendered WITH its provenance label; any figure a script didn't compute shows as "needs reconciliation", never as a guess (per the financial-accuracy rule)
- **Content:** drafts in flight, published this month, next scheduled, from `content-pipeline/` + `memory/calendar.md`
- **Tasks:** a mirror of `memory/kanban.md` columns

## Reference architecture

- **Default:** Next.js app deployed to Vercel, Supabase (free tier) as the data layer, small sync scripts that parse the repo's markdown into tables on a schedule or on git push
- **Lighter alternative:** sheet-backed (Google Sheets as the store, a single static page reading it) for owners who don't want another service
- Read-only first. Editing stays in the repo/chat where the audit trail lives. Write-back is a later phase if ever.
- Access control from day one: this is company-private data, so password protection or Vercel access protection minimum.

## How it gets built

The owner says "build my dashboard" in chat. The OS confirms which connectors are live, picks the architecture above, scaffolds the app in this folder, wires the data reads, deploys, and hands back a URL. Each later widget is added the same way: by asking. Treat every dashboard request as a normal deliverable (quality gate applies).

## What NOT to do

- Don't pre-build widgets for data that has no live source yet
- Don't let the dashboard become a second source of truth; if it disagrees with the repo, the repo wins and the sync gets fixed
- Don't render any financial number the reconciliation scripts didn't produce
