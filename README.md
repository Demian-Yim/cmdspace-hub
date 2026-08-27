---
title: CMDSPACE Hub — 구요한(CMDSPACE) 스킬·엔지니어링·강의자료 통합 허브
project: 00 Skills / cmdspace-hub
owner: Max
status: approved
created: 2026-08-28
updated: 2026-08-28
version: 1.0
---

# CMDSPACE Hub

> **한 줄:** cmdspace.work(구요한, CMDSPACE) 생태계와 요청하신 GitHub 4곳의 **스킬·엔지니어링·강의자료**를 내려받아, Eva(Gemini/Antigravity)·Max(Claude Code)·Emil(GPT) 세 AI가 같은 자료를 같은 경로로 쓰도록 정리한 허브입니다.
> **정본 위치:** `D:/00 Antigravity/00 Skills/cmdspace-hub/` · **백업:** https://github.com/Demian-Yim/cmdspace-hub
> **전체 자산 표:** [CATALOG.md](CATALOG.md) · **Max 진입 스킬:** `cmdspace-hub`

---

## 0. 요청 소스 8개 → 무엇을 가져왔나

| # | 요청 URL | 정체 | 가져온 것 | 위치 |
|---|---|---|---|---|
| 1 | github.com/johnfkoo951 | 구요한 GitHub (64 repo) | 비포크·자산성 repo **10개** 클론 + 정훈님 계정 포크 | `_repos/` |
| 2 | github.com/AgriciDaniel/claude-blog | 블로그 글쓰기·SEO/GEO 플러그인 (★1.9k) | 클론 + 포크 + **Max 플러그인 설치** | `_repos/claude-blog/` |
| 3 | github.com/zubair-trabzada/geo-seo-claude | AI 검색(GEO)+SEO 감사 스킬 (★9.5k) | 클론 + 포크 + **Max 스킬 15종 설치**(venv 포함) | `_repos/geo-seo-claude/`, `~/.claude/skills/geo*` |
| 4 | github.com/uxjoseph/supanova-design-skill | 한국어 랜딩페이지 디자인 스킬 4종 | 클론 + 백업 repo + **Max 우산 스킬 설치** | `_repos/supanova-design-skill/`, `~/.claude/skills/supanova-design-skill/` |
| 5 | cmdspace.work | 서비스 허브(서브도메인 30여 개) | 홈 스냅샷 + 서브도메인 12곳 스냅샷 + PDF 2종 | `50-hub-sites/`, `20-lecture/`, `40-portfolio/` |
| 6 | slashpage.com/cmds-class | 강의 자료 포털 | **35 페이지 전량** Markdown 아카이브 + 인덱스 | `20-lecture/slashpage/` |
| 7 | labs.cmdspace.work/monthly-obsidian-20 | 월간 옵시디언 20회 강의노트 | 전문 Markdown | `20-lecture/monthly-obsidian-20-knowledge-base.md` |
| 8 | akm.cmdspace.work/rubric.html | AKM Index 루브릭 | 루브릭 KR/EN + 서술 축 KR/EN 원문 md + `akm-eval` repo | `30-akm-index/`, `_repos/akm-eval/` |

---

## 1. 폴더 구조

