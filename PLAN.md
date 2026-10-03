# Mary Prompins — Plan

A practically perfect Claude skill that tidies up messy Claude Projects.

## Audience
Non-technical, phone-first Claude Project users.

## Distribution
- Public GitHub repo (private until v1)
- Gumroad listing at $0+ (suggested $3–5), linking to the repo — platform still open, see below
- Claude Code plugin marketplace from this repo: `/plugin marketplace add erdos2n/mary-prompins` → `/plugin install mary-prompins@prompins`
- Standalone product, separate from Grounded

## Shape
One skill, one install. Skill name: `prompins-tidy`.
Fallback trigger: "use Prompins" + any request.
In Claude Code the plugin namespace also prefixes it: `/mary-prompins:prompins-tidy`.

## Repo layout
```
.claude-plugin/marketplace.json          ← Claude Code marketplace catalog
plugins/mary-prompins/
  .claude-plugin/plugin.json             ← plugin manifest
  skills/prompins-tidy/
    SKILL.md                             ← router + house rules
    references/                          ← one file per mode
PROMPTS.md                               ← prompt card
PLAN.md                                  ← this file
```

## Modes & triggers

| Mode | Triggers |
|---|---|
| Onboard | "Let's optimize this project" · "Optimize this project" |
| Checkup | "Can we do some cleaning?" · "Can we clean up this project?" · "Let's clean this up" |
| Slim | "Slim my instructions" · "My instructions are too long" · "Trim my instructions" |
| Lookup doc | "Build me a lookup doc" · "Build my manifest" · "Make an index of my files" · "What's in my files?" |
| Discover | "Look at my past chats and find a skill" · "Am I missing out on any skills?" · "Do you see a skill we could add?" |

## Platform constraints (drive the design)
- Claude can READ project instructions and files; it CANNOT edit them
- All fixes are delivered as paste-ready code blocks or downloadable files
- Custom skills are account-level, not per-project
- Skill upload documented for web/desktop; assume one-time install at claude.ai
- Discover depends on the "Search and reference chats" setting; it hands off to the built-in skill-creator rather than rebuilding it

## Open decisions
1. Slim + Lookup doc: standalone prompts, or offered as follow-ups after Checkup? (v0.1: both — Checkup ends by offering one)
2. Checkup report format on a phone — v0.1 uses score + top 3 fixes; validate in testing
3. First real test case: Rafa's Knowledge Base project, scrubbed
4. Payment platform: Gumroad vs Ko-fi vs Payhip vs GitHub Sponsors
5. License (MIT?) before going public
6. GitHub Release with prebuilt `prompins-tidy.zip` for claude.ai users
7. Landing page: GitHub Pages?
