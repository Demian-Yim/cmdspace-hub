---
title: cmdtrace
source: https://cmdtrace.cmdspace.work/
author: 구요한 (CMDSPACE)
fetched: 2026-08-28
note: markitdown HTML→MD 자동 변환 스냅샷. 정확한 원문은 source URL 참조.
---

[
CMD
TRACE
]

[PROBLEM](#problem)
[SOLUTION](#solution)
[FEATURES](#features)
[DOWNLOAD](#download)

EN
[GET APP →](#download)

FOR DEVELOPERS WHO USE AI

# "WHERE WAS THAT CODE CLAUDE WROTE FOR ME?"

47 sessions this week. The solution is buried in #23... or #31?
**STOP DIGGING. START FINDING.**

[↓ DOWNLOAD FREE](#download)
[SEE THE PROBLEM ↓](#problem)

3
CLI TOOLS

/

∞
SESSIONS

/

0
LOST CONVOS

THE PROBLEM

## SOUND FAMILIAR?

01

### "I KNOW CLAUDE SOLVED THIS..."

You remember the conversation but can't find it. Yesterday? Last week? Which folder?

`~/.claude/projects/*/sessions/*.jsonl`
127 files • 2.3GB

02

### "MY SESSIONS ARE EVERYWHERE"

Claude Code here, OpenCode there, Antigravity somewhere else. No unified view.

📁 ~/.claude/

📁 ~/.opencode/

📁 ~/.antigravity/

03

### "WHAT WAS THIS SESSION?"

Session names like "01JHHK9X2M..." tell you nothing. Open each one hoping it's right.

01JHHK9X2MPQR5...
01JHHKB3NWXY7Z...
01JHHKD8KABC12...

DEVELOPERS LOSE **15-30 MIN/DAY** SEARCHING FOR PAST AI CONVERSATIONS.

THAT'S **2+ HOURS/WEEK** OF PRODUCTIVITY GONE.

THE SOLUTION

## CMDTRACE BRINGS ORDER TO CHAOS

A native macOS app that understands how you work with AI coding assistants.

CmdTrace

![CmdTrace main interface](screenshots/01-main-sessions.png)

🔍

#### FIND IN SECONDS

Search by content, title, tag, or project.

🏷️

#### YOUR ORGANIZATION

Custom names, tags with bulk rename, favorites.

⚡

#### INSTANT RESUME

Jump back into any session with one click.

📊

#### USAGE INSIGHTS

Track your AI usage, costs, and burn rate.

FEATURES

## BUILT FOR HOW YOU WORK

SEARCH

### FIND ANYTHING, INSTANTLY

Powerful search operators for laser-precise results.

`content:authentication`
→ Search inside conversations

`tag:backend project:api`
→ Filter by tag and project

`title:refactor date:today`
→ Find today's refactoring

![Search feature](screenshots/02-search.png)

MULTI-CLI

### ALL YOUR AI TOOLS, ONE PLACE

Switch between Claude Code, OpenCode, and Antigravity instantly.

CLAUDE CODE
`~/.claude/projects/*/sessions/`

OPENCODE
`~/.opencode/sessions/`

ANTIGRAVITY
`~/.antigravity/sessions/`

![CLI switcher](screenshots/03-cli-switch.png)

MONITORING

### KNOW YOUR USAGE

Real-time monitoring with burn rate predictions.

* ✓ Token usage by model (Opus, Sonnet, Haiku)
* ✓ Cost tracking with burn rate projection
* ✓ Plan limits for Pro, Max5, Max20
* ✓ Integrates with ccusage & claude-monitor

![Dashboard](screenshots/04-dashboard.png)

AI POWERED

### AI-GENERATED SUMMARIES

Let AI analyze sessions and generate meaningful titles.

* ✓ Auto-generate session titles from content
* ✓ Smart summaries for quick context
* ✓ Multiple AI providers supported

![AI summary](screenshots/06-ai-summary.gif)

HOW IT WORKS

## 3 STEPS

1

#### DOWNLOAD & LAUNCH

Install CmdTrace. It auto-finds your AI session folders.

→

2

#### ORGANIZE YOUR WAY

Add names, tags, favorites. AI can auto-generate titles.

→

3

#### FIND & RESUME

Search, browse, jump back into any session instantly.

![Resume session](screenshots/05-resume.gif)

![CmdTrace](icon-transparent.png)

## STOP LOSING CONVERSATIONS. START FINDING THEM.

Free and open source. Your data stays on your machine.

v2.4.2
•
macOS 14+
•
Native SwiftUI

[APPLE SILICON](https://github.com/johnfkoo951/CmdTrace/releases/download/v2.4.1/CmdTrace-2.4.1-arm64.dmg)
[INTEL MAC](https://github.com/johnfkoo951/CmdTrace/releases/download/v2.4.1/CmdTrace-2.4.1-x86_64.dmg)

6.6 MB each • DMG installer

⚠️

**"App is damaged" warning?**

Run this command in Terminal:

`xattr -cr /Applications/CmdTrace.app`

🔐

**Resume not working?**

System Settings → Privacy → Automation → CmdTrace → Terminal ✓

BUILD FROM SOURCE:

`git clone https://github.com/johnfkoo951/CmdTrace`
`cd CmdTrace && ./build-app.sh`

[
CMD
TRACE
]

[GITHUB](https://github.com/johnfkoo951/CmdTrace)
[X](https://x.com/YohanKoo)
[THREADS](https://www.threads.net/%40yohan_koo)
[YOUTUBE](https://www.youtube.com/%40cmdspace)
[CONTACT](https://litt.ly/cmds)
