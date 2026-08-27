---
title: system.cmdspace.work
source: https://system.cmdspace.work/
author: 구요한 (CMDSPACE)
fetched: 2026-08-28
note: markitdown HTML→MD 자동 변환 스냅샷. 정확한 원문은 source URL 참조.
---

[![CMDS](/assets/logos/cmds-logo-round.png)
CMDS System Files](/)

[Architecture](#architecture)
[Process](#process)
[Docs](/docs/)
[GitHub](https://github.com/johnfkoo951/cmds-system-files)
[Read the docs →](/docs/)

한

CMDS v4.10.2 · Updated 2026-08-27
CMDS v4.10.2 · 2026-08-27 업데이트

# Knowledge architecture for humans and AI. 사람과 AI를 위한 지식 아키텍처.

The open specification behind a 10,000-note Obsidian vault. Six system files, eight shared rules, eight slash commands — shared openly so you can adapt them to your own second brain.
10,000개 노트 규모 Obsidian 볼트를 떠받치는 공개 규격. 여섯 개의 시스템 파일, 여덟 개의 공유 규칙, 여덟 개의 슬래시 커맨드 — 당신의 세컨드 브레인에도 맞춰 쓸 수 있도록 공개합니다.

[Read the docs문서 읽기](/docs/)
[Download (121KB)다운로드 (121KB)](/files/CMDS-System-Files.zip)
[GitHub](https://github.com/johnfkoo951/cmds-system-files)

10,000+

notes

노트

6

system files

시스템 파일

9

CMDS categories

CMDS 카테고리

120+

plugins

플러그인

The Idea

핵심 아이디어

## A knowledge management system should document itself — both for the human who maintains it and for the AI that reads it. 지식관리 시스템은 스스로를 문서화해야 한다 — 유지하는 사람에게도, 읽어주는 AI에게도.

CMDS (커맨드스페이스) is a Personal Knowledge Management system that has grown past 10,000 notes across 91 categories. At that scale, the system itself needs rules — where files go, how they're named, what properties they carry, which conventions agents must follow.

These system files *are* those rules. They're loaded into every Claude Code session as context. They're read by Gemini, Codex, and Cursor. And now they're shared so you can fork the architecture for your own vault.

CMDS(커맨드스페이스)는 91개 카테고리와 10,000개 노트 규모로 성장한 개인 지식관리 시스템입니다. 그 규모에서는 시스템 자체에 규칙이 필요합니다 — 파일이 어디 가는지, 이름은 어떻게 짓는지, 어떤 프로퍼티를 갖는지, 에이전트는 어떤 관행을 따라야 하는지.

이 시스템 파일들이 *바로* 그 규칙입니다. Claude Code 세션마다 컨텍스트로 로드되고, Gemini·Codex·Cursor가 읽으며, 이제 여러분의 볼트를 위해 포크할 수 있도록 공개됩니다.

The Architecture
아키텍처

## Six files, ordered by precedence. 여섯 개 파일, 우선순위 순으로 로드.

Each file serves a distinct audience. `@include` directives pull shared rules inline; precedence numbers settle conflicts when two files give different advice.
각 파일은 분명한 대상 독자를 가집니다. `@include` 디렉티브로 공유 규칙을 인라인 로드하고, 두 파일이 충돌할 때는 precedence 숫자가 판정합니다.

1

`CLAUDE.md`AI

Claude Code technical guide — file rules, vault commands, Obsidian syntax, output paths.

Claude Code 기술 가이드 — 파일 규칙, 볼트 명령, Obsidian 문법, 출력 경로.

Claude Code

2

`AGENTS.md`AI

Portable rules for every other AI coding agent operating in the vault.

볼트에서 동작하는 타 AI 코딩 에이전트용 이식 규칙.

Gemini · Codex · Cursor

4

`CMDS.md`AI

System philosophy and user context — the why and the who.

시스템 철학과 사용자 컨텍스트 — why 와 who.

All LLMs

5

CMDS GuideHUMAN

Operational standards — required properties, templates, naming conventions.

운영 표준 — 필수 프로퍼티, 템플릿, 이름 규칙.

User + AI

6

CMDS Head QuarterHUMAN

The navigation hub — 91 categories across 100–900 CMDS sections.

네비게이션 허브 — 100–900 섹션의 91개 카테고리.

User

9

`DESIGN.md`VISUAL

Visual language spec — brand tokens, anti-AI-slop rules, skill-to-surface mapping.

시각 언어 규격 — 브랜드 토큰, Anti-Slop 규칙, 스킬↔서피스 매핑.

All visual-output agents

Precedence 3 (ANTIGRAVITY · Gemini), 7–8 (BRAIN · BRAIN\_PROMPT · Gobi) are 3 private files, not distributed.
Precedence 3 (ANTIGRAVITY · Gemini), 7–8 (BRAIN · BRAIN\_PROMPT · Gobi) 은 비공개 3개 파일로, 배포 대상이 아닙니다.

The CMDS Process
CMDS 프로세스

## Four verbs. Four stages. One lifecycle. 네 개의 동사, 네 개의 단계, 하나의 생애주기.

Every note travels the same path — captured, integrated, developed, shared. Each stage has a matching slash command that encodes the workflow.
모든 노트는 같은 길을 지나갑니다 — 포착, 통합, 발전, 공유. 각 단계는 해당 워크플로를 인코딩한 슬래시 커맨드를 갖습니다.

C

Connect

/connect → 📖 100 Themes

Capture ideas, terminology, variables from the inbox as stub notes.

인박스의 아이디어 · 용어 · 변수를 스텁으로 포착.

M

Merge

/merge → 📖 200 Literature

Synthesize multiple notes into a single integrated literature note.

여러 노트를 하나의 통합 문헌 노트로 합성.

D

Develop

/develop → 📖 300–600

Apply method, build an artifact — code, prompt, curriculum, specialty.

방법론 적용, 산출물 제작 — 코드 · 프롬프트 · 커리큘럼 · 전문성.

S

Share

/share → 📖 700–800

Orchestrate existing skills to produce outputs — essays, slides, video.

기존 스킬을 오케스트레이션해 산출물 생성 — 에세이 · 슬라이드 · 영상.

Two audiences, one source
두 독자, 하나의 원천

## Built for humans and AI alike. 사람과 AI 양쪽을 위해.

AI Agents

AI 에이전트

Loaded into context at session start. Every agent references the same precedence-ordered source of truth.

세션 시작 시 컨텍스트로 로드. 모든 에이전트가 동일한 precedence 순서의 원천을 참조.

* Claude Code `CLAUDE.md`
* Gemini CLI `AGENTS.md`
* Codex · Cursor `AGENTS.md`
* Any LLM assistant모든 LLM 어시스턴트 `CMDS.md`

Human Readers

인간 독자

The vault maintainer, collaborators, and curious readers who want to adapt the system.

볼트 관리자, 협업자, 그리고 이 시스템을 자신에게 맞추고 싶은 독자.

* Navigation hub네비게이션 허브 `Head Quarter`
* Standards표준 `CMDS Guide`
* Philosophy철학 `CMDS.md`
* Templates · Workflows템플릿 · 워크플로 `all files`

The 9 Categories
9개 카테고리

## Every note has a home. 모든 노트는 갈 곳이 있습니다.

100 through 900 — a numeric hierarchy inspired by academic taxonomies. 91 subcategories. 10,000+ notes know where they belong.
100부터 900까지 — 학문적 분류 체계에서 영감을 받은 숫자 계층. 91개의 하위 카테고리. 만 개가 넘는 노트가 자신의 자리를 압니다.

100

Themes

Interests · Topics · Variables · Terminologies

200

Literature

Concepts · Frameworks · Theories · Classics

300

Data

Datasets · Questionnaires · Panel Data

400

Methodologies

Research · Statistics · ML · Codes · Prompts

500

Products

Obsidian · ChatGPT · Claude · n8n

600

Specialties

PKM · Second Brain · Gen AI · Productivity

700

Creatives

YouTube · SNS · Music · Digital Art

800

Outputs

PhD · Articles · Lectures · Consulting

900

Divisions

9 operational divisions

Inside a note
노트 한 편의 내부

## Seven required properties. Every note. No exception. 일곱 가지 필수 프로퍼티. 모든 노트. 예외 없음.

Structured frontmatter is how AI agents tell notes apart at scale. English `description` fields double as relevance hints for LLM search.
구조화된 frontmatter는 AI 에이전트가 대량의 노트를 구분하는 방식입니다. 영어로 쓴 `description` 필드는 LLM 검색의 관련성 힌트 역할을 겸합니다.

📄 example-note.md

---
type: note
aliases: []
description: "Meeting minutes from 2026-04-07 retrospective. Contains feedback summary and next-action items."
author:
- "[[Yohan Koo]]"
date created: 2026-04-18
date modified: 2026-04-18
tags: [CMDS, meeting]
# optional
CMDS: "[[📚 831 Consulting]]"
status: completed
---

## Fork the architecture. Keep the philosophy. 아키텍처를 포크하세요. 철학은 간직하세요.

Every file is open. Every convention is documented. Your vault, your rules — but with a head start.
모든 파일은 공개되어 있습니다. 모든 관행은 문서화되어 있습니다. 당신의 볼트, 당신의 규칙 — 대신 출발선을 훨씬 앞에서.

[Read the full docs전체 문서 읽기](/docs/)
[Download ZIPZIP 다운로드](/files/CMDS-System-Files.zip)
[GitHub ↗](https://github.com/johnfkoo951/cmds-system-files)

![CMDSPACE](/assets/logos/cmds-logo-typo-black.png)
![CMDSPACE](/assets/logos/cmds-logo-typo-white.png)

Command your space.
당신의 공간을 지휘하세요.

© 2026 CMDSPACE · Yohan Koo

[Docs](/docs/)
[GitHub](https://github.com/johnfkoo951/cmds-system-files)
[CMDSPACE Education](https://class.cmdspace.kr/)
