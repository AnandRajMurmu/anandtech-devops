# ChatGPT Work Setup

## Architecture

ChatGPT Work executes the Manager, SSOT Maker, Worker, and Reviewer roles. GitHub stores durable state and approvals. Slack carries notifications only. No API server, runtime, database, webhook service, or deployment is required.

## One-time setup

1. Connect the GitHub plugin to `AnandRajMurmu/anandtech-devops`.
2. Connect the Slack plugin.
3. Create a ChatGPT Work project named **AnandTech DevOps Manager**.
4. Add this repository as project context.
5. Use `agents/MANAGER.md` for the Manager.
6. Create the three specialist agents from the other files in `agents/`.
7. Give SSOT Maker and Worker GitHub access only.
8. Give Reviewer GitHub and Slack access.
9. Select and test the Slack notification channel.
10. Test all roles manually before enabling triggers.

## Manual pilot

1. Manager reports current authoritative state.
2. SSOT Maker revises only Section 00 PLAN and draft SSOT.
3. Anand reviews the SSOT PR and merges only to lock it.
4. Manager assigns Unit 01.
5. Worker opens the unit PR.
6. Reviewer requests bounded changes or approves.
7. Reviewer notifies Slack after a terminal verdict.
8. Anand reviews and merges.
9. Repeat one unit at a time.
10. Manager stops after the section and waits for acceptance.

## Later event triggers

After the pilot works:

- merged SSOT PR → Manager identifies first authorized unit;
- opened or updated unit PR → Reviewer checks it;
- requested changes → Worker repairs the same PR;
- approval → Slack notification;
- merged unit PR → Manager identifies next unit;
- final unit merged → section-ready notification.

Keep human gates for SSOT locking, section acceptance, and packaging.

## Useful prompts

- “Manager, report the current authoritative state.”
- “SSOT Maker, prepare Section NN as a draft PR. Do not lock it.”
- “Worker, generate only Unit NN from the locked Section NN SSOT.”
- “Reviewer, review PR #NN and notify Slack only on a terminal verdict.”
