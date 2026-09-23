---
title: talk-sicem-2026-AI와-업무의-변화
source: https://sicem.cmdspace.work/
author: 구요한 (CMDSPACE)
fetched: 2026-08-28
note: markitdown HTML→MD 자동 변환 스냅샷. 정확한 원문은 source URL 참조.
---

[SICEM 2026](#hero)

⌨ space / arrows
⛶ Present

PRESENTATION MODE
`↓` next
`↑` prev
`esc` exit

SICEM 2026 Keynote

# AI로 달라지는 업무, 우리는 어떻게 대응할까? 의료진을 위한 AI Readiness

Speaker
:   구요한 (Yohan Koo)

Role
:   CMDSPACE · 차의과대학교 AI헬스케어융합학과 겸임교수

Date
:   2026.04.09 (목) 15:30 – 15:50

Track
:   Final talk · SICEM 2026

↓ scroll to begin

PROLOGUE

## 의사가 아닌 사람이 왜 여기에?

물리학 학부를 졸업하고, 교육공학 박사과정을 밟으며, 지난 3년간 대학병원 교수진과 의료 학회에서 AI 활용 교육을 진행해왔습니다. 임상의는 아니지만, 임상 현장의 맥락은 이해하고 있습니다.

5+
의료 학회 교육 (외과 · 혈관외과 · 간 · 혈액 · 조혈모세포이식)

3yr
CMDS 지식 시스템 운영 (7,600+ notes)

LG · SK
기업 AI 교육 컨설팅

● THE CORE QUESTION

## 선생님의 지식, AI가 읽을 수 있나요?

20년 임상 경험. 진료 노하우. 연구 패턴. 이 지식이 지금 — **AI가 읽고 활용할 수 있는 형태**로 남아 있습니까?

THE PARADOX

## AI 도구는 넘치는데, 왜 업무는 안 바뀌는가?

ChatGPT가 출시된 지 3년 반. 그동안 Claude, Gemini, Copilot, 그리고 의료 특화 AI까지 수십 개가 쏟아졌습니다.

ChatGPT

Claude

Gemini

Copilot

Perplexity

Med-PaLM

Elicit

Consensus

Glass Health

Doximity GPT

그런데 솔직히 — 선생님의 연구 워크플로우가 근본적으로 바뀌셨습니까? 대부분 "가끔 ChatGPT에 물어보는 정도"에 머물러 있습니다.

THE METAPHOR

## 비포장도로 위의 슈퍼카

🏎️

AI TOOLS

최신형 슈퍼카

🛣️

YOUR KNOWLEDGE

비포장도로

도구(자동차)보다, 도로(지식 구조화)가 먼저다.

THE DIVIDE

## 같은 지식, 다른 운명

같은 내용의 지식이라도, 어떻게 저장하느냐에 따라 AI와의 관계가 완전히 달라집니다. 아래 토글을 눌러 각 형식을 비교해보세요.

임상 지식
연구 노트
행정 문서

### 비구조화 (현재)

✗ AI가 읽을 수 없음

### 구조화 (목표)

✓ AI가 즉시 활용 가능

이 차이가 앞으로 2~3년 안에 연구 생산성의 **결정적 격차**를 만듭니다.

INDUSTRY CONSENSUS · 2026

## 저만 드리는 말씀이 아닙니다

2026년, AI 업계의 최정상 3인이 **동시에 같은 결론**에 도달했습니다. 세 사람의 표현은 다르지만, 가리키는 방향은 하나입니다.

Andrej Karpathy

전 OpenAI · 전 Tesla AI Director

> RAG re-derives.
> Wiki compounds.

검색은 매번 다시 유도하지만, 위키는 누적된다.

OpenAI

Official Blog · 2026

> The agent isn't the hard part — the harness is.

어려운 건 에이전트가 아니라, 하네스(맥락 구조)다.

Tiago Forte

Building a Second Brain · 저자

> PKM is over.
> It's PCM now.

개인 지식 관리(PKM)에서 개인 맥락 관리(PCM)로.

세 사람이 같은 시기에 같은 결론을 냈습니다. **이건 우연이 아닙니다.**
오늘 제가 말씀드릴 *AI Readiness*는, 이 세 가지 통찰의 **의료 분야 버전**입니다.

THE FRAMEWORK

## AI 레디니스: 도구가 아니라 준비 상태

**AI Adoption(도입)**이 아니라, **AI Readiness(준비 상태)**에 집중하자.

01

### 지식 구조화

내 지식을 AI가 읽을 수 있는 형태로 정리한다. Markdown + YAML 메타데이터 + 위키링크.

⏱ 첫 1개 노트: 5분

02

### 워크플로우 정비

연구 파이프라인의 전 단계를 AI-Ready하게 재설계한다. 주제 발견부터 투고까지.

⏱ 이번 주: 10개 노트 이전

03

### AI 연결

하네스 위에 에이전트를 올린다. Claude, Cursor, GPT — 어떤 것이든 가능하다.

⏱ 이번 달: 첫 에이전트 연결

▲ 순서가 중요합니다. 많은 분들이 3번부터 시작하시려 해서 실패합니다.

STEP 1 · FILE FORMAT

## 지식 구조화: 왜 Markdown인가?

.DOCX

🔒

Word

잠긴 금고
독점 포맷

.PDF

📸

PDF

사진
사실상 이미지

NOTION

🏠

Notion

남의 집
클라우드 종속

.MD ✓

🔓

Markdown

열린 텍스트
30년 후에도 읽힘

어떤 AI든 즉시 읽을 수 있고, 30년 후에도 열립니다. Obsidian이 이 Markdown 파일들을 지식 네트워크로 만들어줍니다.

LIVE DEMO · EVIDENCE

## 구조화된 임상 지식, 이렇게 생겼습니다

7,600+
Notes · 노트 개수

3yr
운영 기간

1人
운영자

방금 보신 이 구조가 바로 Karpathy가 말한 *"Wiki Layer"*입니다. 저는 이걸 3년 전부터 운영해왔습니다.
**Karpathy가 2026년에 "해야 한다"고 말한 것을, 저는 이미 "해오고 있던" 것입니다.**

STEP 2 · PIPELINE

## 연구 워크플로우를 AI-Ready하게

01
주제 발견

02
문헌 검색

03
데이터 분석

04
원고 작성

05
투고

CURRENT · 현재 대부분

"원고 작성" 단계에서만 ChatGPT 사용

GOAL · 목표

5개 단계 모두에 AI 에이전트 연결

STEP 3 · AI EVOLUTION

## 검색 → 채팅 → 에이전트

2020

### 검색 시대

키워드를 입력하면 AI가 링크를 돌려줬습니다.

keyword → link

2023-2024

### 채팅 시대

질문하면 AI가 답변을 해줬습니다.

question → answer

2025 →

### 에이전트 시대

AI가 **스스로** 계획을 세우고, 여러 단계를 **자율적으로** 실행하고, 결과를 **검증**합니다.

goal → autonomous execution

> "The agent isn't the hard part — the harness is."

— OpenAI, Building Agents (2026)

에이전트를 기다리지 말고, 하네스를 먼저 만들자.

FOUR AGENTS FOR DOCTORS

## 의사를 위한 4가지 AI 에이전트

클릭하면 상세 내용이 펼쳐집니다.

AGENT 01

### 문헌 리뷰 에이전트

100편의 논문을 1시간에. 자동 합성 매트릭스 생성.

**프로세스:** PubMed 논문 100편 → AI Agent 자동 처리 → 합성 매트릭스 (저자·연도·방법·결과·한계점)

이전에 **2주** 걸리던 작업이, 이제 **1시간** 안에 끝납니다. 최종 검증은 의사 선생님의 몫 — AI는 초안을 만들고, 판단은 사람이 합니다.

2주 → 1시간 (336× faster)

▼ click to expand

AGENT 02

### 원고 작성 에이전트

구조화된 연구 노트에서 IMRaD 초안까지 자동 생성.

**프로세스:** 구조화된 연구 노트 → AI Agent → IMRaD 초안 (Introduction · Methods · Results · Discussion) → 저널 포맷팅 → 투고 체크리스트

핵심은 **"구조화된 연구 노트"**입니다. Markdown으로 정리된 노트가 있어야 에이전트가 제대로 작동합니다.

다시 강조 — 도로가 있어야 차가 달립니다.

▼ click to expand

AGENT 03

### 임상 지식 에이전트

20년 임상 경험 + 최신 근거를 통합한 "나만의 AI 교과서".

선생님이 20년간 쌓은 임상 경험, 진료 패턴, 약물 선택 기준을 구조화해놓으면 — AI가 이를 기반으로 답변합니다.

**예시 질문:** "DPP-4 억제제와 SGLT2 억제제 병용에 대한 최신 근거를, 내 진료 노트와 최신 논문을 모두 참조해서 정리해줘"

AI는 **선생님의 지식과 외부 지식을 합쳐서** 답변합니다. UpToDate를 넘어서, *나만의* 임상 교과서.

▼ click to expand

AGENT 04

### 행정 에이전트

회의록, 일정, 이메일 초안 — 행정 업무 완전 자동화.

**주요 기능:**

• 학회 미팅 녹음을 자동으로 회의록으로 변환
• 일정 최적화 및 리마인더
• 이메일 초안 자동 작성
• 연구비 신청서 보조

가장 간단해 보이지만, **확보되는 시간**이 가장 큽니다.

▼ click to expand

### 4개 에이전트가 합쳐지면

AI는 더 이상 '도구'가 아닙니다. 선생님의 **'연구팀'**이 됩니다.

**RA**문헌 검색/분석

**Editor**원고 다듬기

**Assistant**지식 정리

**Coordinator**행정 관리

24시간 일하고, 잠 안 자고, 월급 받지 않습니다.

TAKE ACTION TODAY

## 오늘부터 시작하세요

실천이 없으면 의미가 없습니다. 세 가지만 하시면 됩니다. 실행하시는 분과 안 하시는 분의 차이가, 앞으로 2~3년 안에 엄청나게 벌어질 겁니다.

01

### Obsidian 설치 + 첫 노트 1개

오늘 저녁 호텔 방에서. 이 발표에서 인상 깊었던 내용 하나를 Markdown으로 정리해보세요.

오늘 · 5분

02

### 진료/연구 노트 10개 이전

가장 자주 참고하시는 가이드라인, 연구 노트 10개를 Markdown으로 옮기세요. YAML 프로퍼티도 함께.

이번 주 · 1~2시간

03

### AI 에이전트 1개 연결

Claude, Cursor, ChatGPT — 어떤 것이든 상관없습니다. 직접 체험해보세요.

이번 달

![QR code to sicem.cmdspace.work](sicem-qr.png)

**sicem.cmdspace.work**
이 페이지 주소 · QR로 저장해두세요

THE GAP

## 2년 후, 돌이킬 수 없는 격차

AI 에이전트 기술은 **매년 2배씩** 좋아지고 있습니다. 2028년이 되면, 두 집단의 연구 생산성 격차는 되돌리기 어려울 만큼 벌어집니다.

2026
2027
2028
2029
→

Research Productivity

AI 없이

AI-Ready

GAP

AI-Ready 의사 (지수 곡선)

AI 없이 일하는 의사 (선형)

좋은 소식 — 지금 시작하면, 아직 늦지 않았습니다.

ONE SENTENCE TO REMEMBER

## AI를 배우지 마세요. AI가 읽을 수 있는 나를 만드세요.

도구는 계속 바뀝니다. ChatGPT가 사라져도, Claude가 바뀌어도 — 선생님의 **구조화된 지식**은 그 위에 어떤 AI든 올릴 수 있습니다. **도구가 바뀌어도, 선생님의 자산은 남습니다.**

![QR to sicem.cmdspace.work](sicem-qr-large.png)

sicem.cmdspace.work
Yohan Koo · [메일 주소 비공개]

감사합니다.

DESIGN VARIANTS · 같은 내용, 5가지 스타일

## 다른 디자인 버전

같은 콘텐츠를 네 가지 다른 디자인 스킬로 재구성해봤습니다. 같은 메시지가 어떻게 다른 목소리를 낼 수 있는지 비교해보세요.

[00

Dark Brutalist CURRENT

14개 인터랙션 · 스크롤 데크 · 발표모드 지원

67 KB · Vanilla JS · 직접 작성](/)
[01

CMDSPACE Brand

브랜드 일관성 · KO/EN 토글 · 9개 네비 웨이포인트

64 KB · IBM Plex Mono · cmdspace-web-builder](/brand)
[02

Minimal · Tufte × Swiss

극도의 미니멀 · 읽는 문서 · JS 0줄

10 KB · System Fonts · minimal-homepage](/minimal)
[03

Pretext Editorial

실제 폰트 측정 · width-tight · 멀티컬럼 + 드롭캡

53 KB · Noto Serif KR · pretext-web-builder](/pretext)
[04

Advanced Editorial

New Yorker × Stripe · 드롭캡 · WCAG AA+ · SVG 메타포

72 KB · Fraunces + Inter · frontend-design](/editorial)

GET IN TOUCH · 연락 및 팔로우

## 구요한 · Yohan Koo

발표 주제 관련 문의, 강연/컨설팅 요청, 연구 협업, 피드백 모두 환영합니다. 아래 채널 중 편하신 곳으로 연락 주세요.

📧

Email

[메일 주소 비공개]
[🔗

Link in Bio

litt.ly/cmds](https://litt.ly/cmds)
[📺

YouTube

@cmdspace](https://www.youtube.com/%40cmdspace)
[💼

LinkedIn

yohan-koo](https://www.linkedin.com/in/yohan-koo-a1baa3138/)
[𝕏

X (Twitter)

@YohanKoo](https://x.com/YohanKoo)
[🧵

Threads

@cmds\_pace](https://www.threads.com/%40cmds_pace)
[🎓

CMDS Class

강의 · 포럼 · 워크숍](https://class.cmdspace.kr/)
[📘

옵시디언 프로페셔널 노트

교보문고 구매 →](https://product.kyobobook.co.kr/detail/S000219435979)

© 2026 Yohan Koo · [메일 주소 비공개]

SICEM 2026 Keynote · Built with Claude Code

[Main](/) ·
[Brand](/brand) ·
[Minimal](/minimal) ·
[Pretext](/pretext) ·
[Editorial](/editorial)

Press `Space` or `↓` to navigate · `P` for presentation mode

✕ Close

![QR code](sicem-qr-large.png)

sicem.cmdspace.work
