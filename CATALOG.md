---
title: CMDSPACE Hub — 자산 카탈로그 (repo 13 · 웹 자료 · Max 설치 상태)
owner: Max
created: 2026-08-28
updated: 2026-08-28
version: 1.0
---

# CATALOG — 전수 자산 표

> 수량은 2026-08-28 로컬 파일 실측(`find`/`ls`). README 표기와 다른 곳은 ※로 정정. 상세 인벤토리는 §3.

## 1. Repo 13 — 한눈에

| # | repo (`_repos/`) | 유형 | 원저자 | 라이선스 | 최근 커밋 | skills | cmds | agents | rules | Win | 담당 | Max 설치 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | cmds-system-files | 참고 문서(시스템 파일) | johnfkoo951 | 미표기(CMDSPACE IP) | 2026-08-27 | 0 | 0 ※문서상 8 | 0 | **9** ※README 8 | ✅ | 공통 | 스킬 `cmds-system-files` |
| 2 | cmds-llm-wiki | Obsidian 볼트 템플릿 | johnfkoo951 | 미표기(자유 fork) | 2026-08-17 | 10(.agents) | 11 claude + 10 codex | 0 | 0 | ⚠️ sed·qmd mac | Max | 미설치(볼트 스코프) |
| 3 | cmds-vault | Obsidian 볼트 템플릿 | johnfkoo951(fork) | MIT(rules) | 2026-08-17 | 15 | 8 ※Win symlink | 0 | 7 ※README 8 | ⚠️ Gobi·symlink | Max | 미설치(참조용) |
| 4 | akm-eval | 평가 루브릭(스킬 1) | johnfkoo951 | MIT | 2026-08-03 | 1 | 0 | 0 | 0 | ✅ | Max | 미설치 ⚠️§4 |
| 5 | cmux-tips | 참고 문서 | johnfkoo951 | CC BY 4.0 | 2026-08-23 | 0 | 0 | 0 | 0 | ❌ mac 전용 | Emil | — |
| 6 | 9yohan-constellation | 참고 문서(페르소나 카드 10) | johnfkoo951 | 미표기 | 2026-08-23 | 0 | 0 | 0(카드 10) | 0 | ✅ 문서 | Eva | — |
| 7 | cmds-18-lec-pj-tutorial | 강의자료·튜토리얼 | johnfkoo951 | 미표기 | 2026-07-06 | 0 | 8 | 0 | 0 | ✅ | Max | 미설치(프로젝트 스코프) |
| 8 | cmdspace-plugins | Claude Code 플러그인 ×2 | johnfkoo951 | MIT | 2026-03-07 | 5+12 | 0 | 5+13 | 0 | ✅ | Max | `research-pipeline` 설치 / dev-orchestrator 미설치 |
| 9 | agent-archives | 도구·앱 | johnfkoo951 | 미표기 | 2026-01-12 | 0 | 0 | 0 | 0 | ❌ mac 앱(py 백엔드 이식 가능) | Eva | — |
| 10 | claude-code-actions | 강의자료(GitHub Actions 워크숍) | joonlab→johnfkoo951 | MIT | 2026-03-04 | 6 | 0 | 6 | 0 | ✅ 클라우드 실행 | Max | 미설치(포크해서 Actions로) |
| 11 | claude-blog | Claude Code 플러그인 | AgriciDaniel | MIT | 2026-08-26 | **32** | 30(`/blog *`) | 5+15 brain | 0 | ✅ install.ps1 | Max | **플러그인 설치** |
| 12 | geo-seo-claude | Claude Code 스킬 스위트 | zubair-trabzada | MIT | 2026-08-27 | 1+15 ※README 13 | 12(`/geo *`) | 5 | 0 | ✅ Git Bash | Max | **설치**(시스템 Python) |
| 13 | supanova-design-skill | 스킬 묶음(프롬프트 4) | uxjoseph | 미표기(taste-skill 준용) | 2026-03-17 | 4 | 0 | 0 | 0 | ✅ | 공통 | **우산 스킬 설치** |