```
00 Skills/
├── cmdspace-hub/                     ← 이 허브 (git: Demian-Yim/cmdspace-hub)
│   ├── README.md                     ← 지금 이 문서 (단계별 가이드)
│   ├── CATALOG.md                    ← 자산 전수 표 (repo 13 · 웹 자료 · 설치 상태)
│   ├── 10-system-files/              ← CMDS 시스템 파일 (공식 ZIP v4.10.2 풀어놓음)
│   │   ├── CMDS-System-Files/        ←   CLAUDE.md·AGENTS.md·CMDS.md·CMDS-Guide.md·CMDS-Head-Quarter.md·DESIGN.md + rules/ 9종
│   │   ├── vault-map-architecture.md ←   2볼트 구조·rules 8·commands 8+7·skills 62·agents 4 지도
│   │   └── llm-wiki-showcase.md      ←   Karpathy 3층(Raw→Wiki→Schema) 구현 설명
│   ├── 20-lecture/                   ← 강의·발표 자료
│   │   ├── monthly-obsidian-20-knowledge-base.md   ← Agentic Memory 6계약·4층·솔루션 비교·검색 설계
│   │   ├── hrprompt-playbook-v3.md                 ← HR 프롬프트 플레이북 30+ 템플릿 7섹션
│   │   ├── openclaw-study-guide.md                 ← OpenClaw 24/7 개인 에이전트 가이드
│   │   ├── cmds-gobi-cohort-1.md · knowledge-resolution-course.md · talk-*.md · youth-*.md …
│   │   └── slashpage/ (35 md + _INDEX.md)          ← 생성형 AI 워크샵·세컨드 브레인·CS4BT·Obsidian 설정·프롬프트 모음
│   ├── 30-akm-index/                 ← AKM Index v1.2 (P·C·H·L·X 5필러 × 25기준) KR/EN + 서술 축 S/A/O
│   ├── 40-portfolio/                 ← yohan-ax-portfolio.pdf · cmdspace-brochure.pdf
│   ├── 50-hub-sites/                 ← cmdspace.work 홈·apps·cmdtrace 스냅샷
│   └── cross-ai/                     ← eva-cmdspace-pack.md · emil-cmdspace-pack.md (포터블)
└── _repos/                           ← git 클론 13개 (origin=Demian-Yim 포크 · upstream=원저자)
    ├── cmds-system-files  cmds-llm-wiki  cmds-vault  akm-eval  cmux-tips
    ├── 9yohan-constellation  cmds-18-lec-pj-tutorial  cmdspace-plugins
    ├── agent-archives  claude-code-actions
    └── claude-blog  geo-seo-claude  supanova-design-skill
```

---

## 2. 단계별 진행 기록 (재현 절차)

### 1단계 — 취득 (Discover)
- GitHub: `gh api users/johnfkoo951/repos`로 64개 전수 조회 → 포크·앱·개인용을 제외하고 **스킬/엔지니어링/강의 자산 10개** 선별. 나머지 3 repo는 직접 클론.
- 웹: `curl`로 ZIP·PDF·md 원문 직접 다운로드(akm rubric md 2종, dimensions md 2종, CMDS-System-Files.zip, PDF 2종). HTML 페이지 22곳은 `markitdown`/`markdownify`로 Markdown 변환(모든 파일 `source:` 프론트매터에 원 URL).
- slashpage 35페이지는 서브에이전트가 페이지별 Markdown + `_INDEX.md` 생성 (31 OK · 4 빈 페이지 · 0 실패).

### 2단계 — 정리 (Organize)
- 번호 접두 폴더(10~50)로 성격별 분리. 변환본은 프론트매터 `note:`에 "자동 변환 스냅샷, 정본은 source URL" 명시.
- 파일명은 ASCII로 통일(한글 파일명은 cross-AI 경로 인용 시 깨짐 방지).

### 3단계 — 설치 (Max에서 즉시 사용)
| 대상 | 방법 | 결과 |
|---|---|---|
| geo-seo-claude | `bash install-win.sh` (비대화) | `~/.claude/skills/geo/` + `geo-*` 15 스킬 + 에이전트 5(`~/.claude/agents/geo-*.md`) + `.venv`(bs4·requests·lxml·playwright·flask…) |
| claude-blog | `claude plugin marketplace add AgriciDaniel/claude-blog` → `claude plugin install claude-blog@agricidaniel-blog` | 32 스킬 · 5 에이전트 (`/blog write` 등) |
| cmdspace-plugins | `claude plugin marketplace add johnfkoo951/cmdspace-plugins` → `claude plugin install research-pipeline@cmdspace-plugins` | 5 스킬(lit-search·lit-review·citation-manager·journal-formatter·research-pipeline) · 5 에이전트 |
| supanova-design-skill | `~/.claude/skills/supanova-design-skill/` 우산 스킬 + `taste.md·redesign.md·soft.md·output.md` | 기존 `taste-skill` 계열과 **별개**로 공존 |
| cmds-system-files | 기존 스킬 SKILL.md 갱신 (v4.10.2·rules 9종·허브 링크) | — |
| cmdspace-hub | 신규 진입 스킬 `~/.claude/skills/cmdspace-hub/SKILL.md` | 이 허브의 인덱스 |

