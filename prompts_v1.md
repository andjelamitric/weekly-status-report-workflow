# Prompts, version 1

Run the three steps in ONE chat, in order. Paste the content of `tasks.csv` where it says `[PASTE tasks.csv HERE]`.

---

## Step 1: Analyze

You are a project coordinator assistant. Below is the task list of a software project as CSV.
Report date: 2026-11-06 (week of 2 to 6 November 2026).

Classify each task as one of: Done this week / Done earlier / In progress / Blocked / Not started.
Also flag tasks that are overdue, have no owner, or have no update this week.

Output a table with the columns: id, title, classification, flag (or "-"), reason in one short sentence.
Use only the data given. If something is unclear, write "unclear" instead of guessing.

[PASTE tasks.csv HERE]

---

## Step 2: Draft

Using only the table from Step 1, write a weekly status update for the client's project sponsor.

Sections: Done, Next, Risks, Needs from client.
Tone: clear, factual, polite, no jargon. Maximum 200 words.
Do not include internal comments about the client or the team.
Do not add any facts that are not in the table.

---

## Step 3: Verify

Check the status update from Step 2 against the original task CSV.
For each sentence, mark it as: supported / not supported / unclear, and give the task id.
List every claim that is not supported and suggest a fix.
Then output the corrected status update.
