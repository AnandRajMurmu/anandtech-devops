# Journey with AnandTech — Repository Instructions

## Mission

Build a deep, beginner-to-production DevOps course using ChatGPT Work for execution, GitHub for durable state and approvals, and Slack for notifications.

## Required context

Before curriculum work, read completely:

1. `docs/master_prompt.md`
2. `docs/project_SSOT.md`
3. `workflow/STATUS.md`
4. The active section's `PLAN.md` and `SSOT.md`
5. The applicable contract under `agents/`

Read only the earlier units and supporting material required for the task.

## Authority order

1. Anand's latest explicit instruction
2. Locked current Section SSOT on `main`
3. `docs/project_SSOT.md`
4. `docs/master_prompt.md`
5. Accepted earlier units
6. Drafts and planning workbooks
7. General knowledge

Report conflicts; do not guess.

## GitHub governance

- `main` contains accepted state.
- Draft work uses focused branches and pull requests.
- Anand merging an SSOT PR into `main` is the lock.
- A locked SSOT changes only through a new owner-approved SSOT PR.
- Never generate a unit from an unmerged Section SSOT.
- Unit work is one unit and one PR at a time.
- Worker and Reviewer never modify an SSOT.
- Never begin the next section before explicit section acceptance.
- Never create a section ZIP unless Anand asks.
- Slack notifications never count as approval.

## Role boundaries

- Manager coordinates; it does not author or independently review units.
- SSOT Maker edits only the active section PLAN and draft SSOT.
- Worker edits only its assigned unit directory.
- Reviewer reviews and comments; it does not repair content.

## Course standard

Write mini-book-quality material, not brief notes. Use the applicable learning progression:

Problem → why → mental model → theory → worked example → guided practice → hands-on → evidence → controlled failure → troubleshooting → recovery → production connection → challenge → artifact → assessment → reflection.

Explain concepts before commands, define terms, interpret evidence, distinguish lab convenience from production engineering, and include safety, cleanup, recovery, and verification where relevant.

## Environment boundary

Do not introduce VMs, cloud accounts, privileged access, destructive commands, or infrastructure unless the current locked Section SSOT authorizes them.

## Completion report

Report changed files, authority checked, validation performed, unresolved decisions, and the exact next human action.
