---
title: llm-wiki-showcase
source: https://llm-wiki.cmdspace.work/
author: 구요한 (CMDSPACE)
fetched: 2026-08-28
note: markitdown HTML→MD 자동 변환 스냅샷. 정확한 원문은 source URL 참조.
---

[![CMDS](/assets/logos/cmds-logo-round.png)
CMDS LLM Wiki
v2.7](/)

[아키텍처Architecture](#architecture)
[마더십 ↔ 위성Mothership ↔ Satellite](#mothership)
[운영Operations](#operations)
[v2.7 신규v2.7 New](#v2-1)
[v1.11.0 릴리즈v1.11.0 Release](https://github.com/johnfkoo951/cmds-llm-wiki/releases/latest)
[문서Docs](/docs/)
[구요한Bio](/bio)
[마더십 →
Mothership →](https://system.cmdspace.work)

EN

CMDS LLM Wiki · v2.8 · 템플릿 v1.11.0 (2026-08-17)
CMDS LLM Wiki · v2.8 · Template v1.11.0 (2026-08-17)

# 사람과 AI 가 함께 컴파일하는 위키. A wiki that humans and AI compile together.

외부 자료를 LLM 이 읽고 영구 위키로 컴파일하는 **위성 볼트(satellite vault)**. [마더십 (CMDSPACE)](https://system.cmdspace.work) 옆에 짝으로 배치되어, 매번 RAG 로 재검색하지 않고 한 번 컴파일된 지식이 계속 성장합니다.
A **satellite vault** where LLM ingests external sources and compiles them into a persistent wiki. Sits paired with the [mothership (CMDSPACE)](https://system.cmdspace.work) — knowledge accumulates instead of being re-fetched each query.

[아키텍처 문서
Architecture docs
→](/docs/)
[v1.11.0 다운로드
Download v1.11.0](https://github.com/johnfkoo951/cmds-llm-wiki/releases/latest)
[마더십 시스템 파일
Mothership system files](https://system.cmdspace.work)
[GitHub](https://github.com/johnfkoo951/cmds-llm-wiki)

1417

마크다운 파일Markdown files

754

위키 페이지Wiki pages

248

Raw SourcesRaw Sources

3-Layer

아키텍처Architecture

3-Layer 아키텍처3-Layer Architecture

## 소스코드 · 실행파일 · 스키마 Source · Runtime · Schema

Karpathy 가 2026-04-06 에 제안한 LLM Wiki 패턴의 직접 구현. **Raw Sources** 는 불변 소스코드, **Wiki** 는 LLM 이 컴파일한 실행파일, **Schema** 는 컴파일러를 정의하는 메타 룰입니다.
Direct implementation of Karpathy's LLM Wiki pattern (2026-04-06). **Raw Sources** are immutable source code, **Wiki** is the LLM-compiled runtime, **Schema** is the meta-rule defining the compiler.

10. Raw Sources

IMMUTABLE · 248 sources

* 📄 Articles
* 📑 Papers
* 📚 Books
* 🎙 Transcripts
* 🌐 Clippings

Compiler

/ingest · Claude Code

LLM 이 읽고 · 추출하고 · 위키화LLM reads, extracts, wikifies

20. Wiki

754 pages · growing

* Concepts
* Entities
* Guides
* Maps

세 계층을 관장하고 · 질의된다governs & is queried by all three

CLAUDE.md — Schema Layer

하네스the harness

* · Folder conventions
* · Frontmatter standards
* · Ingest / Query / Lint specs
* · Wiki page anatomy

"Schema is the harness"

**핵심 통찰**: 매번 LLM 이 RAG 로 재검색하지 않습니다. 한 번 컴파일된 위키가 다음 ingest 의 컨텍스트가 되고, 지식이 *compounding artifact* 로 누적됩니다.
**Key insight**: LLM doesn't re-fetch via RAG every time. Once compiled, the wiki becomes context for the next ingest — knowledge accumulates as a *compounding artifact*.

마더십 ↔ 위성 구조Mothership ↔ Satellite

## 두 볼트, 두 다른 합의 모델. Two vaults, two consensus models.

마더십과 위성은 같은 사용자의 두 볼트지만 **주저자(primary author)** 가 다릅니다. 마더십은 사람이 쓴 노트, 위성은 LLM 이 컴파일한 위키. [kepano](https://github.com/kepano) 의 contamination mitigation 원칙: 둘을 섞지 않습니다.
Mothership and satellite are two vaults of the same user but have different **primary authors**. Mothership = human-authored notes, satellite = LLM-compiled wiki. Per kepano's contamination mitigation principle: don't mix them.

🌍 CMDSPACE\_Local\_MBP — Mothership

Solo · 사람 primary authorSolo · human primary author

* 9 system files (CLAUDE / AGENTS / ANTIGRAVITY / CMDS / Guide / HQ / BRAIN / BRAIN\_PROMPT / DESIGN)
* 9 categories (100–900) · 10K+ notes
* CMDS Process: Connect → Merge → Develop → Share

reference (snapshot) · satellite branches

Core Context.md

모선 스냅샷mothership snapshot

모선 9 시스템 파일의 스냅샷 · 30일마다 refreshSnapshot of mothership's 9 system files · refresh every 30d

🛰 LLM Wiki

이 볼트 · Solo + LLMthis vault · Solo + LLM

Karpathy 패턴 컴파일 · 1417 .md · 754 wikiCompiled Karpathy pattern · 1417 .md · 754 wiki

Other vaults

companion

JoonLab · Admin · Gobi · cmds-vault

### 시스템 파일 매핑 System Files Mapping

| 계층Layer | 마더십 (9 files)Mothership (9 files) | 위성 (6 files)Satellite (6 files) | 관계Relationship |
| --- | --- | --- | --- |
| 기술 규칙Tech rules | `CLAUDE.md` · `AGENTS.md` · `ANTIGRAVITY.md` | `CLAUDE.md` (Schema) · `AGENTS.md` | 위성 = 마더십 simplified + 3-Layer 추가Satellite = mothership simplified + 3-Layer |
| 컨텍스트Context | `CMDS.md` · `🏛 Guide` · `🏛 HQ` | `Core Context.md` | 위성 의 Core Context = 마더십 9 file 의 snapshot (30일 refresh)Satellite Core Context = snapshot of mothership 9 files (30-day refresh) |
| 시각 언어Visual | `DESIGN.md` (2026-05-22 신설, precedence 9) | — | v4.3 디자인 상수 · Anti-AI-Slop · 87-skill ↔ surface 매핑. 위성에서는 별도 시각 자산이 없어 미반영.v4.3 design constants · Anti-AI-Slop · 87-skill ↔ surface mapping. Satellite has no separate visual assets — not mirrored. |
| 페르소나Persona | `BRAIN.md` · `BRAIN_PROMPT.md` | — | Gobi 앱 entry — LLM coding agent 의 always-load 대상은 아님.Gobi app entry — not an always-load target for LLM coding agents. |
| 진입점Entry point | `🛰 CMDS_LLM_Wiki Satellite Vault.md` | `index.md` · `LLM-Wiki-Starter-Kit.md` | 서로의 위치 가리킴 (cross-vault link)Each points to the other (cross-vault link) |
| 로그Log | — | `log.md` | 위성만 — ingest/query 활동 추적Satellite only — tracks ingest/query activity |

**Cross-vault wikilink 불가**: Obsidian 위키링크는 볼트 경계를 넘지 못함. 서로 참조 시 `obsidian://open?vault=...&file=...` URL 사용. 단, **qmd MCP 검색** 은 user-scope 등록되어 어느 볼트에서든 양쪽 모두 검색 가능.
**No cross-vault wikilinks**: Obsidian wikilinks can't cross vault boundaries. Reference each other via `obsidian://open?vault=...&file=...` URLs. However, **qmd MCP search** is user-scoped and can search both vaults from either side.

3 운영 작업3 Operations

## Ingest · Query · Lint 위키의 호흡. Ingest · Query · Lint The wiki's breath.

위키는 살아있는 시스템 — 들숨(Ingest)으로 raw source 를 흡수, 날숨(Query)으로 종합된 답변 생성, 위생점검(Lint)으로 일관성 유지. 마더십의 CMDS Process (Connect→Merge→Develop→Share) 와 다른 vocabulary 지만 보완적입니다.
The wiki is a living system — Ingest absorbs raw sources, Query produces synthesized answers, Lint maintains consistency. Different vocabulary from the mothership's CMDS Process (Connect→Merge→Develop→Share) but complementary.

📥

/ingest

Slash command · raw → wiki

외부 자료 (article · paper · book · transcript) 를 수집해 `10. Raw Sources/` 에 저장 후 LLM 이 추출한 개념·엔티티를 `20. Wiki/` 에 컴파일. 수집 목적 (`collectionPurpose`) 1회 질문 후 진행.
Collects external sources (article/paper/book/transcript) into `10. Raw Sources/`, then LLM extracts concepts/entities and compiles to `20. Wiki/`. Asks purpose once, then proceeds.

🔎

/query

Slash command · wiki → answer

qmd MCP (BM25 + Vector + HyDE) 로 위키와 raw sources 검색 후 답변 합성. wiki-worthy 면 `30. Queries/` 에 file-back. 마더십 볼트도 함께 검색 가능 (cross-vault).
Searches wiki + raw sources via qmd MCP (BM25 + Vector + HyDE), synthesizes answer. Wiki-worthy queries get filed back to `30. Queries/`. Cross-vault search to mothership available.

🧹

/lint

Slash command · health check

Read-only 위생 점검 — orphan / contradiction / stale / frontmatter 일관성. Living Reference Policy 위반 (Core Context 30일 경과) 도 flag. 자동 수정 안 함, 사용자 결정 대기.
Read-only health check — orphan / contradiction / stale / frontmatter coverage. Flags Living Reference Policy violations (Core Context 30+ days old). No auto-fix, waits for user decision.

v2.8 · 템플릿 v1.11.0 (2026-08-17)v2.8 · Template v1.11.0 (2026-08-17)

## 품질 게이트 + 듀얼 harness. Quality gates + dual harness.

초기 위키는 "외부 자료 → 위키 컴파일" 의 단방향이었습니다. 운영하며 메운 품질 게이트 4종에 더해, v1.5~v1.6 에서 **Claude Code + Codex 듀얼 harness** 와 대화형 `/onboard` 셋업이 합류했습니다. 같은 operation 을 두 에이전트에서 1:1 로 실행합니다.
The early wiki was one-way: external source → wiki compilation. On top of four quality gates added through operation, v1.5–v1.6 brought the **Claude Code + Codex dual harness** and an interactive `/onboard` setup. The same operations run 1:1 across both agents.

🔓

Exploration Gate (v4)Exploration Gate (v4)

explored: false | true

새 위키 페이지는 모두 `explored: false` 로 시작. 사람이 직접 읽거나 에이전트가 source-backed 검증을 끝낸 뒤에만 `explored: true`. `confidence: high` 페이지는 반대해석 + 데이터 공백 1줄 기록 (Bias Check). `/lint` 가 unexplored backlog 보고.
Every new wiki page starts with `explored: false`. Promoted to `true` only after human read or agent source-backed verification. `confidence: high` requires a counter-argument + data gap note (Bias Check). `/lint` reports unexplored backlog.

📚

Book Ingest (Progressive Stubs)Book Ingest (Progressive Stubs)

bookIndex · chapterNumber

5+ 챕터 책·문서 사이트 (mdBook · VitePress · GitBook · Docusaurus · ReadTheDocs) 는 한 번에 ingest 하지 않음. 1 Book Index + N chapter stubs (`status: stub`) + 소수 anchor wiki. 사용자가 챕터를 읽으면 해당 stub 을 promote (verbatim + wiki 컴파일 + `status: completed`).
5+ chapter books/doc sites (mdBook, VitePress, GitBook, Docusaurus, ReadTheDocs) aren't ingested in one shot. Create 1 Book Index + N stubs (`status: stub`) + few anchor wiki pages. When user reads a chapter, the matching stub is "promoted" — verbatim insertion + wiki compile + `status: completed`.

📦

70. Outputs/ 격리70. Outputs/ Isolation

{tool}/{YYYY-MM-DD}-{topic}/

외부 도구 (graphify · markdown-formatter) 산출물은 위키 본체 (10/20/30) 와 격리. 라이프사이클이 다름 — wiki 는 \*컴파일 결과물\*, outputs 는 \*분석 결과\*. 한 실행 = 한 dated 폴더, 인사이트는 `30. Queries/` 로 정제 후 위키 흡수.
External tool products (graphify, markdown-formatter) live outside the wiki body (10/20/30). Different lifecycle — wiki is \*compiled knowledge\*, outputs are \*analysis artifacts\*. One run = one dated folder; insights get refined into `30. Queries/` before joining the wiki.

🈂️

CJK 인명 표기CJK Person Naming

native script + aliases

한·중·일인 entity 파일명은 네이티브 스크립트만 (`홍길동.md`, `张汉东.md`). 영문 표기는 transliteration 이지 고유 이름이 아니므로 `aliases` 에 둠. Obsidian graph/검색은 aliases 도 인식 — 접근성 손실 없음.
Korean/Chinese/Japanese person entity filenames use native script only (`홍길동.md`, `张汉东.md`). English transliteration goes in `aliases` — it's not a unique name. Obsidian graph/search resolves aliases — no accessibility loss.

🔀

Claude + Codex 듀얼 harnessClaude + Codex dual harness

.claude/ ↔ .codex/ ↔ .agents/skills/

v1.6.0 부터 같은 operation 이 3면에 미러됨 — `.claude/commands/` (11) · `.codex/commands/` (10) · `.agents/skills/` (10) + `AGENTS.md` schema. Claude Code 와 Codex (Cursor·Windsurf 포함) 가 동일 harness 를 공유. 11 commands: ingest·query·lint·inbox·status·reindex·refresh-context·onboard·capture-tabs·verify·audit.
Since v1.6.0 every operation mirrors across 3 surfaces — `.claude/commands/` (11) · `.codex/commands/` (10) · `.agents/skills/` (10) + the `AGENTS.md` schema. Claude Code and Codex (incl. Cursor/Windsurf) share one harness. 11 commands: ingest, query, lint, inbox, status, reindex, refresh-context, onboard, capture-tabs, verify, audit.

🎬

/onboard 인터뷰 셋업/onboard interview setup

v1.5.0 · first-run

"온보딩해줘" 한 마디로 필수 5문항(위치·이름·Mode A/B·모선 경로·정체성·재활용 축)을 물어 placeholder 일괄 치환 + Core Context 작성 + `status: active` 까지 자동. 수동 sed 셋업(`Setup Guide.md`)도 그대로 병행 지원.
One "onboard me" runs a 5-question interview (path, name, Mode A/B, mothership path, identity, reuse axes) → bulk placeholder substitution + Core Context authoring + `status: active`. The manual `sed` path (`Setup Guide.md`) still works in parallel.

### Living Reference Policy Living Reference Policy

마더십의 9 시스템 파일은 위성과 독립적으로 진화합니다. 위성의 `Core Context.md` 는 그 진화의 **snapshot** 일 뿐 — 30일 이상 오래되면 `/lint` 가 flag 하고, `/refresh-context` 가 재snapshot 합니다. 절대 마더십 원본을 위성에 복사하지 않습니다.
The mothership's 9 system files evolve independently of the satellite. The satellite's `Core Context.md` is just a **snapshot** of that evolution — older than 30 days and `/lint` flags it; `/refresh-context` re-snapshots. The original is never copied into the satellite.

최근 trigger: 2026-08-17 Persona 레이어 (v1.11.0) — 26. Personas 실존 인물 perspective-taking 층 + /ingest 자동 누적 + Simulation Boundary 반날조 장치. 직전: 2026-07-23 논문 파이프라인 완결 — Paper Ingest Mode 12단 분석 (v1.10.0).
Latest trigger: 2026-08-17 Persona Layer (v1.11.0) — 26. Personas perspective-taking tier for real people + /ingest auto-accumulation + Simulation Boundary anti-fabrication guard. Previous: 2026-07-23 full paper pipeline — Paper Ingest Mode 12-step analysis (v1.10.0).

### 최신 릴리즈: v1.11.0 (2026-08-17) — Persona Layer · 실존 인물 페르소나 층 Latest release: v1.11.0 (2026-08-17) — Persona Layer · perspective-taking tier for real people

/ingest 의 세 번째 모드. 논문(DOI·arXiv·PDF)을 자동 감지해 요약이 아니라 **집필용 대조 자산**으로 해부 — 1 Raw Source + 1 허브(S00) + 지식 원자 30~100+ (12단 좌표). 같은 날 나온 v1.9.0 Research Question 카드와 연결되어 논문 → 질문 → 논증 파이프라인이 킷 안에서 완결된다.
The third /ingest mode. Academic papers (DOI, arXiv, PDF) are auto-detected and dissected into a **writing-grade reference asset** — 1 Raw Source + 1 hub (S00) + 30–100+ knowledge atoms on 12 analysis coordinates. Linked to the same-day v1.9.0 Research Question cards, the paper → question → argument pipeline is now complete inside the kit.

* **12단 좌표계** — S01 CITATION 부터 S12 WRITING VALUE 까지 공통 골격 × 6 논문 유형 (양적·질적·이론개념·혼합·척도개발·메타분석) 변형. 12단은 파일 수가 아니라 *좌표* — 모든 지식 원자가 정확히 하나의 축과 하나의 질문을 갖는다.**12-coordinate system** — a shared skeleton from S01 CITATION to S12 WRITING VALUE, with variations across 6 paper types (quantitative, qualitative, theory-concept, mixed-methods, scale-development, meta-analysis). Steps are *coordinates, not files* — every knowledge atom pins one axis and answers one question.
* **기계 검증 게이트** — `p7_verify.py` 가 YAML·좌표·provenance·인용 *전수 verbatim 대조*·Coverage·카탈로그↔파일 정합을 검사. 컴파일 에이전트의 "자체 검증 OK" 가 아니라 스크립트 ALL PASS 가 완료 조건.**Machine verification gate** — `p7_verify.py` checks YAML, coordinates, provenance, *every quote verbatim* against the Raw Source, coverage, and catalog↔file parity. Done means script ALL PASS, not the compiling agent's self-check.
* **템플릿 11종 + 매뉴얼** — Paper Hub·Paper Analysis Note·Atomization SPEC·Scale Page 추가 (7→11) + 사람용 `Paper Ingest Guide` (12단계 해설). Zotero 는 옵션 — provisional citekey 로 완결. v1.9.1 은 RQ/Synthesis 사용 가이드 docs 패치.**11 templates + manual** — Paper Hub, Paper Analysis Note, Atomization SPEC, and Scale Page added (7→11), plus a human-readable `Paper Ingest Guide` explaining the 12 steps. Zotero is optional — provisional citekeys are self-sufficient. v1.9.1 was the RQ/Synthesis usage-docs patch.

[v1.11.0 릴리즈 + ZIP 다운로드v1.11.0 Release + ZIP download
→](https://github.com/johnfkoo951/cmds-llm-wiki/releases/latest)

폴더 구조Folder Structure

## 7 layers · 한 눈에 7 layers · at a glance

번호가 붙은 최상위 폴더는 7개(00·10·20·30·70·80·90)지만, **아키텍처의 핵심은 3층**입니다 — **10. Raw Sources(소스코드)** → **20. Wiki(실행파일)** → **Schema(CLAUDE.md, 컴파일러)**. 나머지 00·30·70·80·90 은 그 3층 위에서 돌아가는 **운영·지원 폴더**입니다. 아래 트리로 전체를 보고, 표에서 각 레이어가 무엇인지 확인하세요.
There are 7 numbered top-level folders (00·10·20·30·70·80·90), but the **architecture is really 3 layers** — **10. Raw Sources (source code)** → **20. Wiki (runtime)** → **Schema (CLAUDE.md, the compiler)**. The rest (00·30·70·80·90) are **operational / support** folders running on top of those three. Scan the tree for the whole, then the table for what each layer is.

CMDS\_LLM\_Wiki/
├── 00. Inbox/ ← 임시 처리 (queue for /ingest)
├── 10. Raw Sources/ ← 불변 (immutable, 248 files)
│ ├── 11. Articles/
│ ├── 12. Papers/
│ ├── 13. Books/
│ ├── 14. Transcripts/
│ ├── 15. Clippings/
│ └── 16. AI Research/
├── 20. Wiki/ ← LLM 컴파일 (compiled, 754 pages)
│ ├── 21. Concepts/ (230 — 추상 개념)
│ ├── 22. Entities/ (187 — 사람·도구·조직)
│ ├── 23. Guides/ (36 — 운영 가이드)
│ └── 24. Maps/ (20 — MOC)
├── 30. Queries/ ← 합성 답변 file-back (25 queries)
├── 70. Outputs/ ← 도구 산출물 (graphify · etc, dated 폴더)
├── 80. References/ ← 첨부파일
├── 90. Settings/ ← 템플릿·공유 설정
│
├── CLAUDE.md ← Schema Layer (LLM 행동 규약)
├── AGENTS.md ← 타 에이전트용 (Codex 등)
├── Core Context.md ← 마더십 사용자 컨텍스트 snapshot
├── index.md ← Master Index (auto-updated)
├── LLM-Wiki-Starter-Kit.md ← 외부 사용자 안내
└── log.md ← Ingest/Query 활동 로그

### 각 레이어 상세 Each layer explained

| 레이어Layer | 무엇인지What it is | 역할Role | 소유 · 특성Owner · trait |
| --- | --- | --- | --- |
| `00. Inbox` | 대기소 (pre-ingest)Staging (pre-ingest) | Web Clipper·캡처가 착지하는 임시 큐. `/ingest` 가 읽어 10.Raw 로 이동Temporary queue where Web Clipper/captures land; `/ingest` moves them into 10. Raw | 처리 후 비움Emptied after processing |
| `10. Raw Sources` | ① 소스코드 (불변)① Source code (immutable) | 원본을 verbatim 보관 — 모든 위키 주장의 근거. 11 Articles·12 Papers·13 Books·14 Transcripts·15 Clippings·16 AI ResearchOriginals kept verbatim — the evidence behind every wiki claim. 11 Articles · 12 Papers · 13 Books · 14 Transcripts · 15 Clippings · 16 AI Research | 인간 큐레이션 · **절대 수정·삭제 금지**Human-curated · **never edited/deleted** |
| `20. Wiki` | ② 실행파일 (LLM 관리)② Runtime (LLM-managed) | Raw 를 컴파일한 지식 페이지. 21 Concepts·22 Entities·23 Guides·24 Maps(MOC)Knowledge pages compiled from Raw. 21 Concepts · 22 Entities · 23 Guides · 24 Maps (MOC) | LLM 작성·cross-reference · 모든 주장에 출처LLM-written, cross-referenced · every claim sourced |
| `CLAUDE.md / AGENTS.md` | ③ 스키마 (하네스)③ Schema (harness) | LLM 행동 규약 = "컴파일러 정의". 폴더 규칙·frontmatter·operation·검증 기준The LLM's rulebook = defines the compiler: folder conventions, frontmatter, operations, verification criteria | 인간+LLM 공동 진화Human + LLM co-evolve |
| `30. Queries` | 질의 산출물 (운영 축)Query output (operational) | `/query`·`/audit` 가 위키를 종합한 답변을 file-back. "좋은 답변은 새 페이지로"`/query`/`/audit` file synthesized answers back — "good answers become new pages" | LLM 생성 · **4번째 구조층 아님**LLM-made · **not a 4th structural layer** |
| `70. Outputs` | 도구 산출물 격리Tool-output isolation | graphify 등 외부 도구 결과. wiki(컴파일 결과물)와 라이프사이클 분리External tool results (graphify, etc.) — isolated from the wiki, different lifecycle | dated 폴더 · 스키마 규칙 면제Dated folders · exempt from schema rules |
| `80. References` | 첨부 저장소Attachment store | 모든 이미지·첨부를 한 곳(Attachments)으로 일원화All images/attachments unified in one place (Attachments) | 지원Support |
| `90. Settings` | 설정·템플릿Settings · templates | Obsidian 노트 템플릿 · Web Clipper 공유 설정Obsidian note templates · Web Clipper sharing config | 지원Support |

## 아키텍처 깊이 들어가기 Dig into the architecture

3-Layer 패턴, 시스템 파일 디테일, Living Reference Policy, 5종 검색 방법 — 모두 문서에서.
3-Layer pattern, system file details, Living Reference Policy, 5 search methods — all in the docs.

[문서 읽기
Read docs
→](/docs/)

만든 사람 · ConnectAbout the author · Connect

## 구요한 具耀翰 Yohan Koo 具耀翰

커맨드스페이스(CMDSPACE) 대표 · 차의과학대학교 겸임교수 · 국가과학기술인력개발원(KIRD) 객원교수. AI 활용 · 지식관리 · 업무자동화 강의와 임원 코칭을 합니다. SK 경영포럼(이천포럼) 2년 연속 연사, LG그룹 900명 임원교육, LG전자·LG이노텍 CEO 1:1 코칭. 5,300+ 옵시디언 노트를 운영하는 지식관리 실천가. **"바로 쓸 수 있는 것만, 깊이 있게."**
CEO of CMDSPACE · Adjunct Professor at CHA University · Visiting Professor at KIRD. Lectures and executive coaching on AI, knowledge management, and workflow automation. Two-time SK Management Forum speaker, LG's 900-executive program, and CEO 1:1 coaching at LG Electronics/Innotek. A knowledge-management practitioner running 5,300+ Obsidian notes. **"Only what you can use tomorrow — in depth."**

[🔗 모든 링크 · litt.ly/cmdsAll links · litt.ly/cmds](https://litt.ly/cmds)
[LinkedIn](https://www.linkedin.com/in/yohan-koo-a1baa3138/)
[X](https://x.com/YohanKoo)
[Threads](https://www.threads.com/%40cmds_pace)
[Instagram](https://www.instagram.com/cmds_pace/)
[YouTube](https://www.youtube.com/%40cmdspace)
[GitHub](https://github.com/johnfkoo951)
Email
[cmdspace.work](https://cmdspace.work)

![CMDS](/assets/logos/cmds-logo-round.png)

**CMDS LLM Wiki**
Karpathy 패턴 위성 볼트 · 구요한Karpathy pattern satellite vault · Yohan Koo

[문서Docs](/docs/)
[마더십Mothership](https://system.cmdspace.work)
[GitHub](https://github.com/johnfkoo951/cmds-llm-wiki)
[구요한 · BioBio](/bio)
[CMDSPACE](https://cmdspace.work)

© 2026 CMDSPACE · Karpathy LLM Wiki Pattern (2026-04-06) 의 Obsidian 구현 · 마더십 시스템 파일은 [system.cmdspace.work](https://system.cmdspace.work) 에서.
© 2026 CMDSPACE · Obsidian implementation of the Karpathy LLM Wiki Pattern (2026-04-06). Mothership system files at [system.cmdspace.work](https://system.cmdspace.work).