백업: 1~12 = `Demian-Yim/<name>` 포크(`isFork=true`), 13 = 독립 repo(원본이 taste-skill 포크라 GitHub fork 불가). 모두 `origin=Demian-Yim`, `upstream=원저자`.

## 2. 웹 자료 (허브 폴더)

| 폴더 | 파일 | 원 URL | 형태 |
|---|---|---|---|
| 10-system-files | `CMDS-System-Files/` (6 문서 + rules 9) | system.cmdspace.work/files/CMDS-System-Files.zip | **원본 ZIP**(v4.10.2, 2026-08-27) |
| 10-system-files | system.cmdspace.work.md · system-docs.md · vault-map-architecture.md · llm-wiki-showcase.md | system / vault-map / llm-wiki .cmdspace.work | HTML→MD 변환 |
| 20-lecture | monthly-obsidian-20-knowledge-base.md | labs.cmdspace.work/monthly-obsidian-20 | HTML→MD (강의노트 전문) |
| 20-lecture | hrprompt-playbook-v3.md | hrprompt.cmdspace.work | HTML→MD (30+ 템플릿) |
| 20-lecture | openclaw-study-guide.md | openclaw.cmdspace.work | HTML→MD |
| 20-lecture | ai-deep-research-comparison · knowledge-resolution-course · knowledge-resolution-framework · cmds-gobi-cohort-1 · talk-2026-dream-transfer-multi-agent · talk-sicem-2026-ai-and-work-change · talk-showcloud-research-knowledge-resolution · youth-cmds-process-showcase · macos-terminal-emulator-comparison | 각 서브도메인 | HTML→MD |
| 20-lecture/slashpage | 01~35 + `_INDEX.md` | slashpage.com/cmds-class/* | 페이지별 MD (31 OK · 4 얇은 페이지) |
| 30-akm-index | akm-index-latest-kr/en.md · akm-dimensions-v1.2-kr/en.md | akm.cmdspace.work/files/* | **원본 MD** |
| 30-akm-index | akm-home.md · akm-rubric-page.md · akm-dimensions-page.md | akm.cmdspace.work | HTML→MD |
| 40-portfolio | yohan-ax-portfolio.pdf(482KB) · cmdspace-brochure.pdf(490KB) | cmdspace.work/assets/downloads/* | **원본 PDF** |
| 50-hub-sites | cmdspace.work-home.md · cmdtrace.md · apps-cmdspace-catalog.md | cmdspace.work 등 | HTML→MD |

## 3. Repo 상세 인벤토리

### 1. cmds-system-files
- **정의:** 10,000+ 노트 Obsidian PKM을 AI 에이전트가 읽고 운영하게 만드는 6 시스템 문서 + 공유 규칙 + 9 아키텍처 패턴 배포판.
- **6 시스템 문서(`files/`, precedence):** CLAUDE.md(1) · AGENTS.md(2) · CMDS.md(4) · CMDS-Guide.md(5) · CMDS-Head-Quarter.md(6) · DESIGN.md(9). 비공개 3종(ANTIGRAVITY.md=3, BRAIN.md=7, BRAIN_PROMPT.md=8) 미포함.
- **rules 9:** blank-line · directory-structure · file-creation · file-move · frontmatter-standard · indentation · mermaid · video-project-workflow · wikilink.
- **슬래시 커맨드(문서 언급, 실체는 cmds-vault):** /connect /merge /develop /share /inbox /lint /query /status.
- **9 패턴:** precedence · STATIC/DYNAMIC · @include · Essential · required-for/optional-for · memory-type · token-estimate · changelog · shared rules.
- **설치:** 6 문서를 볼트 루트, `rules/*.md`를 `.claude/rules/`, `{your-name}`·`{vault-path}` 치환. 의존성 없음.
- **재사용:** precedence·memory-type 패턴 → "에이전트에게 문서 읽히는 법" 강의 모듈 / rules 9종 → 수강생 볼트 표준 규칙 팩 / CMDS 4단계 + 100~900 카테고리 → 지식관리 진단 레퍼런스.

### 2. cmds-llm-wiki
- **정의:** Karpathy LLM Wiki(Raw→Wiki→Schema)를 Claude Code + Codex 이중 하네스로 실행하는 위성 볼트 템플릿(v1.11 Persona Layer).
- **`.claude/commands` 11:** audit · capture-tabs · inbox · ingest · lint · onboard · query · refresh-context · reindex · status · verify · **`.codex/commands` 10**(onboard 제외) · **`.agents/skills` 10** 동일.
- **hooks:** qmd-reindex.sh · validate-raw-source.sh · **scripts:** p7_verify.py(논문 12좌표 검증 게이트).
- **템플릿 13 · Web Clipper JSON 18**(arxiv·github·hackernews·linkedin·substack·youtube 등).
- **설치:** clone → Obsidian 볼트로 열기 → 플레이스홀더 치환 → `Core Context.md` 작성 → (선택) qmd → `/status` `/ingest` `/query` `/lint`.
- **Win 주의:** README의 `sed -i ''`는 BSD 문법(Git Bash는 `sed -i`), qmd는 Homebrew 전용(선택).
- **재사용:** `/ingest`의 "왜 수집하는가" 강제 질문 장치 / 이중 하네스 = 런타임 이식성 실습 / 12단 논문 분석 스키마 = 연구방법론 워크숍.

### 3. cmds-vault
- **정의:** cmds-system-files 규약 + Gobi Desktop 연동을 붙인 수업용 완성형 Obsidian 볼트(v1.2.2).
- **skills 15:** canvas-to-jpg · cmds-llm-wiki · cmds-maintenance · cmds-onboarding · create-gobi-homepage · daily-book-update · docx-to-markdown · gobi-cli · gobi-onboarding · md-to-pdf · obsidian-canvas · obsidian-mermaid · thinking-partner · video-add-chapters · video-cleaning.
- **commands 8:** connect · develop · inbox · lint · merge · query · share · status (루트 `commands/`·`rules/`는 Windows 체크아웃에서 symlink 텍스트 — 실체는 `90. Settings/94. Agent Settings/`).
- **rules 7**(blank-line·file-move 미포함) · **prompts 11**(CBH·DBU·DDO·DRB·EIC·GDR·RVA + Book 4종 AAV·OTP·PTI·SNS).
- **설치:** clone → Obsidian → WELCOME.md → `[[Me]]` 치환 → Gobi `init/warp/syncfiles/sync`.
- **재사용:** 수강생 배포용 "클론→바로 쓰기" 볼트 / onboarding 인터뷰 질문은행 → 컨설팅 인테이크 / Book 프롬프트 4종 → 저술 워크숍 / video-add-chapters → 강의 영상 후처리.
- **⚠️ 정훈님 볼트(StarterKit 구조)에 이식 금지 — 참조만.**

### 4. akm-eval
- **정의:** AKM Index v1.2(5필러×25기준, 0~100)로 자기 지식관리 시스템을 증거 기반 셀프 평가하고 리포트 생성하는 Claude Code 스킬(v1.2.2).
- **references 6:** rubric.md · rubric-en.md · report-schema.md · report-template.html(성적표) · runtime-paths.md(Codex/Gemini/Grok/Hermes/OpenClaw 경로 레지스트리) + README.
- **필러:** P Prompt 20% · C Context 25% · H Harness 20% · L Loop 20% · X Interop&Governance 15%. 레벨 0~4, 밴드 M0~M4.
- **설치:** `git clone … ~/.claude/skills/akm-eval` 또는 ZIP → "AKM 평가해줘". 10~60분 7단계.
- **⚠️ 데이터 전송:** 7단계에서 `akm-report.json`을 `akm.cmdspace.work/api/submit`으로 POST(동의 플래그 `consent.submit`, 거부 시 로컬만). 설치하면 **평가 전 정훈님 동의 확인 필수** — 그래서 이번엔 미설치, 루브릭 원문은 `30-akm-index/`로 활용.
- **재사용:** 수강 전/후 진단 평가지 / "자기보고 상한 1점·증거 필수" 규칙 / 성적표 템플릿 리브랜딩.

### 5. cmux-tips
- **정의:** macOS 터미널 cmux로 Claude Code 세션 수십 개를 병렬 운용한 필드 노트(README + appearance, 한국어판 포함). CC BY 4.0.
- **핵심:** project=workspace · session=tab 공간 기억 규칙, 워크스페이스 그룹, hooks→status pill→자동 큐레이션, `cmux read-screen/send` 원격 조종.
- **Win:** ❌ 실행 불가. 개념("병목은 실행이 아니라 주의")만 강의 인용. → Emil 요약·슬라이드화.

### 6. 9yohan-constellation
- **정의:** 9 역사적 요한 × 9 CMDS Division × 9 열매 1:1:1 매핑 다중 페르소나 에이전트 시스템 문서 + 랜딩.
- **페르소나 카드 10:** 00-9yohan-prime · 901-kepler-map(KM&Research) · 902-goethe-sense(Writing) · 903-dewey-learn(Teaching&Curriculum) · 904-bach-score(Media) · 905-neumann-compute(Analytics) · 906-baptist-prepare(Partnerships) · 907-mccarthy-reason(Product) · 908-huizinga-play(Events) · 909-calvin-advise(Consulting).
- **문서:** canonical.md · constellation.md · architecture.md · workflows.md · playbooks.md(10 시나리오) · schemas.md · yohans.md · RUNBOOK.md · yohan-registry.json. scripts 4(validate-persona-canon.py 등).
- **재사용:** 903·901·909 카드 = 교육·KM·컨설팅 서브에이전트 프롬프트 즉시 사용 / 9×9×9 삼중 폐쇄 = 역할 분해 워크숍 프레임 / 정훈님 6캐릭터(Pink~Kant) 체계와 비교 사례.

### 7. cmds-18-lec-pj-tutorial
- **정의:** 명령어 0개 — Claude Code에게 자연어로 시켜 git을 배우는 월간 CMDS 18회 실습 키트.
- **commands 8:** /start /setup-check /step /save /undo /experiment /ship /site · **guides 6:** 01 첫 저장소 → 02 저장·되돌리기 → 03 브랜치 → 04 PR → 05 GitHub Pages → 06 규칙화. `.claude/settings.json`에 force push·rm 차단.
- **설치:** 폴더에서 `claude` → `/start`. git·gh·Claude Code만.
- **재사용:** 비개발자 AI 교육 포맷(자연어 은유 커맨드) 복제 템플릿 / 6단 난이도 계단 = 90분~3시간 워크숍 뼈대 / settings.json 안전장치 = 모든 실습 repo 표준.

### 8. cmdspace-plugins
- **research-pipeline:** agents 5(literature-scout haiku · literature-analyst sonnet · manuscript-architect opus · manuscript-editor · publication-formatter) · skills 5(research-pipeline · lit-search · lit-review · citation-manager · journal-formatter) · MCP: PubMed·Firecrawl·Pinecone. **Max 설치됨.**
- **dev-orchestrator:** agents 13(Brain opus 4 · Hand sonnet 5 · Eye haiku 4) · skills 12(autopilot·focus·pipeline / plan·decompose·estimate / code-review·security-review·tdd / deepsearch·deepinit·hud). 미설치(정훈님 기존 에이전트 32명과 중복 — 필요 시 `claude plugin install dev-orchestrator@cmdspace-plugins`).
- **references 6:** tier-routing-guide · execution-plan-template · apa7-guide · manuscript-outline-template · pipeline-state-template · synthesis-matrix-template.
- **재사용:** 3-Tier(Brain/Hand/Eye) 모델 라우팅 = 비용-품질 오케스트레이션 강의 사례 / 5단 연구 파이프라인 = 대학원 워크숍 / APA7·synthesis matrix = 논문 작성 워크시트.

### 9. agent-archives
- **정의:** Claude Code·OpenCode 세션 히스토리 검색·태깅·통계·Resume 데스크톱 앱(Electron+FastAPI, SwiftUI 병행). mac 전용.
- **Win 재사용 포인트:** `history-server.py` + `history-viewer.html` + `update-index.py`는 순수 Python/HTML → 세션 활동 대시보드로 이식 가능(Eva). AKM "Loop 30일 가동 증거" 자동 수집 도구 아이디어.

### 10. claude-code-actions
- **정의:** GitHub Actions 무료 티어만으로 Claude Code 스케줄러를 만드는 4단계 워크숍(joonlab 원본 재구성).
- **workflows 11:** step1-hello-claude · step2-scheduled · step3-with-mcp · step4-full-pipeline · claude-code-report · daily-research-digest · genai-class-weekly · learning-content · meeting-actions · newsletter-draft · repo-health-dashboard. **skills 6 · agents 6 · templates 9 · docs 8**(prerequisites → advanced-patterns, cost-guide, troubleshooting).
- **설치:** Fork → Secrets `CLAUDE_CODE_OAUTH_TOKEN`(또는 `ANTHROPIC_API_KEY`) → Actions 탭 Run. **OS 무관** — Windows에서 완벽 사용.
- **재사용:** "서버 없이 AI 자동화" 강의 완제품 / `genai-class-weekly.yml`·`newsletter-draft.yml` = 정훈님 주간 강의자료·뉴스레터 자동 생성 파이프라인(현재 Windows 작업 스케줄러 기반 자동화의 클라우드 대안) / output/ 실제 결과물 = 시연 샘플.

### 11. claude-blog (v2.2.0)
- **skills 32:** blog(오케스트레이터) · blog-analyze · audio · audit · brand · brief · calendar · cannibalization · chart · cluster · decay · discourse · factcheck · flow · geo · google · image · locale-audit · localize · multilingual · notebooklm · outline · persona · repurpose · rewrite · schema · seo-check · strategy · style · taxonomy · translate · write.
- **agents 5:** blog-researcher · blog-reviewer · blog-seo · blog-translator · blog-writer · **brain agents 15**(curator 13 + claude-blog-secretary + workflow-coverage).
- **commands 30:** `/blog write|rewrite|analyze|brief|calendar|strategy|outline|seo-check|schema|repurpose|geo|audit|cannibalization|factcheck|image|persona|brand|discourse|taxonomy|notebooklm|audio|google|update|cluster|multilingual|translate|localize|locale-audit|flow|style|decay`.
- **5-Gate Delivery Contract:** ① Capability Discovery ② Format Completeness ③ Visual Verification(375/768/1280) ④ Content Review(90점+, P0 0) ⑤ Asset&Link Integrity. scripts 20(py) · references 22 · templates 12 · brain/ Obsidian 볼트(canon 10편·claim-ledger).
- **설치:** `/plugin marketplace add AgriciDaniel/claude-blog` → `/plugin install claude-blog@agricidaniel-blog` (**Max 완료**). Python 3.11+, 스크린샷 patchright/playwright, 이미지 Banana MCP/Gemini 폴백.
- **재사용:** 5-Gate = AI 산출물 품질관리 강의 결정적 사례 / references 22편(ai-slop-detection·eeat·cognitive-load…) = 콘텐츠 품질 교재 / templates 12 = 블로그·뉴스레터 포맷 / blog-style learn = 강사 문체 유지 / flowdesign.ai.kr 인사이트 칼럼 90점 게이트.

### 12. geo-seo-claude
- **skills 15 + 오케스트레이터 `geo`:** geo-audit · brand-mentions · citability · compare · content · crawlers · llmstxt · platform-optimizer · proposal · prospect · report · report-pdf · schema · technical · update.
- **agents 5:** geo-ai-visibility · geo-content · geo-platform-analysis · geo-schema · geo-technical. **commands 12:** `/geo audit|quick|citability|crawlers|llmstxt|brands|platforms|schema|technical|content|report|report-pdf`.
- **scripts 6**(brand_scanner · citability_scorer · crm_dashboard · fetch_page · llmstxt_generator · webapp) · **schema 6**(article-author · local-business · organization · product-ecommerce · software-saas · website-searchaction) · white-label/ · examples/(실제 감사 리포트 3종).
- **설치(완료):** `bash install-win.sh` → `~/.claude/skills/geo/`(scripts·schema·hooks) + `geo-*` 15 + `~/.claude/agents/geo-*.md` 5. ⚠️ **Windows 판은 venv를 만들지 않고 시스템 Python에 `pip --user`** — 스크립트가 실패를 삼켜 flask·playwright가 빠졌던 것을 수동 `pip install --user -r requirements.txt`로 보완(9종 import OK) + Playwright Chromium 설치·로드 확인. 미설치: pandoc(PDF).
- **재사용:** GEO = 2026 신규 강의 주제(도입 데이터: AI 유입 +527%, 전환 4.4×, 투자 마케터 23%) / scoring-methodology = "AI가 인용하는 글쓰기" 루브릭 / prospect+proposal+white-label = 컨설턴트 서비스화 완제품 / flowdesign.ai.kr `/geo audit` → `/geo llmstxt`.

### 13. supanova-design-skill
- **skills 4(폴더→frontmatter name):** taste-skill→`supanova-design-engine` · redesign-skill→`supanova-redesign-engine` · soft-skill→`supanova-premium-aesthetic` · output-skill→`supanova-full-output`. 설정 4(DESIGN_VARIANCE 8 · MOTION_INTENSITY 6 · VISUAL_DENSITY 3 · LANDING_PURPOSE conversion).
- **research/laziness 11편:** root-causes(cognitive-shortcuts · output-limits · rlhf-and-compute · training-data-bias) → remediation(prompt-engineering · parameter-tuning · architectural-patterns · reference-prompts) + findings.
- **스택:** Tailwind CDN + Pretendard + Iconify Solar, 단일 HTML, `word-break: keep-all`.
- **설치(완료):** `~/.claude/skills/supanova-design-skill/`(SKILL.md 우산 + taste/redesign/soft/output.md). 기존 `taste-skill` 계열(원본 영어판)과 공존.
- **재사용:** 한국어 타이포 표준 → 강의 모집 랜딩 품질 / output-skill = 모든 AI 산출물 범용 규칙 / laziness 11편 = "LLM은 왜 게으른가" 1회차 강의 자료 / 수치 슬라이더 = 프롬프트 파라미터화 실습.

## 4. 요주의 사항
1. **akm-eval 데이터 전송** — 7단계 `api/submit` POST. 설치·실행 시 `consent.submit:false`로 시작.
2. **저작권** — cmds-system-files·강의자료·HR 플레이북·PDF는 CMDSPACE 저작물(외부 재배포 금지). cmux-tips CC BY 4.0. 나머지 MIT/미표기.
3. **볼트 충돌** — cmds-vault·cmds-llm-wiki·cmds-system-files의 rules(들여쓰기 TAB·frontmatter 7속성·100~900 폴더)는 정훈님 볼트 StarterKit 규약과 다름. 문구 차용만.
4. **플러그인 Python 의존성** — claude-blog는 플러그인 설치만으로 textstat·patchright·google-genai가 안 깔린다. `dependency_smoke.py --component preflight|browser|audio`로 검사 후 `pip install --user` 보완(2026-08-28 수행).
5. **에이전트 과밀** — dev-orchestrator(13 에이전트)는 미설치 유지 권장. claude-blog brain agents 15는 플러그인 내부 `brain/`에 있고 글로벌 등록되지 않음.

## HISTORY
- 2026-08-28 v1.0 신설 — Explore 서브에이전트 인벤토리 + Max 실측 대조. (Max)
