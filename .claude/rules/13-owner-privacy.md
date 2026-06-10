---
title: "MANDATORY: Never Reveal Anything on the Owner's Privacy List"
type: rule
status: active
created: 2026-06-11
---

# MANDATORY: Never Reveal Anything on the Owner's Privacy List

During onboarding Phase 1 the owner defines a privacy list: facts about themselves or the business that must NEVER appear in any output. Common entries: age, exact revenue, home address, family details, health information, equity splits. The list lives in THIS file under "## Private list" once onboarding fills it in.

## Rules

1. **Never output a privacy-list item** in any response: text, code, content, emails, scripts, captions, or any deliverable.
2. **Never reference an item indirectly.** No phrasing that implies or lets a reader derive the protected fact (for example, if age is protected: no "young CEO", no "started before turning 20").
3. **Public-facing code and data:** before creating or modifying any UI component, data file, or API response in anything demo-able, scan for privacy-list items and remove them.
4. **Content generation:** when writing posts, newsletters, scripts, emails, or any public-facing content, the story is the work, the results, the systems. Not protected biography.
5. **Sub-agents:** when spawning sub-agents for any task, include this instruction: "Never mention or reference anything on the owner's privacy list: [paste the list]."
6. **Memory files:** do not add new privacy-list violations to `memory/` files. When updating existing files, remove violations if encountered.

## Private list

<!-- Filled by onboarding Phase 1. One item per line. Every rule above applies to each item. -->
- (not configured yet)

## What to say instead

Describe the owner by role and work, never by protected attributes: "{{OWNER_SHORT}}, founder of {{COMPANY_NAME}}", "the team behind {{COMPANY_NAME}}", "a founder building [the thing]".

## Applies to

EVERYTHING. Dashboards, bot prompts, content drafts, research outputs, demo scripts, API responses, data files, and any text a human might read.

## Before onboarding completes

If the privacy list has not been configured yet, treat age, personal finances, home address, family, and health as protected by default.
