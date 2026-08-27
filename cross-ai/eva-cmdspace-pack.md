---
title: CMDSPACE 허브 — Eva(Antigravity/Gemini) 포터블 팩
owner: Max
updated: 2026-08-28
for: Eva
---

# 🟦 CMDSPACE 허브 — Eva 포터블 팩

> Antigravity 룰 폴더에 넣거나 프롬프트에 첨부해 사용. Eva는 **코드 실행 + 이미지 생성 + 앱 빌드**가 되므로 ① `gh repo clone Demian-Yim/<repo>` 후 로컬 실행 또는 ② 규칙만 재현 중 택1.
> 정본 경로: `D:/00 Antigravity/00 Skills/cmdspace-hub/` (README.md → CATALOG.md) · 포크: `D:/00 Antigravity/00 Skills/_repos/`

## Eva가 맡을 것 (담당 Schumann🎼·Bowie🌟)

### 🎼 CMDS 시스템 파일 → 정훈님 프로젝트 CLAUDE.md/ANTIGRAVITY.md 개선
- **읽기:** `cmdspace-hub/10-system-files/CMDS-System-Files/{CLAUDE.md, AGENTS.md, CMDS.md, DESIGN.md}` + `rules/`
- **차용 패턴:** `precedence`(문서 우선순위 번호) · `memory-type`(feedback/reference) · `required-for/optional-for`(어느 작업에 필수인지) · `token-estimate` · `@include`. Eva용 파일은 원저자도 `ANTIGRAVITY.md`(precedence 3, 비공개)로 분리했다 — 정훈님 프로젝트에도 Eva 전용 시스템 파일을 같은 규격으로.
- **하지 말 것:** 볼트 폴더 체계(100~900)·TAB 들여쓰기 규칙을 정훈님 StarterKit 볼트에 이식하지 않는다.

### 🎼 강의·워크숍 설계 재료
- **커리큘럼 벤치마크:** `20-lecture/slashpage/19-cs4bt-curriculum.md`(기초→Foundation→Expert) · `09~14 생성형 AI 워크샵 5모듈` · `17 세컨드 브레인 워크샵` · `_INDEX.md` Top 5.
- **강의 프레임:** `20-lecture/monthly-obsidian-20-knowledge-base.md` — Agentic Memory **6계약**(Write·Reconcile·Retrieve·Correct·Forget·Audit) + 4층(정본/검색/추론/실행) + 솔루션 비교(Mem0·Honcho·Cognee·Letta) + 논문 9편. 임원·연구자 강의 골격.
- **HR 교육 실습지:** `20-lecture/hrprompt-playbook-v3.md` — 7섹션 30+ 템플릿, Prompt Canvas 6요소(Role·Task·Context·Inputs·Constraints·Output).
- **진단 워크숍:** `30-akm-index/akm-index-latest-kr.md` — 5필러(P·C·H·L·X)×25기준, 레벨 0~4, §8 채점 프로토콜(10~60분). 서술 축 `akm-dimensions-v1.2-kr.md`의 2×2(S×M)·버블(S×A, 크기 O) 시각화 문법 → Eva가 차트·다이어그램 생성.

### 🌟 시각·랜딩·이미지 (Eva 실행)
- **supanova-design-skill:** `gh repo clone Demian-Yim/supanova-design-skill` → `taste-skill/SKILL.md` + `output-skill/SKILL.md`를 프롬프트에 첨부 → 단일 HTML(Tailwind CDN·Pretendard·Iconify Solar) 랜딩 생성 → Eva가 렌더 확인·스크린샷. 설정: DESIGN_VARIANCE 8 · MOTION_INTENSITY 6 · VISUAL_DENSITY 3 · LANDING_PURPOSE conversion. 정훈님 룰(`landing-page-guide-v2`, 폰트 하한)이 우선.
- **9yohan-constellation:** `docs/files/personas/903-dewey-learn.md`(교육) · `901-kepler-map.md`(KM) · `909-calvin-advise.md`(컨설팅) = 서브에이전트 페르소나 카드. 초상·타일 이미지 생성(`scripts/build-yohan-tiles.py`)은 Eva 몫. 정훈님 6캐릭터 체계와 비교해 갭 찾기.
- **agent-archives:** mac 앱이지만 `history-server.py`+`history-viewer.html`+`update-index.py`는 순수 Python/HTML → Windows 세션 대시보드로 이식(Eva 코드 작업).

### 🌟 GEO 리포트 시각화 (Max가 감사 → Eva가 차트)
- Max가 `/geo audit https://flowdesign.ai.kr` 결과(JSON/MD)를 넘기면 Eva는 `_repos/geo-seo-claude/templates/geo-report-template.html` 스타일로 점수표·로드맵 차트 렌더. `docs/scoring-methodology.md` 참조.

## 공통 규칙
- 변환본(md)은 스냅샷 — 인용 시 프론트매터 `source:` URL을 함께 적는다.
- CMDSPACE 저작물(강의자료·HR 플레이북·PDF)은 내부 재구성만, 외부 재배포 금지.
- 새로 만든 산출물은 프로젝트 `docs/`에 두고 `current_state.md` 1줄.
