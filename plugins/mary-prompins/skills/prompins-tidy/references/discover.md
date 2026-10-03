# Discover — "Am I missing out on any skills?"

Goal: find the workflows this user keeps repeating in this project and propose them as skills. Then hand off to the built-in skill-creator — don't build the skill yourself.

## 1. Check access

- Past-chat search must be available (the user's "Search and reference chats" setting). Inside a project, search only covers that project's chats — which is exactly what we want.
- If search isn't available: tell the user which setting unlocks it, then offer a fallback — *"Or tell me 2–3 things you find yourself explaining or asking for over and over."*

## 2. Search for repetition

Run several searches using content words from the project's topic and instructions. Look for:

| Signal | Example |
|---|---|
| Same multi-step request across chats | "log my meal", "draft a follow-up email" every week |
| Context the user keeps re-explaining | "remember, the format is…" |
| Corrections the user keeps making | "no, I told you to use…" |
| Templates or formats pasted repeatedly | the same table layout, the same headings |
| Procedures already sitting in the instructions | anything Slim marked "Move → skill" |

Also check which skills the user already has, and don't propose duplicates.

## 3. Report the top 3 candidates

| Skill idea | What it would do | Evidence | Would trigger on |
|---|---|---|---|
| weekly-recap | Turns notes into the Friday update format | Asked in 6 chats | "do my weekly recap" |

Rank by how often it shows up and how much re-explaining it would save. If you find nothing worth a skill, say so plainly.

## 4. Hand off

When the user picks one, give them a ready-to-send prompt for the built-in skill-creator, in its own code block:

```
Use skill-creator to build a skill called [their-prefix]-weekly-recap that turns my notes into my Friday update format: [the format details you found].
```

Notes for the handoff:
- Suggest a short personal prefix for their skill names (e.g. their initials) so it never collides with other skills.
- skill-creator is a built-in example skill; if it isn't available, tell the user it can be turned on in their skills settings.
- After the skill is installed, the matching procedure can be cut from their instructions — offer *"Say 'slim my instructions'"* to do it.
