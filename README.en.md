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
├── SKILL.md                    install flow + day-to-day rules
├── assets/hub-template.html    the to-do hub page
└── references/
    ├── onboarding.md           onboarding questionnaire
    ├── conventions.md          hub data rules
    ├── daily-rhythm.md         morning and evening check-ins
    ├── persona.md              personality
    └── safety.md               what it won't do
```

## License

MIT
