# Mary Prompins ☂️

A practically perfect Claude skill that tidies up messy Claude Projects.

If your project's AI forgets things, ignores your instructions, or can't find the right file, your project probably needs a cleaning. Mary Prompins checks it, slims your instructions, builds a lookup doc for your files, and finds skills hiding in your past chats.

## What it does

| Say | Mary will |
|---|---|
| "Let's optimize this project" | Get you set up and run a first checkup |
| "Can we clean up this project?" | Give you a tidiness score and the top 3 fixes |
| "Slim my instructions" | Hand you shorter instructions to paste in, plus a backup of the old ones |
| "Build me a lookup doc" | Make an index of your files for you to upload |
| "Am I missing out on any skills?" | Search your past chats for repeated work worth turning into a skill |

Full list: [PROMPTS.md](PROMPTS.md)

## Install

### Claude app (claude.ai)

> One-time setup, done in a browser (web or desktop). After that it works in the phone app too.

1. Turn on **Code execution and file creation** in Settings → Capabilities.
2. Download `prompins-tidy.zip` from the latest Release. *(coming soon — for now, zip the folder `plugins/mary-prompins/skills/prompins-tidy`)*
3. Go to **Customize → Skills → + → Create skill → Upload a skill** and pick the zip.
4. Open any project and say **"Let's optimize this project."**

### Claude Code

```
/plugin marketplace add erdos2n/mary-prompins
/plugin install mary-prompins@prompins
```

## Good to know

- Mary can **read** your instructions and files but can't **edit** them — she hands you paste-ready text and downloadable files.
- Skills are installed on your account, so Mary is available in every project.
- Finding skills in past chats needs **Search and reference chats** turned on in Settings.

## Support

Mary Prompins is free. If she saved you a headache and you'd like to say thanks, a tip is always appreciated — never expected.

☂️ **Venmo:** [@rafa2](https://venmo.com/code?user_id=2129500326330368350)