> **미설치(선택):** `dev-orchestrator@cmdspace-plugins`(README는 13 에이전트라 하나 실제 1/1 — 실체 부족) · geo `playwright install chromium`(스크린샷용, 150MB) · `geo-report-pdf`용 pandoc.

### 4단계 — 백업 (정훈님 GitHub)
- 13개 repo 모두 `origin = https://github.com/Demian-Yim/<name>` · `upstream = 원저자`.
  - 신규 포크 9개: cmds-llm-wiki·akm-eval·cmux-tips·9yohan-constellation·cmds-18-lec-pj-tutorial·cmdspace-plugins·agent-archives·claude-code-actions (+ 기존 포크 cmds-vault·claude-blog·geo-seo-claude 재사용)
  - `supanova-design-skill`은 원본이 taste-skill 포크라 GitHub fork 불가 → **독립 repo로 push**(이력 보존).
  - `cmds-system-files`는 4월 로컬 → upstream 8/27 **v4.10.2로 fast-forward** 후 Demian-Yim에 push.
- 이 허브 폴더 자체는 `Demian-Yim/cmdspace-hub` repo.

### 5단계 — 3-AI 배포 (Eva·Emil)
- `data/applied-skills.json`(SSOT)에 `geo`·`supanova-design-skill`·`cmdspace-hub` 3줄 등록 → `_automation/repo_skill_sync.py`(3일 주기 `DAE_ForkSkillSync`)가 `cross-ai/eva-fork-skills.md`·`emil-fork-skills.md`에 자동 반영.
- 허브 전용 포터블 팩: [cross-ai/eva-cmdspace-pack.md](cross-ai/eva-cmdspace-pack.md) · [cross-ai/emil-cmdspace-pack.md](cross-ai/emil-cmdspace-pack.md).

---

## 3. 세 AI가 쓰는 법

| | **Max (Claude Code)** | **Eva (Antigravity/Gemini)** | **Emil (ChatGPT)** |
|---|---|---|---|
| 진입 | 스킬 `cmdspace-hub` 자동 트리거(cmdspace·AKM·월간 옵시디언…) | `cross-ai/eva-cmdspace-pack.md`를 룰 폴더에 넣거나 프롬프트 첨부 | `cross-ai/emil-cmdspace-pack.md`를 커스텀 지시문/프로젝트 파일로 |
| 실행 능력 | 플러그인·스킬 직접 실행(`/geo audit`, `/blog write`, research-pipeline) | `gh repo clone Demian-Yim/<repo>` 후 로컬 실행 또는 규칙 재현 | 규칙·템플릿·루브릭 **텍스트만** 사용(HR 플레이북·AKM 채점표·CMDS 프로세스) |
| 대표 과제 | GEO/SEO 감사 보고서, 블로그 원고, 문헌 리뷰 파이프라인, 랜딩 HTML | 강의안·워크숍 설계에 CS4BT·세컨드 브레인 커리큘럼 차용, 이미지·앱 | HR 프롬프트 교육 자료, AKM 자가진단 문답, 강의 스크립트 초안 |

---

## 4. 재사용 가치 Top 7 (정훈님 강의·컨설팅 기준)

