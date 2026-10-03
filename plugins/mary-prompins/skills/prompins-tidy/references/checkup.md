# Checkup — "Can we clean up this project?"

Goal: a phone-sized hygiene report with a score, the top 3 fixes, and one next step.

## 1. Inventory

- The project instructions (in your context). Count rough word length and number of sections.
- The project files: names, types, rough size. If code execution is on, list `/mnt/project/`.
- Whether a lookup doc already exists (a file named like LOOKUP, MANIFEST, INDEX, README).

## 2. Look for these problems

| Problem | What it looks like | Why it hurts |
|---|---|---|
| Duplicate rule | Same instruction in two places (or in instructions AND a file) | Copies drift apart and start contradicting |
| Conflict | Two rules that can't both be followed | The AI picks one at random |
| Dead reference | Mentions a tool, file, link, or setting that doesn't exist | Wastes attention; may cause errors |
| Stray paste | Leftover chat replies ("Now I'll update…", "Here's the revised…"), half code fences, notes-to-self | Confuses what is an instruction |
| Procedure in instructions | Step-by-step how-tos that only apply sometimes ("when logging X, do A, B, C") | Loaded every message even when irrelevant — should be a skill |
| Reference data in instructions | Long lists, specs, tables, bios | Should be a project file |
| Shouting | ALL CAPS, NEVER, CRITICAL, NON-NEGOTIABLE without a reason | Reasons work better than volume |
| Messy files | Vague names ("doc1.pdf"), duplicates, outdated versions, no lookup doc | The AI can't tell what to read when |

Quote the offending line (short) so the user can find it. Don't invent problems to fill a quota — a clean project gets a short report.

## 3. Score

Start at 10. Subtract:

| Finding | Points |
|---|---|
| Each conflict | −2 |
| Each dead reference or stray paste | −1 |
| Duplicates (any) | −1 |
| Procedures living in instructions (any) | −1 |
| Reference data living in instructions (any) | −1 |
| No lookup doc with 4+ files | −1 |
| Instructions longer than ~800 words | −1 |

Floor at 1.

## 4. Report format (keep it to about one phone screen)

```
Tidiness: 6/10

Top 3 fixes
1. [problem] — "[short quote]" → [fix]
2. ...
3. ...
```

Then a compact table of everything else found (Problem | Where | Fix).

Then exactly one next step, matched to the biggest problem:

| Biggest problem | Next step to offer |
|---|---|
| Instructions (duplicates, strays, procedures, shouting) | *Say "slim my instructions"* |
| Files (no lookup doc, messy names) | *Say "build me a lookup doc"* |
| Procedures that keep repeating | *Say "am I missing out on any skills?"* |
