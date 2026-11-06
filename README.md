# Weekly Status Report Workflow (prompt chain)

A small multi-step prompt workflow that turns a project task list into a short, client-facing weekly status update, with a built-in check against invented facts.

## Why

Status updates take time every week and are easy to get wrong: a task marked "Done" may still wait for client sign-off, a blocker may be hidden in a note, and internal remarks must not reach the client. This workflow tests how far an AI assistant can help with that, and where a human still has to check.

## How it works

1. **Analyze**: the model classifies each task and flags overdue, ownerless or stale items.
2. **Draft**: from that table only, the model writes the client update (Done / Next / Risks / Needs from client).
3. **Verify**: the model checks every sentence of the draft against the original data and corrects unsupported claims.

The prompts are in `prompts_v1.md` (and later versions). The sample data in `tasks.csv` is **fictional** and contains deliberate inconsistencies to test the workflow (for example a task marked "Done" that still waits for sign-off, a task without an owner, and an internal remark about the client).

## How to run

1. Open a chat with an AI assistant (model used: **[WRITE THE MODEL NAME]**).
2. Paste Step 1 with the content of `tasks.csv`.
3. Paste Step 2, then Step 3, in the same chat.
4. Read the final text yourself before it goes to anyone.

## Iteration log

| Version | What I changed | What went wrong before | Result |
| --- | --- | --- | --- |
| v1 | First version | - | [WRITE WHAT YOU SAW] |
| v2 | [WRITE] | [WRITE] | [WRITE] |

## What I learned

- [WRITE: where did the model make mistakes?]
- [WRITE: which instruction fixed it?]
- [WRITE: what must a human always check?]

## How AI was used

[EDIT TO MATCH WHAT IS TRUE] The sample data and the first prompt version were drafted with the help of Claude. I ran the workflow, evaluated the outputs, and made the changes described in the iteration log.

## Possible next steps

- Run the same chain with real data from a task tracker export.
- Automate the three steps with a script and an API.
- Add a fourth step that suggests next actions for the project manager.