1. **AKM Index 루브릭** (`30-akm-index/akm-index-latest-kr.md`) — 5필러×25기준·성숙도 사다리·채점 프로토콜(§8, 10~60분) → 고객사 AI 지식관리 진단 워크숍에 그대로 투입 가능. 서술 축 S/A/O로 2×2·버블 시각화 문법까지 제공.
2. **월간 옵시디언 20회** (`20-lecture/monthly-obsidian-20-knowledge-base.md`) — Agentic Memory "6계약"(Write·Reconcile·Retrieve·Correct·Forget·Audit) + 4층 모델 + Mem0/Honcho/Cognee/Letta 비교 + 논문 9편 → 임원·연구자 대상 "AI 메모리와 지식베이스" 강의 골격.
3. **CMDS 시스템 파일** (`10-system-files/`) — CLAUDE.md·AGENTS.md·DESIGN.md·rules 9종 = "AI에게 주는 설계도" 실물. 정훈님 볼트/프로젝트 CLAUDE.md 개선 레퍼런스(precedence·memory-type·required-for 프론트매터 패턴).
4. **HR 프롬프트 플레이북 v3** (`20-lecture/hrprompt-playbook-v3.md`) — 7섹션 30+ 템플릿(채용·온보딩·성과·노무·분석·QA) + Prompt Canvas 6요소 + 보안 가이드 → HR 대상 AX 교육 실습지.
5. **CS4BT 커리큘럼·생성형 AI 워크샵** (`20-lecture/slashpage/19~23, 09~14`) — 기초→Foundation→Expert 3단 구조와 워크샵 5모듈 구성 = 커리큘럼 벤치마크.
6. **cmds-llm-wiki** (`_repos/cmds-llm-wiki`) — Karpathy 3층 + Claude·Codex 이중 하네스 + `/ingest`·`/query`·`/lint`·`/verify`·`/audit` 11 커맨드 → 정훈님 볼트의 `/ingest`·`/query` 고도화 참고(복제 아님).
7. **geo-seo-claude + claude-blog** — flowdesign.ai.kr 노출 개선(2026-08-23 착수)의 다음 단계: `/geo audit https://flowdesign.ai.kr` → `/geo llmstxt` → 인사이트 칼럼은 `/blog analyze`로 90점 게이트.

---

## 5. 갱신·유지 규약

```bash
# 개별 repo 최신화 (upstream → 로컬 → 정훈님 포크)
cd "D:/00 Antigravity/00 Skills/_repos/<repo>" && git pull upstream main && git push origin main
# geo 스킬 자체 업데이트
/geo-update            # Max에서
# 허브 웹 스냅샷 재수집: 이 README §2 1단계의 curl 목록 재실행 후 markitdown 변환
# 허브 커밋
cd "D:/00 Antigravity/00 Skills/cmdspace-hub" && git add -A && git commit -m "chore: refresh snapshots" && git push
```

- 새 CMDSPACE 자산 발견 시: 같은 번호 폴더에 넣고 `CATALOG.md` 1행 + (스킬이면) `data/applied-skills.json` 1줄.
- 주의 — `cmds-vault`·`cmds-llm-wiki`를 정훈님 옵시디언 볼트(StarterKit 구조)에 **그대로 이식 금지**(폴더 체계·rules 충돌). 아이디어·rules 문구만 차용.
- 저작권 — 강의자료·HR 플레이북·포트폴리오 PDF는 CMDSPACE 저작물. 내부 참고·재구성만, 외부 재배포 금지. repo는 각 라이선스(대부분 MIT) 준수.

---

## 6. 검증 (2026-08-28 실측)

- `_repos/` 13개 클론 · `git remote -v` 전부 origin=Demian-Yim / upstream=원저자 확인 · 포크 12개 `isFork=true`, supanova 독립 repo push 성공.
- 허브 파일: 10-system-files 19 · 20-lecture 34+36(slashpage) · 30-akm 7 · 40-portfolio 2 · 50-hub 3. HTML→MD 변환 22건 중 인코딩 깨짐 1건(hrprompt) 재변환 확인.
- slashpage 35/35 (31 OK · 4 EMPTY: 07·14·17·20은 원 페이지 자체가 링크만 있는 얇은 페이지).
- Max 설치: `claude plugin list`에 claude-blog·research-pipeline 로드, `~/.claude/skills/geo*` 16 폴더·`~/.claude/agents/geo-*` 5, 스킬 목록에 `geo`·`supanova-design-skill`·`cmdspace-hub` 노출 확인.
- 미검증: geo Playwright 스크린샷·PDF 보고서(pandoc 미설치) — 필요 시 `python -m playwright install chromium`.

## HISTORY
- 2026-08-28 v1.0 신설 — 정훈님 지시("cmdspace 8개 소스 다운로드·정리, Eva/Max/Emil 사용 가능하게" + "00 Skills와 내 깃허브에 백업"). (Max)
