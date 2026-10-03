# Lookup doc — "Build me a lookup doc"

Goal: one file that tells the AI what's in every project file and when to read it. (Internally this is a manifest; call it a "lookup doc" with the user.)

## Steps

1. List every project file. If code execution is on, read `/mnt/project/`; otherwise use the files visible in your context.
2. Skim each file just enough to describe it in one line. Don't summarize the whole thing.
3. Flag problems as you go: duplicates, near-duplicates, outdated versions, vague names.
4. Build `LOOKUP.md` with the template below and offer it as a download.
5. Give the user ONE line to add to their instructions, in its own code block:

```
Before answering from project files, check LOOKUP.md to find the right file.
```

6. Tell them: *"Upload LOOKUP.md to your project files, then add that line to your instructions."*

## Template

```markdown
# Lookup Doc

Updated: YYYY-MM-DD

| File | What it is | Read it when… |
|---|---|---|
| resume-2026.pdf | My current resume | Writing cover letters, bios, job applications |
| brand-colors.md | Hex codes and fonts | Making anything visual |

## Cleanup suggestions
- `notes.pdf` and `notes-final.pdf` look like duplicates — keep one.
- `doc1.pdf` → rename to something descriptive, e.g. `lease-agreement-2025.pdf`.
```

## Rules

- The "Read it when…" column is the most important one — write it as situations the user would actually be in.
- If a file is huge or mostly irrelevant, say so in the cleanup section.
- When files are added later, the user can say "update my lookup doc" and you regenerate it.
