# Slim — "Slim my instructions"

Goal: hand the user a shorter, cleaner set of instructions to paste in, with every change explained.

## What belongs in project instructions

Instructions are loaded on **every message**, so they should only hold what's always true:

1. **Who I am** — a few lines of context about the user and the project's purpose
2. **How to talk to me** — tone, format, length
3. **Routing** — "when I ask about X, read file Y" (point to the lookup doc if there is one)
4. **Hard rules** — the handful of things that must never be broken, each with a short reason

Everything else moves somewhere better.

## Sort every line

| Bucket | Rule of thumb | Where it goes |
|---|---|---|
| **Keep** | True on every message | New instructions |
| **Move → file** | Reference info (lists, specs, bios, examples) | A project file, listed in the lookup doc |
| **Move → skill** | A multi-step procedure used only sometimes | Skill candidate — hand off to Discover / skill-creator |
| **Cut** | Duplicate, dead reference, stray paste, outdated | Gone (it's in the backup) |

## Output, in this order

1. **One-line summary:** *"Your instructions went from ~1,400 words to ~350."* (estimates are fine — say so)
2. **Change table:** Line (short quote) | Bucket | Reason. Group Cuts together if there are many.
3. **Backup:** create `old-instructions-YYYY-MM-DD.md` for download containing the current instructions verbatim. If you can't create files, tell the user to copy their current instructions somewhere safe first.
4. **New instructions** in ONE code block, labeled: *"Replace everything in your project instructions with this:"*
5. **Moved content:**
   - Files: create each as a downloadable `.md` file, labeled *"Upload this to your project files."*
   - Skills: list them as candidates and point to the next step.
6. **One next step:** usually *Say "build me a lookup doc"* (if files moved) or *Say "am I missing out on any skills?"* (if skill candidates exist).

## Writing the new instructions

- Keep the user's phrasing where it works; tighten, don't rewrite their personality out.
- Replace shouting with reasons: "NEVER use bullet points!!!" → "Write in short paragraphs — I find bullet lists hard to read."
- Use a small routing table instead of long if/then paragraphs.
- Aim for something that fits on one or two phone screens.
