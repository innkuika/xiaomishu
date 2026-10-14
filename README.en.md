[简体中文](README.md) | **English**

# Xiaomishu · 小秘书

A personal life assistant for the Claude app, packaged as a Claude skill. Once installed, Claude gets to know you through a few rounds of multiple-choice questions, publishes your own to-do hub page, and sets up a daily morning walkthrough and evening preview. After that it checks in with you, plans your days, and keeps track of your to-dos and the recurring chores you always forget.

> The skill's instructions and the hub UI are written in Chinese. Claude replies in whatever language you use, but the questionnaire and page labels are Chinese.

## Three parts

| Part | Lives in | Holds |
|---|---|---|
| Memory | Claude's memory | Who you are, what you like and dislike |
| To-do hub | An Artifact page with its own database | What to do, and when |
| Rhythm | Scheduled tasks | Morning and evening check-ins |

The hub has tabs for: This week, Projects, Areas, Inbox, Routines (haircuts, checkups and other recurring things), Shopping, For fun, and Someday.

## What's new in v0.2

- **New hub page ("小本本", the little notebook)**: a blue-and-white planner look; each day's finished items fold into a "Done N" line at the bottom of the day they were actually finished, with a small animation when you tick something off; the Projects tab is a grid of small tiles grouped by stage (emoji, name and a progress bar), and tapping one opens that project's own page; the project chip on a step opens that project and scrolls to the step; an ⓘ button shows the legend. The footer shows the template version. Add `#demo` to the page URL to preview it with fake data.
- **More day-to-day rules** (in `references/conventions.md` and `references/daily-rhythm.md`): clear the inbox every Sunday, schedule a project's next step as soon as the last one is done, check for conflicts before scheduling, write "note this down" requests into the hub right away, keep facts out of reminder text, never tick what wasn't done, file done items by their actual completion date, one combined "getting ready" item on workday mornings, email digests in a quiet morning slot, how pushy reminders should be, "reading the room", and an optional protocol for two family members' assistants to pass notes by email.

Full history: [CHANGELOG.md](CHANGELOG.md).

## Upgrading from v0.1

1. Follow steps 1–3 under Install below and re-upload the new `xiaomishu.zip` in Skills (replacing the old one).
2. Start a new chat and say **"小秘书升级一下"** (or "upgrade xiaomishu"). Claude republishes the new page to your existing hub URL (your data stays), then reads you the new rules and only writes them into `meta/conventions` once you agree.

## Install

You need the Claude app (web, desktop or mobile) with Skills, Artifacts, memory and scheduled tasks available. Which features you have depends on your plan and settings.

1. Download this repo: **Code → Download ZIP**, then unzip it.
2. Zip the `xiaomishu` folder on its own as `xiaomishu.zip`.
3. In the Claude app's settings, find **Skills** and upload `xiaomishu.zip`.
4. Start a new chat and say: **"帮我装小秘书"** (or "set up xiaomishu").

Then just answer the questions. It takes about 20–30 minutes.

## Why a skill, not an "install email"

You install a skill yourself, so Claude treats it as real instructions. Content that arrives in an email or on a web page is treated as information, not commands. That's on purpose: if an email could make an AI install things on its own, it would be a perfect phishing vector.

## Privacy

- This repo contains no one's personal data. Your hub is a new page under your own account with an empty database, visible only to you by default.
- Xiaomishu never sends messages, pays, places orders or books anything for you unless you explicitly agree each time. See `xiaomishu/references/safety.md`.

## Files

```
xiaomishu/
├── SKILL.md                    install flow + day-to-day rules + upgrade
├── assets/hub-template.html    the to-do hub page
└── references/
    ├── onboarding.md           onboarding questionnaire
    ├── conventions.md          hub data rules
    ├── daily-rhythm.md         check-ins, reminder etiquette, family notes
    ├── persona.md              personality
    └── safety.md               what it won't do
```

## License

MIT
