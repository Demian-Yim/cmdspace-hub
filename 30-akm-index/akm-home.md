---
title: akm-home
source: https://akm.cmdspace.work/
author: 구요한 (CMDSPACE)
fetched: 2026-08-28
note: markitdown HTML→MD 자동 변환 스냅샷. 정확한 원문은 source URL 참조.
---

[![CMDS](/assets/logos/cmds-logo-round.png)
AKM Index](/)

[Pillars필러](#pillars)
[Rubric루브릭 전문](/rubric.html)
[Dimensions서술 축](/dimensions.html)
[Study연구 참여](https://akm-study.cmdspace.work)
[Scoring채점](#ladder)
[Baseline기준 사례](#baseline)
[Board보드](#board)
[Get assessed →평가 받기 →](/submit.html)

EN

AKM Index v1.2 · Updated 2026-08-02
AKM Index v1.2 · 2026-08-02 개정

# How mature is your knowledge system when AI agents run it? AI 에이전트가 함께 굴리는 지식관리, 몇 점입니까?

The AKM Index (Agentic Knowledge Management Index) is an open, evidence-based rubric — 5 pillars × 25 criteria, scored 0–100 with behaviorally anchored levels. Every point requires an artifact: a file path, a config, a dated log. Built and calibrated on a 10,000-note production system.
AKM Index(에이전트 지식관리 지수)는 공개 증거 기반 루브릭입니다 — 5개 필러 × 25개 기준, 행동 앵커 레벨로 0–100점. 모든 점수는 아티팩트(파일 경로·설정·날짜 있는 로그)를 요구합니다. 10,000 노트 규모의 실제 운영 시스템에서 만들어지고 캘리브레이션됐습니다.

[See the rubric루브릭 보기](/rubric.html)
[Rubric (KR .md)루브릭 전문 (KR .md)](/files/akm-index-v1.2-kr.md)
[Rubric (EN .md)루브릭 전문 (EN .md)](/files/akm-index-v1.1-en.md)
[GitHub](https://github.com/johnfkoo951/akm-eval)

5

pillars

필러

25

criteria

기준

0–100

points

점수

M0–M4

maturity bands

성숙도 밴드

The Idea

핵심 아이디어

## Score the system, not the notes — the human, the knowledge base, the agent runtimes, and the loop that binds them. 노트가 아니라 시스템을 채점한다 — 사람, 지식 기반, 에이전트 런타임, 그리고 이들을 묶는 루프까지.

A beautiful Zettelkasten scores low if agents can't reach it. Rough notes score high if the agent pipeline around them is sound. The unit of measurement is the whole working system: a persistent knowledge store, at least one agent runtime connected to it, and evidence of use within the last 30 days.

Two rules keep it honest. *Self-report caps at level 1* — anything higher needs an artifact. And *level 4 requires a record of the system fixing itself*: an audit that changed a rule, an incident that became a hook. No record, no 4 — however sophisticated the setup.

아무리 아름다운 제텔카스텐도 에이전트가 접근할 수 없으면 낮은 점수를 받습니다. 노트가 거칠어도 그 주변의 에이전트 파이프라인이 견고하면 높은 점수를 받습니다. 측정 단위는 작동하는 시스템 전체입니다 — 지속적 지식 저장소, 그것에 연결된 에이전트 런타임 1개 이상, 그리고 최근 30일 내 사용 흔적.

두 가지 규칙이 엄밀함을 지킵니다. *자기보고는 상한 1점* — 그 이상은 아티팩트가 필요합니다. 그리고 *레벨 4는 "시스템이 시스템을 고친 기록"이 필수*입니다: 규칙을 바꾼 감사, 훅이 된 사고 기록. 기록이 없으면 아무리 정교해도 4는 없습니다.

The Five Pillars
5개 필러

## Five pillars, weighted by what carries the system. 시스템을 떠받치는 무게대로 가중치를 준 5개 필러.

Context weighs most — supplying the right knowledge is why the system exists. Interop weighs least, so single-runtime users aren't punished. Each pillar holds five criteria, each scored 0–4.
컨텍스트가 가장 무겁습니다 — 맞는 지식을 공급하는 것이 시스템의 존재 이유이기 때문입니다. 이식성이 가장 가벼운 이유는 단일 런타임 사용자에게도 공정하기 위해서입니다. 필러마다 5개 기준, 기준마다 0–4 레벨.

P

Prompt Engineering20%

Are instructions to agents managed as versioned assets — layered, contracted, routed, exemplified, lifecycled?

에이전트에게 주는 지시가 버전 관리되는 자산인가 — 계층화 · 계약 명세 · 트리거 라우팅 · 예시 · 수명주기.

P1–P5

C

Context Engineering25%

Can agents find the right knowledge at the right size — taxonomy, metadata, retrieval, progressive disclosure, provenance?

에이전트가 맞는 지식을 적정 분량으로 찾을 수 있는가 — 주소체계 · 메타데이터 · 검색 · 점진 공개 · 출처와 신선도.

C1–C5

H

Harness Engineering20%

Is the runtime equipped and safe — tool surface, skill library, guardrails, persistent memory, orchestration?

런타임이 강력하고 안전하게 정비됐는가 — 도구 표면 · 스킬 라이브러리 · 가드레일 · 지속 메모리 · 오케스트레이션.

H1–H5

L

Loop Engineering20%

Does the cycle actually run and compound — pipeline, cadenced reviews, backlog control, write-back, self-correction? Requires 30-day operating evidence.

사이클이 실제로 돌고 복리로 쌓이는가 — 파이프라인 · 주기 리뷰 · 적체 관리 · 복리 환류 · 자기교정. 최근 30일 가동 증거 필수.

L1–L5

X

Interop & Governance15%

Does it survive beyond one runtime and one disk — portability, topology, recoverability, security, shareability?

하나의 런타임·디스크 너머에서도 살아남는가 — 런타임 이식성 · 토폴로지 · 복구 · 보안 · 전수 가능성.

X1–X5

### P 4.0×5

1. Instruction layering지시 계층화
2. Task contracts작업 계약 명세
3. Trigger & routing design트리거·라우팅 설계
4. Exemplars & counter-examples예시·반례 코퍼스
5. Prompt asset lifecycle프롬프트 자산 수명주기

### C 5.0×5

1. Taxonomy & addressability지식 주소체계
2. Machine-readable metadata기계가독 메타데이터
3. Retrieval infrastructure검색 인프라
4. Progressive disclosure & budget점진 공개·컨텍스트 예산
5. Provenance & freshness출처·신선도 관리

### H 4.0×5

1. Tool surface도구 표면
2. Skill & automation library스킬·자동화 라이브러리
3. Guardrails & permissions권한·가드레일
4. Persistent memory & state지속 메모리·상태
5. Orchestration & observability오케스트레이션·관측성

### L 4.0×5

1. Defined pipeline파이프라인 정의
2. Cadenced reviews주기 리뷰
3. Backlog & flow control적체·흐름 관리
4. Compounding write-back복리 환류
5. Self-correction loop자기교정 루프

### X 3.0×5

1. Cross-runtime portability런타임 이식성
2. Device & agent topology기기·에이전트 토폴로지
3. Recoverability복구 가능성
4. Security & privacy보안·프라이버시
5. Shareability & standardization전수·표준화

[25개 기준 전체 앵커 보기 (레벨 0–4 상세)Browse all 25 criteria with level 0–4 anchors](/rubric.html)

The Maturity Ladder
성숙도 사다리

## One ladder for all 25 criteria. Reproducible by design. 25개 기준 전부에 같은 사다리. 그래서 재현 가능합니다.

Every criterion climbs the same five rungs. Different evaluators looking at the same evidence should land within one level of each other — that's the design goal, borrowed from behaviorally anchored rating scales.
모든 기준이 같은 다섯 단을 오릅니다. 같은 증거를 본 다른 평가자가 ±1레벨 안에 도달하는 것 — 행동기준평정척도(BARS)에서 빌려온 설계 목표입니다.

0

Absent부재

×0.00

The concept doesn't exist yet.

해당 개념이 존재하지 않음.

1

Ad-hoc임시

×0.25

Done by hand, undocumented, unreproducible.

그때그때 손으로. 문서 없음, 재현 불가.

2

Documented문서화

×0.50

Rules exist on paper; compliance depends on willpower.

규칙은 문서로 존재하나 준수는 사람 의지에 의존.

3

Systematized시스템화

×0.75

Tooling enforces the rule — breaking it is harder than keeping it.

도구·훅이 규칙을 강제 — 어기기가 지키기보다 어려움.

4

Self-improving자가개선

×1.00

A recorded case of the system fixing itself. No record, no 4.

시스템이 시스템을 고친 기록된 사례. 기록 없으면 4 없음.

**Evidence or cap at 1증거 없으면 상한 1**Self-report alone never scores above level 1. Cite a file path, config, or dated log.자기보고만으로는 1점이 상한. 파일 경로·설정·날짜 있는 로그를 인용해야 합니다.

**Conservative ties애매하면 낮은 쪽**Between two levels? Take the lower one. Inflation is the default failure mode of self-assessment.두 레벨 사이에서 애매하면 낮은 쪽. 인플레이션은 자기평가의 기본 실패 모드입니다.

**30-day rule for Loop루프 필러 30일 규칙**L-pillar levels 3+ require dated artifacts from the last 30 days. Pretty pipelines without recent runs cap at 2.L 필러 3점 이상은 최근 30일 날짜가 찍힌 아티팩트 필수. 가동 흔적 없는 파이프라인은 2점 상한.

**Anti-cramming벼락치기 무효**Artifacts batch-created days before an assessment don't count as loop evidence. Dates are checked.평가 직전 일괄 생성된 아티팩트는 루프 증거로 불인정. 날짜를 확인합니다.

**Adversarial verification적대적 검증**Before a score is final, a skeptic pass attacks every level in both directions and spot-checks the claims.점수 확정 전, 검증 패스가 모든 레벨을 양방향으로 공격하고 주장을 스팟체크합니다.

**Bands성숙도 밴드**0–20 M0 Manual · 21–40 M1 Tooling · 41–60 M2 Structured · 61–80 M3 Orchestrated · 81–100 M4 Compounding.0–20 M0 수동 · 21–40 M1 도구화 · 41–60 M2 체계화 · 61–80 M3 오케스트레이션 · 81–100 M4 복리형.

Calibration Baseline
캘리브레이션 기준 사례

## The reference system scores 72.0 — and that's the point. 기준 시스템의 점수는 72.0 — 바로 그게 핵심입니다.

CMDS — the 10,000-note, 7-vault, 81-skill system this rubric was built on — was audited by 8 parallel agents across 130 tool calls, then challenged by 5 adversarial verifiers. Two scores were revised downward on decisive evidence. If the rubric gave its own author 95, you shouldn't trust it.
이 루브릭의 모체인 CMDS(10,000 노트 · 7볼트 · 81스킬)를 8개 병렬 에이전트가 130회 도구 호출로 감사하고, 5개 적대적 검증 패널이 공격했습니다. 2개 점수가 결정적 증거로 하향됐습니다. 루브릭이 제 저자에게 95점을 줬다면 믿을 이유가 없었을 겁니다.

PPrompt프롬프트

16 / 20

CContext컨텍스트

20 / 25

HHarness하네스

14 / 20

LLoop루프

13 / 20

XInterop이식성·거버넌스

9 / 15

72.0
**M3 Orchestrated오케스트레이션**
4 criteria reached level 4 · 8 criteria docked to level 2레벨 4 달성 4개 · 레벨 2 감점 8개

**What earned level 4레벨 4를 만든 것**Incident postmortems that became rules, a write-blocking validation hook born from a real failure, token budgets measured-redesigned-remeasured.규칙이 된 사고 포스트모템, 실제 실패에서 태어난 쓰기 차단 검증 훅, 측정→재설계→재측정된 토큰 예산.

**What got docked감점된 것**Weekly reviews that never ran, a 10,000-note vault with no git backup, an empty global agent file, plaintext tokens in config.한 번도 안 돌아간 위클리 리뷰, git 백업 없는 10,000 노트 볼트, 0바이트 전역 에이전트 파일, 설정 속 평문 토큰.

**The diagnosis한 줄 진단**"The system already knows how to fix itself — the human hasn't rejoined the loop, and there's no safety net." Most sophisticated setups fail the same way."시스템이 시스템을 고치는 능력은 이미 있는데, 사람이 루프에 복귀하지 않았고 안전망이 없다." 정교한 시스템 대부분이 같은 방식으로 무너집니다.

**Since then그 후**Four rounds later (Aug 22): 72.0 → 74.25 → 77.25 → 80.75 — every gain from executed audit backlogs, verified by adversarial panels. The calibration case above stays frozen at round 1; the live trajectory is on the [board card](/report.html?id=cmds-2026-08).4회차까지(8/22) 72.0 → 74.25 → 77.25 → 80.75 — 상승분 전부가 감사 백로그의 실행 기록에서 나왔고 적대 패널 검증을 거쳤습니다. 위 기준 사례는 1회차에 고정해 두며, 살아 있는 궤적은 [보드 카드](/report.html?id=cmds-2026-08)에서 볼 수 있습니다.

Descriptive Dimensions · v1.2
서술 축 · v1.2

## The same 70 is not the same 70. 같은 70점이 같은 70점이 아닙니다.

A single-vault 300-note system at M3 and a 12-vault, 10,000-note ecosystem at M3 share a number — not an achievement. v1.2 fixes the reading without touching the score: three verifiable dimensions are reported alongside maturity. Not a difficulty multiplier (that invites inflating complexity — a Goodhart trap) but norming: state the comparison group, keep the score pure.
단일 볼트 3백 노트의 M3와 12볼트 1만 노트의 M3는 숫자만 같을 뿐 다른 성취입니다. v1.2는 점수를 건드리지 않고 해석을 고칩니다 — 검증 가능한 서술 축 3개를 성숙도 옆에 병기합니다. 난이도 계수 합산(복잡도 부풀리기를 유인하는 Goodhart 함정)이 아니라 규준 참조: 비교 집단을 명시하고 점수는 순수하게 지킵니다.

**M — Maturity (the score, unchanged)성숙도 (기존 점수, 불변)**25 criteria × level 0-4 anchors × 0-100. Still the only thing that is scored.25기준 × 레벨 0-4 앵커 × 0-100. 여전히 유일하게 채점되는 축.

**S — Scale규모**How much system is being operated — seven measured counts (notes, stores, runtimes, automations, skills, humans, years) → S/M/L/XL band.얼마나 큰 시스템을 운영하는가 — 실측 카운트 7필드(노트·저장소·런타임·자동화·스킬·인원·연차) → S/M/L/XL 밴드.

**A — Autonomy자율운영도**How much of the recurring operation runs without a human — a standard 8-operation checklist (backup, indexing, measurement, retrospective, hygiene, secrets, promotion, memory GC), each none/manual/auto.반복 운영이 사람 없이 도는 비율 — 표준 운영 8종(백업·인덱싱·측정·회고·위생·시크릿·승격·메모리정리) 각각 없음/수동/자동.

**O — Output coupling산출 결합도**Does knowledge reach third parties — artifacts delivered through the system in 90 days → O0-O3.지식이 제3자에게 닿는가 — 90일 내 시스템 경유 산출물 수 → O0-O3.

One score becomes a four-coordinate profile — e.g. the reference system now reads **M 77.25 (M3) · S-XL · A 88% · O3**. As profiles accumulate, the board aggregates them into a 2×2 portfolio matrix (Speedboat / Fleet / Casting off / Overloaded) and an Edwards-Parry response surface testing the scale-autonomy congruence hypothesis — with honesty gates: no fitted surface below N=30.
점수 하나가 4좌표 프로파일이 됩니다 — 기준 사례는 이제 **M 77.25 (M3) · S-XL · A 88% · O3**로 읽힙니다. 프로파일이 쌓이면 보드는 2×2 포트폴리오 매트릭스(쾌속정/함대/출항 준비/과적)와 Edwards-Parry 반응표면(규모-자율화 정합 가설)으로 집계합니다 — 단, N=30 미만에서는 곡면을 적합하지 않는 정직성 게이트와 함께.

[Dimensions — spec & charts →
서술 축 전문 · 그래프 보기 →](/dimensions.html)
[Spec .md (KR/EN)
명세 .md 내려받기](/files/akm-dimensions-v1.2-kr.md)

Assessment Board
평가 보드

## Assessed systems, on the record. 평가 받은 시스템들의 공식 기록.

Every card is an adversarially verified assessment. Only what each participant consented to share appears here — full reports open only where public detail was granted.
모든 카드는 적대적 검증을 통과한 평가입니다. 참여자가 동의한 범위만 공개되며, 상세 리포트는 공개 동의가 있는 경우에만 열립니다.

### 리더보드Leaderboard

총점순 · 카드 상세는 아래by total score · full cards below

| # | 시스템System |  | 총점Total | 밴드Band | P/20 | C/25 | H/20 | L/20 | X/15 | L4 | 프로파일Profile | 궤적Δ | 날짜Date | 응원Cheers |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Get Assessed
평가 받기

## Three ways to run the index on your system. 당신의 시스템에 지수를 돌리는 세 가지 방법.

1

Self-run셀프 평가

free · 10–60min무료 · 10–60분

Download the rubric, feed it to any capable coding agent with access to your system, follow the protocol: evidence → score → adversarial verify.

루브릭을 내려받아 시스템 접근 권한이 있는 코딩 에이전트에게 주고, 프로토콜대로: 증거 수집 → 채점 → 적대적 검증.

2

Remote kit원격 평가 킷

guided · 60–90min가이드 · 60–90분

No filesystem access needed — 14 artifact requests plus 34 interview questions with evidence probes. Request the kit by email.

파일시스템 접근 불필요 — 아티팩트 요청 14종 + 증거 프로브가 달린 인터뷰 34문항. 이메일로 킷을 요청하세요.

3

Workshop워크샵·강의

CMDSPACE

Team or cohort assessment with a debrief and an improvement roadmap ranked by expected point gain.

팀·코호트 단위 측정과 디브리핑, 예상 상승폭 순으로 정렬된 개선 로드맵까지.

**Self-run with the skill (Claude Code) — [full guide →](/submit.html)스킬로 셀프 평가 (Claude Code) — [상세 안내 →](/submit.html)**
`git clone https://github.com/johnfkoo951/akm-eval.git ~/.claude/skills/akm-eval` → 새 세션에서 "AKM 평가해줘". 상세 절차는 [참여 안내 페이지](/submit.html) 참조 ([ZIP](/files/akm-eval-skill.zip)도 제공 · 스킬 v1.2.2, 2026-08-02 갱신).
`git clone https://github.com/johnfkoo951/akm-eval.git ~/.claude/skills/akm-eval` → say "run the AKM Index" in a new session. Full walkthrough on the [participation page](/submit.html) ([ZIP](/files/akm-eval-skill.zip) also available · skill v1.2.2, updated 2026-08-02).

**Submission & privacy제출·프라이버시 정책**
스킬이 평가 종료 시 결과를 운영팀 수신함(`/api/submit`)에 업로드합니다 — 업로드 전 안내가 표시되며 **원치 않는다고 말하면 업로드하지 않습니다**. 기록은 비공개 저장소에 보관되고, **보드 공개는 별도 동의 플래그**(실명·이메일·상세 공개를 직접 선택)를 따릅니다. 철회는 언제든 이메일로 — 수신 영수증(receiptId)만 알려주시면 됩니다. 이메일 제출도 가능합니다.
The skill uploads results to the operations inbox (`/api/submit`) at the end of a run — you're notified first and **nothing is sent if you object**. Records live in private storage; **board publication is a separate opt-in** via consent flags (real name / email / detail visibility are your choice). Revoke anytime by email with your receiptId. Email submission also works.

## Measure it. Then compound it. 측정하세요. 그리고 복리로 쌓으세요.

The rubric is open — anchors, protocol, anti-gaming rules, everything. Attribution appreciated: "Based on AKM Index v1.2".
루브릭은 전부 공개입니다 — 앵커, 프로토콜, 안티게이밍 규칙까지. 사용 시 "AKM Index v1.2 기반" 표기를 권장합니다.

[Take the assessment평가 참여하기](/submit.html)
[Download EN rubricEN 루브릭 다운로드](/files/akm-index-v1.1-en.md)
Request assessment ✉평가 요청 ✉

![CMDSPACE](/assets/logos/cmds-logo-typo-black.png)
![CMDSPACE](/assets/logos/cmds-logo-typo-white.png)

Command your space.
당신의 공간을 지휘하세요.

© 2026 CMDSPACE · Yohan Koo · AKM Index v1.2

[GitHub](https://github.com/johnfkoo951/akm-eval)
[System Files](https://system.cmdspace.work)
[LLM Wiki](https://llm-wiki.cmdspace.work)
[CMDSPACE](https://cmdspace.work)
Contact
