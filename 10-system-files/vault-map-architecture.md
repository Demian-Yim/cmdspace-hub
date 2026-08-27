---
title: vault-map-architecture
source: https://vault-map.cmdspace.work/
author: 구요한 (CMDSPACE)
fetched: 2026-08-28
note: markitdown HTML→MD 자동 변환 스냅샷. 정확한 원문은 source URL 참조.
---

[![CMDS](/assets/logos/cmds-logo-round.png)
Vault Map](/)

[4 Layers](#layers)
[Mothership](#mothership)
[LLM Wiki](#llm-wiki)
[Global](#global)
[Compare](#compare)
[학습 경로](#path)

EN

Vault Map · 2026-05-09 · CMDSPACE
Vault Map · 2026-05-09 · CMDSPACE

# 두 개의 볼트, 하나의 시스템. Two vaults, one system.

메인 볼트(`CMDSPACE_Local_MBP`)와 LLM 위키 위성(`CMDS_LLM_Wiki`)이 글로벌 한 층(`~/.claude/`)을 공유한다. 그 위에 **4가지 추상화 레이어 — Rules · Commands · Skills · Agents** 가 쌓여 있다. 룰 8개, 명령 8+7개, 스킬 62개, 에이전트 6개. 한 페이지에서 전체 지도를 본다.
A mothership vault (`CMDSPACE_Local_MBP`) and an LLM Wiki satellite (`CMDS_LLM_Wiki`) share a global layer (`~/.claude/`). On top of that, **four abstraction layers — Rules · Commands · Skills · Agents** stack up. 8 rules, 8+7 commands, 62 skills, 6 agents — see the whole map on one page.

[4 레이어 보기See the 4 layers](#layers)
[초보자 진입 경로Beginner path](#path)
[System Files](https://system.cmdspace.work)

L4

Agent

페르소나·역할 위임Persona delegation

~6

L3

Skill

반복 패턴 자동화 (자연어 트리거)Reusable automation

62

L2

Command

슬래시 명령 — 워크플로 진입점Slash command entry

8 + 7

L1

Rule

모든 출력의 헌법 — 자동 로드Constitution — auto-loaded

8

핵심 아이디어

The Idea

## 한 단계가 잘 되면 다음 단계로 압축된다 — 정보가 코드로 굳어지는 사다리. When a step works, it compresses into the next — a ladder where information solidifies into code.

한 줄 프롬프트가 잘 되면 → `92. Prompts/{name}.md` 에 저장 (재사용 가능). 패턴이 보이면 → `91. Skills/{name}/SKILL.md` 로 추상화 (트리거 자동 인식). 도메인이 분리되면 → `.claude/agents/{name}.md` 로 페르소나 위임.

**위로 갈수록 강력하고, 아래로 갈수록 안정적**. Rule 만 \*맨 아래\*에서 위 모든 층을 받쳐주는 구조 — 룰은 진화하지 않고 \*규약\*이라서.

A one-line prompt that worked → save to `92. Prompts/{name}.md` (reusable). When a pattern emerges → abstract into `91. Skills/{name}/SKILL.md` (trigger auto-recognized). When a domain becomes its own → delegate to `.claude/agents/{name}.md` (persona).

**Higher = more powerful, lower = more stable**. Only Rules sit at the bottom supporting every layer above — rules don't evolve, they're constitutional.

§ 1 · 4 추상화 레이어4 Abstraction Layers

## 한 페이지로 보는 4 레이어 스택. The 4-layer stack on one page.

볼트에서 AI와 협업하는 방식은 4단계 사다리로 추상화된다. 비유: Rule = 회사 취업규칙, Command = 단축키, Skill = 매뉴얼+도구, Agent = 외주 직원.
Collaboration with AI in a vault is abstracted into a 4-layer ladder. Analogy: Rule = company policy, Command = shortcut, Skill = manual+toolkit, Agent = contractor.

Layer 1

Rule 8

헌법 · Constitution

모든 작업에 **조건 없이 적용되는 제약**. 출력 형식·금지사항. 모든 에이전트가 자동 로드.
Unconditional constraints on every output. Auto-loaded by all agents.

* indentation-rules.md
* frontmatter-standard.md
* wikilink-rules.md
* +5 more

Layer 2

Command 8+7

단축키 · Slash entry

`/명령어` — **고정된 워크플로의 진입점**. 메인 볼트 8개 (CMDS Process Suite) + LLM 위키 7개.
`/command` — fixed workflow entry. 8 in mothership + 7 in LLM Wiki.

* /connect /merge /develop /share
* /inbox /lint /query /status
* + /ingest /reindex (LLM Wiki)

Layer 3

Skill 62

매뉴얼+도구 · Toolkit

**반복 패턴이 트리거가 되는 자동화 단위**. 자연어 트리거가 자동 매칭 — 다 외울 필요 없음.
Reusable automation. Natural-language triggers auto-match — no need to memorize.

* cmds-onboarding · daily-book-update
* tone-writer · thebetter-writer
* +58 more global skills

Layer 4

Agent ~6

외주 직원 · Persona

**특화된 역할/페르소나** — 자체 컨텍스트·도구·판단으로 멀티스텝 작업 수행. 본인이 호출, 다른 에이전트가 호출.
Specialized role/persona — own context, tools, judgment for multi-step work.

* essay-reviewer-korean (vault)
* social-media-content-adapter (vault)
* html-website-builder (global) +3

핵심 인사이트Core Insight

왜 4단계인가 — Compounding 사다리
Why 4 layers — the Compounding ladder

→한 줄 프롬프트 (휘발성)매번 시킴

↓92. Prompts/{name}.md재사용 가능

↓91. Skills/{name}/SKILL.md트리거 자동 인식

↓.claude/agents/{name}.md페르소나 위임

**인사이트Insight**: 위로 갈수록 \*재사용성·자동화 강도\* ↑, 아래로 갈수록 \*불변성·일관성\* ↑. Rule 은 진화하지 않는 헌법.Higher = more reusable & automated; lower = more invariant & consistent. Rule = constitution that doesn't evolve.

§ 2 · 메인 볼트 (Mothership)Mothership Vault

## CMDSPACE\_Local\_MBP — 사람의 1인칭 substrate. CMDSPACE\_Local\_MBP — the human first-person substrate.

10,000+ 노트, 91 카테고리, 3+ 년 누적. **본인 의견·voice·1인칭 작업**이 사는 곳. 4 레이어 모두 살아있음.
10,000+ notes, 91 categories, 3+ years. Where **your opinion · voice · first-person work** lives. All 4 layers active.

### 2.1   Rules — 모든 출력의 헌법 (8개)Rules — Constitution of All Output (8)

위치: `.claude/rules/` · `CLAUDE.md` · `AGENTS.md` 에서 `@import` 로 자동 로드. 세션 시작 시점에 8개가 한꺼번에 컨텍스트에 들어감.
Location: `.claude/rules/` · auto-loaded via `@import` from `CLAUDE.md`/`AGENTS.md`. All 8 enter context at session start.

룰Rule

무엇을 강제Enforces

왜 중요한가Why it matters

indentation-rules

YAML = **2 spaces** / Body = **TAB**YAML = **2 spaces** / Body = **TAB**

YAML 에 탭 들어가면 Obsidian 파서 깨짐. 룰 깨지면 노트가 영구히 망가질 수 있음Tabs in YAML break the Obsidian parser. Violation can permanently corrupt a note.

frontmatter-standard

7 필수 필드 (type, aliases, *description (영문 + double-quote)*, author, date created/modified, tags) + `CMDS:` vs `index:` 방향성7 required fields + `CMDS:` vs `index:` direction

메타데이터 = AI 친화 PKM 의 *진짜 본문*. description 1-2문장 영문이 LLM 의 relevance hintMetadata *is* the real body for AI. The English description is the LLM's relevance hint.

wikilink-rules

3종 결정 트리: `[[wikilink]]` / `@import` / 백틱 코드. 이모지 prefix 정확히3-branch decision: `[[wikilink]]` / `@import` / backtick code; emoji prefixes exact

Wikilink 한 글자 틀리면 빈 노트가 Inbox 에 자동 생성 → 영원한 쓰레기A single-char typo creates an empty note in Inbox — permanent debris.

mermaid-rules

모든 라벨 큰따옴표. `[/` 시작 금지All labels quoted; no `[/` start

Mermaid 파서가 한글·특수문자에 민감. 룰 따르면 다이어그램 100% 렌더Parser is fragile with Korean/specials. Rule = 100% render rate.

blank-line-rules

Obsidian-tight 마크다운 — heading→subheading 사이 빈 줄 XObsidian-tight markdown — no blank between heading→subheading

사용자 시각 선호 + 일관성. AI가 습관적으로 빈 줄 넣는 걸 막음Visual preference + consistency. Stops AI from habitually adding blanks.

file-creation-rules

모든 코드 → `00. Inbox/03. AI Agent/{lane}/`. 파일명 `YYYY-MM-DD-desc.ext`All code → `00. Inbox/03. AI Agent/{lane}/`; filename `YYYY-MM-DD-desc.ext`

8 lane (Claude/OpenClaw/Codex/Antigravity × MBP/Studio) — 어떤 에이전트가 만든 건지 영구 추적8 lanes track which agent on which machine — permanent provenance.

video-project-workflow

영상 프로젝트는 `/DEV/video-projects/`. 볼트엔 추적 MD만Video projects → `/DEV/video-projects/`; only tracking MD in vault

`node_modules` 가 볼트 인덱싱 파괴. 룰 안 지키면 볼트 성능 망`node_modules` destroys vault indexing — performance ruin without this rule.

directory-structure

9 카테고리(100-900) + 폴더(00-90) + symlink 패턴9 categories + folder convention + symlink pattern

새 머신 setup 가이드 — Obsidian Sync 가 dotfile 동기화 안 하므로New-machine setup guide — Obsidian Sync skips dotfiles.

Rule 층의 가치Value of the Rule layer

AI 일관성의 헌법 · 3+년 기술부채 방지 · 에이전트 lock-in 없음Constitution of AI consistency · 3+ years debt prevention · No agent lock-in

**1만개 노트가 같은 모양**: AI 가 만든 노트와 사람이 만든 노트의 구분이 외형적으로 없음AI-made vs human-made notes are visually indistinguishable.

**Claude · Codex · Cursor · Antigravity** 모두 같은 룰 따라서 작업 → 어떤 에이전트로도 교체 가능all follow the same rules → any agent is replaceable.

### 2.2   Commands — CMDS Process 운영 동사 (8개)Commands — CMDS Process Verbs (8)

CMDS Process (Connect → Merge → Develop → Share) 4단계가 **그대로 슬래시 명령**. cross-cutting 4개 추가.
The CMDS Process (Connect → Merge → Develop → Share) becomes **slash commands** directly. Plus 4 cross-cutting utilities.

명령Command

단계 / FanStage / Fan

무엇을 / 언제What / When

/connect

Connect · 1→1

Inbox 항목 → 📖 100 Themes stub. 자동 분류 + 자동 dedupe. **Low friction** — 인박스 빠르게 등록할 때Inbox item → 📖 100 Themes stub. Auto-classify + dedupe. Low-friction quick capture.

/merge

Merge · N→1

N개 노트 → 1개 합성된 📖 200 Literature 노트. Multi-dialog (purpose/candidates/angle/draft). **가장 무거운 명령**N notes → 1 synthesized 📖 200 Literature note. Multi-dialog. The heaviest command.

/develop

Develop · 1→1

방법론 적용·아티팩트 생성 (코드/프롬프트/커리큘럼) → 📖 300-600. 코드는 `00. Inbox/03. AI Agent/` 로Apply methodology, build artifacts (code/prompt/curriculum) → 📖 300-600.

/share

Share · 1→N

기존 합성 → 📖 700-800 (뉴스레터·슬라이드·SNS). **스킬 오케스트레이터** — 직접 콘텐츠 안 씀Existing synthesis → 📖 700-800 (newsletter/slides/SNS). **Skill orchestrator** — never writes directly.

/inbox

Cross-cutting · Router

9개 inbox 하위폴더 스캔 → AskUserQuestion 으로 stage 라우팅. **Read-only**Scans 9 inbox subfolders → routes to a stage command via AskUserQuestion. Read-only.

/lint

Cross-cutting · Health

scope 인자 (inbox/connect/merge/develop/share/all) — orphan/contradiction/stale/frontmatter coverageScope arg — orphans/contradictions/stale/frontmatter coverage.

/query

Cross-cutting · Search+Synth

메인 볼트 + LLM Wiki 동시 검색 → 답변 합성. 값진 답은 해당 CMDS 카테고리에 file-backSearches mothership + LLM Wiki, synthesizes answer; valuable ones file back to a CMDS category.

/status

Cross-cutting · Snapshot

한 화면 요약 — stage 별 노트 수 + 추천 다음 액션. **Zero dialog**. 세션 시작 시 가장 먼저One-screen snapshot — counts per stage + recommended next action. Zero dialog. Run first each session.

Command 층의 인사이트Command layer insight

명령어는 자동화가 아니라 \*사고를 강제하는 비계\*Commands aren't automation — they're cognitive scaffolding

*"이걸 connect 할까, merge 할까?"* 자문하는 순간이 **메타인지의 첫 단**. CMDS Process 가 머릿속 개념이었던 시절보다, 슬래시 명령이 된 이후 어느 단계 일을 하고 있는지가 매번 의식됨.

Asking *"Should I connect or merge this?"* is the **first beat of metacognition**. The CMDS Process used to be a mental model — once it became slash commands, every session forces you to know which stage you're in.

### 2.3   Local Agents — 페르소나 위임 (2개)Local Agents — Persona Delegation (2)

위치: `.claude/agents/` · 볼트-내부 에이전트인 이유: **본인 voice + 한국어 콘텍스트**가 강하게 필요. 글로벌이 아니라 *볼트 안*에 있어야 일관됨.
Location: `.claude/agents/`. These are vault-internal because they require **your voice + Korean context**; consistency demands they live in the vault, not globally.

essay-reviewer-korean

한국어 에세이 리뷰·개선Korean essay review

구조·논리·수사적 효과 분석 + 개선안. *"내 글 봐줘"* 의 정형화 — 매번 같은 검토 기준Structure / logic / rhetoric analysis + suggestions. Standardizes "review my writing".

social-media-content-adapter

SNS 어댑테이션SNS adaptation

임의 텍스트 → Threads · X · LinkedIn · 카카오톡 등 플랫폼별 포스트. 한 본문 → 4-6 플랫폼Arbitrary text → platform-specific posts (Threads/X/LinkedIn/KakaoTalk).

### 2.4   Vault-internal Skills — 거의 없음 (의도)Vault-internal Skills — Near-zero by Design

설계 결정Design decision

재사용 가능한 모든 자동화는 글로벌(`~/.claude/skills/`)에 둔다All reusable automation lives in global (`~/.claude/skills/`)

볼트 내부 `.claude/skills/` 에는 **2개**만 (`api-model-sync`, `write-post`). 대부분 스킬은 글로벌에 위치 → 모든 프로젝트에서 재사용. 볼트 내부 스킬은 *볼트-바운드 작업*만 (예: API 모델 노트 자동 동기화).

Only **2** in the vault's `.claude/skills/`. Everything else is global so every project can reuse it. Vault-internal is reserved for vault-bound work only.

§ 3 · LLM 위키 위성 볼트LLM Wiki Satellite Vault

## CMDS\_LLM\_Wiki — AI 의 3인칭 정리 공장. CMDS\_LLM\_Wiki — AI's third-person curation factory.

Karpathy LLM Wiki 패턴 (Raw Sources → Wiki → Queries) 의 구현. 메인 볼트와 **정반대 — 1인칭 X, AI 합성물 O**.
Implementation of Karpathy's LLM Wiki pattern (Raw Sources → Wiki → Queries). The opposite of the mothership — **no first-person, AI-synthesized only**.

### 3.1   Commands — LLM Wiki Pipeline (7개)Commands — LLM Wiki Pipeline (7)

Command

Role

무엇을What

/ingest

Capture → Process

인박스의 raw 자료 → `10. Raw Sources/` 로 이동(MOVE) + 5–10개 위키 페이지 자동 생성 + cross-link 설치Inbox raw → `10. Raw Sources/` (MOVE) + auto-create 5–10 wiki pages + install cross-links.

/query

Synthesize

Core Context → index → Wiki → Sources 순으로 합성. Substantial 답변은 `30. Queries/` 에 자동 파일링 → **Compounding 엔진**Synthesizes Core Context → index → Wiki → Sources. Substantial answers auto-file to `30. Queries/` — the Compounding engine.

/inbox

Router

인박스 스캔 → 어떤 자료를 ingest 할지 라우팅Scans inbox → routes what to ingest.

/lint

Health check

orphan / broken link / contradiction / stale / inbox-residue / pointer-targetorphan / broken link / contradiction / stale / inbox-residue / pointer-target.

/status

Snapshot

Sources / Wiki / Queries 카운트 + 최근 활동 + top-linked pagesSources / Wiki / Queries counts + recent activity + top-linked pages.

/refresh-context

Rebuild

Core Context 의 pointer 타겟 (BRAIN/HQ/CMDS) 다시 dereferenceRe-dereference Core Context pointer targets (BRAIN/HQ/CMDS).

/reindex

Rebuild

qmd 검색 인덱스 + graph 재생성Rebuild qmd index + graph.

### 3.2   3-Layer Architecture3-Layer Architecture

Layer 1

Raw Sources

10. Raw Sources/

**불변 원본** — 절대 수정 금지. 클리퍼가 가져온 그대로. 카테고리: 11.Articles · 12.Papers · 13.Books · 14.Transcripts · 15.Clippings.**Immutable originals** — never edit. Categories: Articles/Papers/Books/Transcripts/Clippings.

Layer 2

Wiki

20. Wiki/

**LLM 이 관리하는 합성 페이지**. ingest 마다 5–10 개 페이지 신규/업데이트. 모든 주장에 `[[wikilink]]` 인용. concept · entity · guide · map.**LLM-maintained synthesis pages**. 5–10 new/updated per ingest. All claims cite `[[wikilink]]`.

Layer 3

Queries

30. Queries/

**좋은 답변이 다시 페이지로** → 다음 query 의 입력이 됨. *이 피드백이 compounding 의 엔진*.**Substantial answers become pages** → input for next query. *This feedback is the compounding engine.*

의도된 부재Intentional absences

Rules · Skills · Agents 가 없는 이유Why no Rules, Skills, or Agents

**Rules**: 메인 볼트에서 한 번 정의하고 모든 볼트가 공유. *룰은 한 번만 정의한다*는 원칙defined once in mothership, shared across vaults — the "define rules once" principle.

**Skills · Agents**: 7개 명령어로 충분히 self-contained. 워크플로우 자체가 명령어에 담겨 있음.7 commands are enough — the workflow lives in the commands themselves.

→ 반대로 메인 볼트는 4 레이어 모두 살아있음. **작업 다양성이 다르기 때문**.→ The mothership has all 4 layers because work diversity is different.

§ 4 · 글로벌 도구상자Global Toolkit

## `~/.claude/` — 두 볼트가 공유하는 도구상자. `~/.claude/` — the toolkit both vaults share.

두 볼트 어디서 작업해도 동일하게 호출 가능. **재사용 가능한 모든 자동화가 여기**. **4 agents · 62 skills**.
Callable from either vault. **All reusable automation lives here**: 4 agents · 62 skills.

### 4.1   Global Agents (4개)Global Agents (4)

html-website-builder

HTML 사이트 신규 제작New HTML site builder

개념 → 컴포넌트 → 페이지 생성. 이 사이트도 cmdspace-web-builder 스킬과 연계해 만들어짐Concept → components → pages. (This site uses the cmdspace-web-builder skill.)

presentation-english-coach

한 → 영 발표 코칭KO → EN presentation coaching

한국어 자료 → 영어 발표 스크립트 + delivery 코칭Korean material → English presentation script + delivery coaching.

presentation-generator-ko

한국어 프레젠테이션Korean presentation

한국어로 프레젠테이션 자동 구성·구조화·스피커 노트Auto-structures Korean presentations with speaker notes.

raycast-script-generator

Raycast bash 스크립트Raycast bash scripts

Raycast 메타데이터 + bash 스크립트 동시 생성. 클립보드/URL/파일 자동화Raycast metadata + bash for clipboard/URL/file automation.

### 4.2   62 Skills · 8 카테고리62 Skills · 8 Categories

🟢 클릭하면 카테고리 안의 스킬 목록이 펼쳐집니다. *다 외울 필요 없음* — 자연어 트리거가 자동 매칭.
🟢 Click a card to expand. *No need to memorize* — natural-language triggers auto-match.

A

CMDS 시스템 운영CMDS System Ops ⭐8

코호트 1주차 학생에게 가장 먼저 노출First-touch skills for new cohort students

* `cmdspace-web-builder` v4.3 표준 사이트 즉시 제작v4.3 standard site builder
* `cmdspace-update` cmdspace.work 랜딩 동기화·배포cmdspace.work apex sync
* `system-docs-updater` 8 시스템 파일 4-way 동기화4-way system files sync
* `cmds-doc-formatter` CMDS 컴플라이언트 마크다운CMDS-compliant markdown
* `cmds-canvas` MOC · Meeting · Weekly CanvasMOC / Meeting / Weekly canvases
* `cmds-sns-promo` 4 SNS 동시 어댑테이션 (KO/EN)4-platform SNS adaptation (KO/EN)
* `cmds-format` CMDS 노트 포맷팅 전문가CMDS note formatting specialist
* `web-deployments-sync` Vercel 프로젝트 인덱스 갱신Vercel project index sync

목록 보기Show skills

B

콘텐츠 제작Content Production6

더배러 · 강의 · SNS 본인 voice 학습형더배러 newsletter · lectures · SNS — voice-aware

* `thebetter-writer` 더배러 voice 로 에세이Essays in 더배러 voice
* `tone-writer` 진지·통찰·유머 3톤 변주3-tone variation
* `series-writer` 다편 시리즈 + 통합편 합성Multi-part series + integration
* `write-post` DEVLOG → AI 사례 게시글DEVLOG → AI case post
* `interactive-writing-assistant` 아이디어 → 수정 인터랙티브Idea → revision interactive
* `terminology-researcher` CMDS 학술 용어 노트 (한/영)CMDS academic terminology (KO/EN)

목록 보기Show skills

C

문서·포맷팅Docs & Formatting10

Obsidian · 마크다운 · CanvasObsidian · markdown · canvas

* `markdown-formatter` 비정형 → Obsidian 마크다운Unstructured → Obsidian MD
* `obsidian-markdown` wikilink/embed/callout/properties
* `obsidian-markdown-structure` 프론트매터·헤딩 구조 검증Frontmatter/heading validation
* `obsidian-yaml-frontmatter` YAML 일관성YAML consistency
* `obsidian-links` 위키링크 검증 + 깨진 링크 수정Wiki-link validation + repair
* `obsidian-mermaid` Obsidian 호환 MermaidObsidian-compatible Mermaid
* `obsidian-bases` .base 파일 (뷰·필터·수식)
* `obsidian-canvas` Canvas 자동 레이아웃Auto layout for canvases
* `json-canvas` .canvas 노드/엣지 직접 편집
* `obsidian-cli` Obsidian CLI v1.12+

목록 보기Show skills

D

프레젠테이션·문서 출력Presentations & Docs5

슬라이드 · PPTX · Keynote · PDF · 비즈니스 문서Slides · PPTX · Keynote · PDF · biz docs

* `markdown-slides` Deckset/Marp 슬라이드
* `pptx-cmds` PowerPoint .pptx 생성·편집
* `keynote` macOS Keynote 네이티브 (JXA)
* `md-to-pdf` 전문 스타일 PDF (HTML+Chrome)Pro PDF (HTML + headless Chrome)
* `business-docs` 한글 인보이스·제안서·계약서KR invoices · proposals · contracts

목록 보기Show skills

E

멀티미디어Multimedia8

오디오·이미지·비디오·OCRAudio · image · video · OCR

* `audio-transcriber` Whisper/ElevenLabs STT → CMDS 노트
* `audio-generator` ElevenLabs TTS (배치)
* `image-generation-skill` 슬라이드·문서용 AI 이미지AI images for slides/docs
* `video-cleaning` Whisper+FFmpeg 침묵·필러 제거Whisper+FFmpeg silence/filler removal
* `markdown-video` Deckset MD + TTS → 발표 영상Deckset MD + TTS → presentation video
* `heygen` HeyGen AI 아바타 v2 API
* `youtube-kr-subtitle` 유튜브 한글 자막 burn-inYouTube → KR subtitles burn-in
* `deepseek-ocr` DeepSeek-OCR + MLX
* `notebooklm-logo-remover` NotebookLM 워터마크 제거NotebookLM watermark removal

목록 보기Show skills

F

자동화·도구Automation Tools10

파일 정리·Raycast·태그·웹·훅File org · Raycast · tags · web · hooks

* `file-organizer` 폴더 → 토픽 기반 정리Folder → topic-based organization
* `downloads-organizer` Downloads 정리·중복 제거Downloads cleanup + dedupe
* `raycast-script-command` Raycast bash 스크립트 생성
* `macos-file-tags` Finder 색상 태그 관리
* `defuddle` 웹페이지 → 깔끔 마크다운Web → clean markdown
* `plaud-cloud-tools` Plaud Cloud · 전사·요약
* `gemini-with-claudecode` Claude Code 안에서 Gemini 호출Call Gemini from Claude Code
* `hook-creator` Claude Code 훅 생성
* `skill-creator` 스킬을 만드는 스킬 (재귀)Skill that creates skills
* `meeting-minutes` 한국어 비즈니스 회의록KR business meeting minutes

목록 보기Show skills

G

옵시디언 플러그인·웹Plugins & Web5

플러그인 0→1, 매거진 사이트, DocusaurusPlugin 0→1, magazine site, Docusaurus

* `obsidian-plugin-builder` 옵시디언 플러그인 0→1Obsidian plugin 0→1
* `obsidian-plugin-dev` 버전업·테스트·릴리즈Version/test/release
* `obsidian-magazine-site` 노트 묶음 → 매거진/위키Notes → magazine/wiki site
* `obsidian-docusaurus-builder` 옵시디언 → Docusaurus v3Obsidian → Docusaurus v3
* `minimal-homepage` 단일 HTML 가벼운 홈페이지Single-HTML lightweight homepage

목록 보기Show skills

H

인프라·전문가 도구Infra & Expert Tools10

Vercel · DNS · 그래프 · Naval brainVercel · DNS · graph · Naval brain

* `vercel-deployer` 정적 사이트 Vercel 자동 배포Static site auto-deploy to Vercel
* `vercel-react-best-practices` TSX React 베스트 프랙티스TSX React best practices
* `domain-routing` Cloudflare DNS + Vercel 도메인Cloudflare DNS + Vercel domain
* `web-design-guidelines` UI 코드 컴플라이언스 리뷰UI compliance review
* `remotion-best-practices` Remotion (React video)
* `course-designer` 교육 자료 → 과정·모듈 설계Education → curriculum design
* `graphify` 임의 입력 → 지식 그래프Any input → knowledge graph
* `omc-reference` OMC 에이전트 카탈로그
* `ai4pkm-helper` AI4PKM 온보딩 가이드AI4PKM onboarding guide
* `vibe-study-application` 바이브코딩 스터디 지원서Vibe-coding study application
* `naval` Naval brain 의사결정 컨설팅Naval brain decision consulting

목록 보기Show skills

왜 62개인가Why 62

62개는 과잉이 아니라 누적 — \*3번 이상 반복된 작업\*만 스킬화62 isn't excess — it's accumulation. A skill is created only when a task repeats 3+ times.

**대부분 한 줄 트리거Most are one-line triggers**: "Raycast 스크립트 만들어줘" / "오디오 전사해줘" — *다 외울 필요 없음, AI가 매칭*"Make a Raycast script" / "Transcribe this audio" — no memorization needed, AI matches.

**재귀 시스템Recursive system**: `skill-creator` 가 새 스킬 만들고, `hook-creator` 가 훅 만듦 — 시스템 자체가 시스템을 확장creates new skills; `hook-creator` creates hooks — the system extends itself.

**Compounding 의 정점Peak of Compounding**: 본인 도메인의 한 줄 프롬프트가 → SKILL.md 가 → 다른 사람도 재사용 가능한 자산으로A one-line prompt in your domain becomes a SKILL.md, then a reusable asset for others.

§ 5 · 두 볼트 비교Two Vaults Compared  ⭐

## 같은 패턴, 다른 목적. Same pattern, different purpose.

이 비교가 **전체 시스템의 인사이트**. 같은 4 레이어 패턴이 *다른 콘텐츠 철학* 위에 올라간다.
This comparison is **the system's central insight**. The same 4-layer pattern rides on *opposite content philosophies*.

글로벌GLOBAL

~/.claude/

차원Dimension

Mothership

CMDSPACE\_Local\_MBP

LLM Wiki

CMDS\_LLM\_Wiki

주저자Author

**사람 (구요한)Human (구요한)**

**LLM (사람은 큐레이터)LLM (human curates)**

콘텐츠 철학Content philosophy

*내 의견·내 voice* — 적게 쓰더라도 1인칭*My opinion · my voice* — first-person, even if sparse

*외부 자료의 정리* — 많이 ingest 하더라도 3인칭*External material curation* — third-person, even if voluminous

Process

**Connect → Merge → Develop → Share**

**Ingest → Query (Compounding)**

명령 수# commands

**8** · CMDS Process Suite

**7** · LLM Wiki Pipeline

Rules

**8** · 모든 볼트의 헌법constitution for all vaults

없음 · 메인 룰 importnone · imports mothership rules

Skills

거의 0 (모든 게 글로벌에)~0 (all in global)

0 (명령어로 충분)0 (commands suffice)

Agents

**2** · essay-reviewer · social-adapter

0

검색 도구Search

qmd (lex/vec/hyde) + grep + Obsidian

동일 (LLM 위키 인덱스만)same (LLM Wiki index only)

공유 모드Sharing

비공개 (구요한 본인)private (구요한 only)

공개 가능 (교양 위키화)shareable (publishable wiki)

수명Lifespan

영구 (3+년 누적, 10,000+)permanent (3+ yrs, 10,000+)

무제한 ingest, 단 쿼리 응답 위주unlimited ingest, query-response focused

Graduation 신호Graduation signal

(해당 없음 — mothership)(N/A — mothership)

100+ sources / Grep 한계 / Web Clipper inbox 일 5+100+ sources / Grep limit / Clipper inbox 5+/day

부트캠프 §2.2 의 3 reasonsBootcamp §2.2 — 3 reasons

왜 두 볼트로 분리했나 — boundary · design · contaminationWhy split into two vaults — boundary · design · contamination

**1. AI 검색 boundary**: 메인 볼트 query 가 LLM Wiki 페이지로 오염되지 않게 — 환각 방지 + 보안·권한 분리Mothership queries don't get polluted by LLM Wiki pages — prevents hallucinations, separates security/access.

**2. 설계 원칙의 근본적 차이Fundamentally different design**: 인간 작업 흐름 (Connect/Merge/Develop/Share) vs AI 데이터 처리 흐름 (Ingest/Query) — 폴더 구조가 다름Human workflow (Connect/Merge/Develop/Share) vs AI data flow (Ingest/Query) — folder structures differ.

**3. 작성 주체의 물리적 분리Physical separation of authorship**: 인간 오리지널 vs AI 가공물 → *지식 오염 방지*Human originals vs AI processed → *prevents knowledge contamination*.

→ 이 3가지는 *운영해본 사람에게는 자명* 하지만, 처음 보는 사람에게는 추상적. 그래서 코호트 학생들에게는 **인라인 (in-vault) 옵션** 도 함께 제공.→ Obvious to those who've operated it; abstract to newcomers — so cohort students also get an **in-vault inline option**.

§ 6 · 학습 진입 경로Learning Path

## 초보부터 시스템 디자이너까지. From beginner to system designer.

학생은 *남이 쌓아둔 사다리* 위에서 시작하고, 본인 도메인이 두꺼워질수록 *자기 사다리*를 추가한다.
Start on someone else's ladder. As your domain thickens, add your own rungs.

1주차 학생Week 1 student

5개만 — 남이 쌓아둔 사다리에 올라가기Just 5 — climb the existing ladder

* **CLAUDE.md** 가 자동 로드된다는 것 (8 룰 포함)auto-loads (with 8 rules)
* `/status` — 매번 세션 시작 시 한 화면 요약one-screen snapshot at session start
* `/connect` — 인박스 정리의 첫 단first rung of inbox processing
* `cmds-onboarding` — 본인 컨텍스트로 채우기fill the vault with your context
* `daily-book-update` — 책 아웃라인 캔버스 (W2 Living Book)book outline canvas (W2 Living Book)

→ 이 5개로 **Compounding 사다리의 1단** (남이 만든 프롬프트 사용) 시작.→ These 5 launch **Compounding rung 1** (using others' prompts).

한 달 후 (3–4주차)After one month

루틴화 + 본인 프롬프트 저장Routinize + save your own prompts

* `/inbox` → `/connect` 또는or `/merge` 일상 루틴화becomes daily routine
* 본인 프롬프트 1–3개를save 1–3 of your own prompts to `92. Prompts/Distill/`에 저장 (Compounding 2단) (Compounding rung 2)
* 글로벌 스킬 5개 정도 외움memorize ~5 global skills: `tone-writer`, `markdown-slides`, `audio-transcriber`, `defuddle`, `markdown-formatter`
* (선택) LLM Wiki 인라인 시도 — 메인 볼트 안에서 `LLMWiki/` 폴더로(optional) try LLM Wiki inline — `LLMWiki/` folder inside mothership

6개월 후 (graduation)After 6 months (graduation)

자기 스킬 + standalone LLM Wiki + 본인 변형Own skills + standalone LLM Wiki + your variant

* 본인 도메인 스킬 1–3개를 `91. Skills/community/` 에 작성 (cmds-vault PR)write 1–3 domain skills into `91. Skills/community/` (cmds-vault PR)
* LLM Wiki standalone 분리 — `cmds-llm-wiki v1.3.0` 클론 + `mv` 한 번graduate LLM Wiki to standalone — clone `cmds-llm-wiki v1.3.0` + one `mv`
* 본인 cmds-vault 변형 (안 쓰는 카테고리 제거 / 본인 도메인 추가)fork cmds-vault (drop unused categories / add yours)
* `/share` 로 외부 산출물 자동화 (뉴스레터·슬라이드·SNS)automates external outputs
* 본인 에이전트 페르소나 1개 추가 (`.claude/agents/`)add your first agent persona

시스템 디자이너System designer

시스템을 \*바꾸는\* 사람The one who changes the system

* 룰 자체를 수정 (`.claude/rules/`) — 비로소 *시스템 디자이너*edit the rules themselves — finally a *system designer*
* 새 명령 추가 (`.claude/commands/`) — 본인 워크플로 슬래시 명령화add new commands — slash-command your workflow
* `skill-creator` · `hook-creator` 로 *스킬을 만드는 스킬 · 훅을 만드는 훅*to create skills/hooks recursively
* 다른 볼트로 governance 분리 (Pair · Team · Public)split into Pair / Team / Public vaults

§ 7 · 가치Value

## 왜 이렇게까지 했는가. Why go this far.

1

AI 시대 지식 작업 재설계Redesigning knowledge work

한 사람이 *연구하고 가르치는* 도메인 (PKM × LLM × Multi-Agent)을, **직접 살아내는 시스템**으로. 4 focus axes: Obsidian PKM · System Files · LLM Wiki · 9Yohan Multi-Agent.A live experiment in researching-while-teaching the LLM era of PKM. Four focus axes operated daily on this substrate.

2

재사용 가능한 사다리Reusable ladder

룰 8 = 헌법 · 명령 8 = 인지 비계 · 스킬 62 = 도구상자 · 에이전트 6 = 페르소나. 새 학생도 **0에서 시작 안 함** — 클론 한 번이면 3+년 누적의 사다리.8 rules = constitution · 8 commands = cognitive scaffolding · 62 skills = toolkit · 6 agents = personas. New students don't start at zero.

3

Compounding 의 실증Proof of Compounding

매번 시키기 vs 한 번 코드화 — 6개월 차이가 **복리로 벌어짐**. 코호트의 핵심 메시지 *"시키기 → 쌓기"* 가 본 시스템 그 자체.Re-asking vs code-once — 6 months compounds dramatically. The cohort's central message *"Ask → Stack"* *is* this system.

4

볼트 분리의 의미Meaning of vault separation

단순 폴더 분리가 아니라 **인간 vs AI 작업의 governance 분리**. 7개 companion vault 까지 확장하면 7개 governance 모델 — 솔로/Pair/Team/Public.Not just folder partition — **governance separation between human and AI work**. With 6 companion vaults, 7 distinct governance models in one ecosystem.

§ 8 · 한 화면 요약One-screen summary

## 덮어두기 좋은 요약 카드. A summary card to keep open.

8

Rules

헌법 · 자동 로드constitution

8+7

Commands

메인 + LLM 위키mothership + LLM Wiki

62

Skills

8 카테고리8 categories

~6

Agents

vault 2 + global 4vault 2 + global 4

Mothership ↔ LLM Wiki

두 볼트가 글로벌을 공유하면서 각자의 governance·voice·콘텐츠 철학을 유지한다Two vaults share the global layer while preserving their own governance, voice, and content philosophy

**Mothership** · `CMDSPACE_Local_MBP` · 사람 (1인칭) · Connect→Merge→Develop→ShareHuman (1st person) · Connect→Merge→Develop→Share

**LLM Wiki** · `CMDS_LLM_Wiki` · LLM (3인칭) · Ingest→Query (Compounding)LLM (3rd person) · Ingest→Query (Compounding)

![CMDS](/assets/logos/cmds-logo-round.png)
Vault Map

구요한의 볼트 시스템 — 4 레이어 × 2 볼트. 코호트 1주차 ~ 시스템 디자이너까지.
구요한's vault system — 4 layers × 2 vaults. From beginner to system designer.

#### 시스템 파일System Files

* [system.cmdspace.work](https://system.cmdspace.work)
* [/docs · 5 system files](https://system.cmdspace.work/docs/)
* [GitHub · cmds-system-files](https://github.com/johnfkoo951/cmds-system-files)

#### 레포지토리Repos

* [cmds-vault (mothership starter)](https://github.com/johnfkoo951/cmds-vault)
* [cmds-llm-wiki (standalone)](https://github.com/johnfkoo951/cmds-llm-wiki)
* [Karpathy LLM Wiki gist](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)

#### 관련 사이트Related sites

* [cmdspace.work · apex](https://cmdspace.work)
* [cohort.cmdspace.work](https://cohort.cmdspace.work)
* [9yohan.cmdspace.work](https://9yohan.cmdspace.work)
* [llm-wiki.cmdspace.work](https://llm-wiki.cmdspace.work)

vault-map.cmdspace.work · 2026-05-09

© CMDSPACE · 구요한© CMDSPACE · 구요한
