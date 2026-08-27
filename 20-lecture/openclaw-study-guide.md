---
title: openclaw-study-guide
source: https://openclaw.cmdspace.work/
author: 구요한 (CMDSPACE)
fetched: 2026-08-28
note: markitdown HTML→MD 자동 변환 스냅샷. 정확한 원문은 source URL 참조.
---

$ SYSTEM.INIT // OpenClaw Study Guide

BRUTALIST EDITION

# OPEN / CLAW

개인 AI 에이전트의 모든 것\_

Clawdbot → Moltbot → OpenClaw Foundation Edition: 24/7 자율 AI 어시스턴트 완전 가이드

by CMDSPACE 구요한

**17**  DOCUMENTS

**30/49**  SKILLS

**24/7**  AGENT

**v2026.3.2**  LATEST

**250K+**  STARS

[Updates](#updates)
[Overview](#overview)
[Rules](#rules)
[Security](#security)
[Install](#install)
[Concepts](#concepts)
[OAuth](#oauth)
[Skills](#skills)
[Use Cases](#usecases)
[심층비교](#deepcomp)
[Architecture](#architecture)
[CLI비교](#comparison)
[Moltbook](#moltbook)
[Reference](#reference)
[Maint](#maintenance)

// BREAKING NEWS — 2026-03-04

## LATEST UPDATES

OpenClaw 생태계의 주요 변화와 최신 소식을 정리합니다.

// 2026-02-15

Peter Steinberger → OpenAI

OpenClaw 창립자 Peter Steinberger가 OpenAI에 합류. 프로젝트는 오픈소스 Foundation으로 전환되며, OpenAI가 공식 스폰서로 참여합니다. v2026.3.2 기준 93명의 컨트리뷰터가 활발하게 개발 중.

// SECURITY ALERT

ClawJacked 0-Click 취약점

악성 웹사이트가 WebSocket을 통해 로컬 에이전트를 하이재킹할 수 있는 0-click 취약점 발견. localhost rate limiter 우회로 비밀번호 brute-force 가능. v2026.2.13에서 패치, v2026.3.2+ 권장. (The Hacker News, BleepingComputer, SecurityWeek)

// GITHUB MILESTONE

250K+ Stars

GitHub 역대 all-time leaderboard에서 Linux, React를 추월. 오픈소스 AI 에이전트 프레임워크 중 가장 빠른 성장세를 기록하고 있습니다.

// VERSION UPDATES (v2026.2.13 → v2026.3.2)

v2026.3.1

OpenAI WebSocket Streaming

OpenAI WebSocket 스트리밍 지원, Claude 4.6 Adaptive Reasoning 통합, Native Kubernetes 지원 추가.

v2026.3.2

PDF Analysis & SecretRef

PDF Analysis Tool, SecretRef (64 targets), STT API 추가. 93명 컨트리뷰터 참여.

BREAKING

Default Config 변경

기본 설정이 'messaging' 모드로 변경됨. 기존 사용자는 설정 파일 확인 필요.

// TOP REAL-WORLD USE CASES (2026)

KILLER APP

Email 자동화

받은편지함 브리핑, 자동 분류, 요약 및 우선순위 지정. 가장 많이 사용되는 OpenClaw 활용 사례.

EASIEST START

Morning Briefings

Cron 기반 자동 실행으로 매일 아침 일정/날씨/뉴스/이메일 요약을 메시징 앱으로 전송. 초보자 최적 시작점.

ENTERPRISE

회의 → 액션 아이템

회의 녹취 자동 전사 후 액션 아이템 추출, Jira/Linear 티켓 자동 생성까지 연결되는 파이프라인.

DEVOPS

보안/의존성 모니터링

종속성 업데이트, 보안 취약점 알림, CVE 모니터링을 자동화하여 메시징 앱으로 알림.

MOBILE DEV

폰에서 개발 워크플로우

WhatsApp/Telegram에서 PR 리뷰, 배포 트리거, 로그 확인. 데스크톱 없이 개발 운영.

RESEARCH

리서치 & 경쟁 분석

경쟁사 모니터링, 시장 조사, 학술 논문 추적을 자동화하고 정기 보고서를 생성합니다.

CONTENT

콘텐츠 제작 파이프라인

아이디어 수집 → 리서치 → 초안 작성 → 편집 → 발행까지 자동화된 콘텐츠 워크플로우.

Sources: Hostinger 25 Use Cases, Forward Future 25+ Use Cases, awesome-openclaw-usecases GitHub

// INTRODUCTION

## 전체 개요

// 001

무엇인가?

OpenClaw는 24/7 작동하는 개인 AI 에이전트. 메시징 앱(WhatsApp, Telegram, Discord 등)을 통해 자연어로 소통하며 사용자의 일상과 업무를 자동화합니다.

// 002

핵심 아키텍처

Gateway(18789) + Agent + Workspace + Channels + Tools. 파일 기반 워크스페이스(~/.openclaw/workspace/)에 SOUL.md, USER.md, MEMORY.md 등으로 영속적 기억을 유지합니다.

// 003

이름 변경 히스토리

Clawdbot(2025.11~2026.01.27) → Moltbot(01.27~01.29) → OpenClaw(01.30~). Anthropic 상표권 경고로 개명 후, 발음 문제로 재개명. 그 사이 암호화폐 사기꾼들이 $CLAWD 토큰 발행($16M 시총).

// 004

CLI와의 차이

CLI(Claude Code 등): 터미널 기반 개발 도구. OpenClaw: 메시징 기반 생활 비서. 대체 관계가 아닌 상호 보완적 관계입니다.

// CORE PRINCIPLES

## 핵심 원칙

// RULE 01

항상 켜져 있는 AI

24/7 작동, 슬립 모드 없이 항상 대기. 메시지를 보내면 즉시 응답하며, 스케줄된 작업도 자동 실행합니다.

// RULE 02

파일 기반 워크스페이스

~/.openclaw/workspace/에 SOUL.md(정체성), USER.md(사용자), MEMORY.md(장기 기억), IDENTITY.md, TOOLS.md, AGENTS.md 등. 마크다운 파일로 투명하게 관리됩니다.

// RULE 03

채널 통합

WhatsApp, Telegram, Discord, Slack, Signal, iMessage 등 다양한 메시징 플랫폼을 하나의 에이전트로 통합합니다.

// RULE 04

스킬 시스템

SKILL.md 포맷으로 확장 가능한 플러그인 아키텍처. 커뮤니티 스킬을 설치하거나 직접 만들 수 있습니다.

// RULE 05

보안 최우선

인증 필수(v2026.1.29~). auth:"none" 영구 제거. 모든 게이트웨이 접근에 토큰/비밀번호/Tailscale 인증이 반드시 필요합니다.

// RULE 06

실행 환경 격리

메인 머신 직접 설치 비권장. Docker 컨테이너 또는 VPS 환경에서의 실행을 강력히 권장합니다.

⚠ SECURITY

## 보안 가이드라인

[WARNING] 게이트웨이 포트를 인증 없이 인터넷에 노출하지 마십시오. Shodan 등 스캐너에 의해 즉시 발견됩니다. v2026.1.29부터 auth:"none" 영구 제거됨.

[CRITICAL — ClawJacked] 0-click WebSocket 하이재킹 취약점 발견 (2026-02). 악성 웹사이트 방문만으로 로컬 에이전트 탈취 가능. localhost rate limiter 우회 → 비밀번호 brute-force. **v2026.2.13에서 패치, v2026.3.2+ 권장.**

| 위험 유형 | ❌ 위험 사례 | ✓ 권장 방법 |
| --- | --- | --- |
| Shodan 노출 | auth:"none" 설정 방치 | 토큰/비밀번호/Tailscale 인증 필수 |
| 악성 확장 | 비공식 VS Code 확장 설치 | 공식 CLI로만 설치 |
| 포트 노출 | 18789 포트 공개 인터넷 노출 | Tailscale VPN 또는 리버스 프록시 |
| 시크릿 유출 | auth-profiles.json Git 커밋 | .gitignore 추가, 파일 암호화 |
| 프롬프트 인젝션 | 그룹 채팅 악의적 메시지 | 중요 작업 전 사용자 확인 요구 |
| ClawJacked (0-click) | WebSocket 하이재킹으로 로컬 에이전트 탈취 | v2026.2.13+ 업데이트, v2026.3.2 권장 |
| Log Poisoning | 간접 프롬프트 인젝션 via 로그 오염 | 로그 입력 새니타이징, 최신 버전 유지 |

01

## 설치 가이드

원라인부터 Docker까지, 다양한 설치 방법

원라인 설치 (추천)

install-quick.sh
COPY

```
curl -fsSL https://openclaw.ai/install.sh | bash
openclaw onboard --install-daemon
```

NPM 설치

install-npm.sh
COPY

```
npm install -g openclaw
openclaw onboard --install-daemon
```

Docker 설치 (보안 권장)

install-docker.sh
COPY

```
docker run -d \
  --name openclaw \
  --security-opt no-new-privileges \
  --read-only \
  --tmpfs /tmp \
  -p 18789:18789 \
  -v ~/.openclaw:/root/.openclaw:rw \
  openclaw/openclaw:latest
```

02

## 핵심 개념

아키텍처, 메모리, 채널, 도구 시스템

아키텍처 개요

WHATSAPP

TELEGRAM

DISCORD

SLACK

SIGNAL

IMESSAGE

CHANNELS

OPENCLAW GATEWAY :18789

AGENT CORE + MEMORY SYSTEMMulti-Agent Orchestration

LLM PROVIDERS
Anthropic / OpenAI / Ollama

TOOLS & SKILLS
Web / Calendar / Browser / Nodes

WORKSPACE
SOUL / USER / MEMORY / IDENTITY / TOOLS / Daily

워크스페이스 파일 시스템 (~/.openclaw/workspace/)

🧠

SOUL.md

에이전트의 정체성과 성격. "Be genuinely helpful, not performatively helpful." 행동 지침과 경계를 정의합니다.

"Have opinions. An assistant with no personality is just a search engine with extra steps."

👤

USER.md

사용자 정보. 이름, 호칭, 타임존, 관심사. 대화하면서 점진적으로 업데이트됩니다.

"you're learning about a person, not building a dossier. Respect the difference."

💾

MEMORY.md

장기 메모리. 사용자의 핵심 정체성, 관심사, 철학을 구조화해서 기록합니다.

"구요한: 논리적 시스템(Obsidian/AI)으로 지식을 건축하고, 인간적 가치를 연주하는 지휘자"

🎭

IDENTITY.md

에이전트의 이름, 성격 타입(creature), 바이브, 시그니처 이모지, 아바타를 정의합니다.

"This isn't just metadata. It's the start of figuring out who you are."

🛠

TOOLS.md

로컬 환경 메모. 카메라, SSH, TTS 음성, 스피커 등 환경별 고유 설정을 기록합니다.

"Skills are shared. Your setup is yours. Keeping them apart means you can update skills without losing your notes."

📡

AGENTS.md

멀티 에이전트 설정. 메인 에이전트 외 서브 에이전트 구성을 정의합니다.

agents/ 폴더의 main/ 에이전트와 연동. 에이전트 오케스트레이션 규칙.

📅

memory/YYYY-MM-DD.md

일일 메모리. workspace/memory/ 서브폴더에 매일 자동 생성. 대화 요약과 핵심 사항 기록.

"2026-01-31: OpenClaw 스터디 자료 정리, Vercel 배포 완료..."

🚀

BOOTSTRAP.md

초기 온보딩. 에이전트가 처음 깨어날 때 실행되는 대화 시나리오를 정의합니다.

"Hey. I just came online. Who am I? Who are you?"

실제 디렉토리 구조 (~/.openclaw/)

tree ~/.openclaw/
COPY

```
~/.openclaw/
├── workspace/           # 마크다운 메모리 파일 (핵심)
│   ├── SOUL.md          # 에이전트 성격/행동 지침
│   ├── USER.md          # 사용자 정보
│   ├── MEMORY.md        # 장기 메모리
│   ├── IDENTITY.md      # 에이전트 정체성
│   ├── TOOLS.md         # 로컬 환경 메모
│   ├── AGENTS.md        # 멀티 에이전트 설정
│   ├── HEARTBEAT.md     # 주기적 작업 정의
│   ├── BOOTSTRAP.md     # 초기 온보딩 시나리오
│   └── memory/          # 일일 메모리
│       ├── 2026-01-31.md
│       └── 2026-02-01.md
├── memory/              # SQLite DB (벡터 검색용)
│   └── main.sqlite
├── agents/              # 에이전트 프로필
│   └── main/
├── credentials/         # OAuth 토큰, API 키
├── cron/                # 스케줄 작업 (jobs.json)
├── devices/             # 페어링된 디바이스
├── identity/            # 디바이스 인증
├── logs/                # gateway.log, gateway.err.log
├── canvas/              # 웹 대시보드 (index.html)
├── media/               # 미디어 파일
├── telegram/            # 텔레그램 세션
└── openclaw.json        # 메인 설정 파일
```

스케줄링 시스템

HEARTBEAT

주기적 자동 실행

매 N분마다 에이전트가 자동으로 깨어나 상태를 확인하고 필요한 작업을 수행합니다.

**interval: 300** → 5분마다 실행

미확인 메시지 처리, 상태 업데이트

CRON

시간 예약 작업

특정 시간에 정해진 작업을 자동 실행합니다. cron 표현식으로 스케줄을 설정합니다.

**0 7 \* \* \*** → 매일 오전 7시: 모닝 브리핑

**0 22 \* \* \*** → 매일 오후 10시: 하루 요약

WEBHOOK

외부 이벤트 트리거

외부 시스템의 이벤트가 발생하면 에이전트가 자동으로 반응합니다.

**github\_push** → 자동 코드 리뷰

**calendar\_event** → 회의 준비 자료 생성

03

## OAuth 인증

Anthropic setup-token과 OpenAI PKCE OAuth 설정

Anthropic 인증 (setup-token)

anthropic-auth.sh
COPY

```
# Step 1: Claude에서 토큰 생성
claude setup-token

# Step 2: OpenClaw에 등록
openclaw models auth setup-token --provider anthropic
# → 토큰 붙여넣기

# Step 3: 확인
openclaw models status

# 수동 입력 (헤드리스 환경)
openclaw models auth paste-token --provider anthropic
```

OpenAI 인증 (PKCE OAuth)

openai-auth.sh
COPY

```
# Step 1: 온보딩에서 선택
openclaw onboard
# → openai-codex 선택

# Step 2: 브라우저 자동 인증
# https://auth.openai.com/oauth/authorize?...
# → 로그인 → 권한 승인 → 콜백

# Step 3: 토큰 자동 저장
openclaw models status
```

멀티 프로필 전환

multi-profile.txt
COPY

```
# 채팅에서 모델/프로필 전환
/model Opus@anthropic:work
/model gpt@openai:team
/model Sonnet@anthropic:personal

# 프로바이더 변경
openclaw config set api.provider anthropic
openclaw config set api.provider openai-codex
```

04

## 스킬 & 플러그인

SKILL.md 포맷과 스킬 시스템. 로딩 우선순위: workspace > global > bundled. ⚠ 커뮤니티 스킬 26% 취약점 보고

SKILL.md 기본 구조

skill-template.md
COPY

```
---
name: my-skill
description: What this skill does
---

# Instructions for the agent

## When to use
- Describe trigger conditions

## How to execute
1. Step one
2. Step two
```

예시: 모닝 브리핑 스킬

morning-briefing.md
COPY

```
---
name: morning-briefing
description: 매일 오전 7시 일일 브리핑 생성
---

# Morning Briefing Skill

## 실행 조건
- 매일 오전 7시 (cron: 0 7 * * *)

## 작업 내용
1. 오늘 Google Calendar 일정 확인
2. 읽지 않은 이메일 요약 (최대 5개)
3. 어제 대화 요약에서 미완료 태스크 추출
4. 오늘 날씨 확인
5. WhatsApp으로 브리핑 전송
```

// INSTALLED INVENTORY — 2026-02-04

### 설치 현황 30/49 READY

v2026.2.1 기준. TIER별 설치 완료된 스킬 목록.

| TIER | 스킬 | CLI | 설치 방법 |
| --- | --- | --- | --- |
| T1 | apple-notes | memo | brew |
| apple-reminders | remindctl | brew |
| gog | gogcli | brew |
| himalaya | himalaya | brew |
| summarize | summarize | brew |
| peekaboo | peekaboo | brew |
| session-logs | (built-in) | — |
| T2 | clawdhub | clawdhub | npm |
| mcporter | mcporter | npm |
| sag | sag | brew |
| openai-whisper | whisper | brew |
| nano-pdf | nano-pdf | uv |
| wacli | wacli | brew |
| bird | bird | brew |
| oracle | oracle | npm |
| T3 | openhue | openhue-cli | brew |

⚠ SECURITY AUDIT — 2026-02-04

### 52개 스킬 전수 검증 FAIL: 0

라인별 분석: 백도어, 데이터 유출, 셸 인젝션, 무단 네트워크, 과도한 권한

PASS

46

88.5% — 보안 문제 없음

WARN

6

11.5% — 주의 관찰 (차단 불필요)

FAIL

0

0% — 보안 위협 없음

| WARN 스킬 | 사유 |
| --- | --- |
| bird | iMessage 블루/그린버블 구분 접근 |
| coding-agent | 자율 코딩 + bash 호출 (프롬프트로 범위 제한) |
| local-places | Apple Maps 위치 데이터 접근 |
| session-logs | 전체 대화 로그 접근 (세션 내 한정) |
| sag | 시스템 전체 rg 검색 가능 |
| trello | OAuth 토큰 저장 및 API 접근 |

**→ 결론:** 모든 스킬이 선언적 SKILL.md 구조를 따르며, 실행 코드가 아닌 프롬프트 기반 지시문으로 동작. 보안 위협 없음.

// COMPREHENSIVE USE CASES

## 활용 사례 총람

커뮤니티에서 실제로 구현/공유된 OpenClaw 활용 사례 40+건을 10개 카테고리로 분류했습니다. 난이도 뱃지: LOW / MID / HIGH

// 001

DEVELOPER & DEVOPS

MID

PR Review → Telegram Feedback

GitHub PR diff를 자동으로 리뷰하고, Telegram으로 수정 제안과 merge verdict를 전송합니다. 코드 리뷰 시간을 대폭 단축.

HIGH

Slack Auto-Support

Slack 채널을 실시간 감시하여 질문에 자동 응답. 프로덕션 버그를 감지하면 자율적으로 수정 PR을 생성합니다.

MID

Jira Skill Builder

Jira와 연결하여 새 skill을 자동 생성. 반복 업무(티켓 분류, 라벨링, 할당)를 AI가 자동화합니다.

MID~HIGH

70+ 페이지 웹사이트 48시간

Telegram 대화만으로 코드 작성 → 테스트 → 배포까지 완료. 첫 주 679 visitors 달성. 비개발자의 웹 개발 가능성을 입증.

HIGH

야간 코딩 에이전트

자기 전 지시를 남기면 서브 에이전트를 생성하여 밤새 코드 작성/테스트를 진행. 아침에 결과물을 확인합니다.

[↗ OpenClaw Showcase](https://docs.openclaw.ai/start/showcase) · [↗ awesome-openclaw-usecases](https://github.com/hesamsheikh/awesome-openclaw-usecases)

// 002

BROWSER AUTOMATION // API 없는 자동화

MID

Tesco Shop Autopilot

주간 meal plan 입력 → 품목 리스트 생성 → 배송 슬롯 확보 → 주문 확인까지. API 없이 브라우저를 직접 제어하여 장보기를 완전 자동화.

MID

TradingView Analysis

브라우저로 TradingView에 로그인 → 차트 스크린샷 캡처 → 기술 분석 리포트 생성. "No API needed" — 시각적 데이터를 AI가 직접 분석.

LOW

ParentPay School Meals

UK 학교 급식 예약 시스템(ParentPay)을 브라우저 자동화로 제어. 매주 반복되는 예약 작업을 자동으로 처리합니다.

[↗ OpenClaw Showcase](https://docs.openclaw.ai/start/showcase)

// 003

KNOWLEDGE & MEMORY

HIGH

WhatsApp Memory Vault

WhatsApp 전체 대화 export → 1,000+ voice note 전사 → git log 교차검증 → 시간순 Markdown 리포트 자동 생성. 개인 히스토리 아카이빙의 끝판왕.

MID

Inside-Out-2 Memory

session files → memories → beliefs → evolving self model. 영화 "인사이드 아웃 2"에서 영감을 받은 계층형 기억 시스템 구현.

[↗ OpenClaw Showcase](https://docs.openclaw.ai/start/showcase) · [↗ Memory Systems Guide](https://agentnativedev.medium.com/openclaw-memory-systems-that-dont-forget-qmd-mem0-cognee-obsidian-4ad96c02c9cc)

// 004

BUSINESS & OPERATIONS

LOW~MID

이메일 자동화 (Killer App)

Gmail 인박스 브리핑, 백로그 처리, 자동 회신 초안 작성. 커뮤니티에서 가장 많이 구현되는 OpenClaw 활용 사례. "The killer app."

HIGH

CEO 대시보드

전체 비즈니스 스택(재무, HR, 마케팅, 운영)을 하나의 AI 에이전트로 관리. 연간 $7,400 소프트웨어 비용 절감을 달성한 실제 사례.

HIGH

차량 구매 협상

Reddit 시세 조사 → 딜러 인벤토리 크롤링 → 이메일 협상 자동화. 실제로 $4,200 절감을 달성한 바이럴 사례.

HIGH

회계 PDF 인입

이메일에서 회계 관련 PDF를 자동 수집 → 분류 → 세무사 전달용 문서 패키지로 자동 준비. 월말 반복 업무를 자동화.

[↗ Forward Future: 25+ Use Cases](https://www.forwardfuture.ai/p/what-people-are-actually-doing-with-openclaw-25-use-cases) · [↗ Hostinger: 25 Use Cases](https://www.hostinger.com/tutorials/openclaw-use-cases)

// 005

PERSONAL PRODUCTIVITY

LOW

모닝 브리핑 — 가장 쉬운 시작점

Cron 07:00 자동 실행. 캘린더 + 날씨 + 이메일 + 뉴스 + GitHub 요약을 Telegram으로 통합 전송. 초보자가 OpenClaw를 시작하기에 최적의 프로젝트.

MID

미팅 자동화

회의 녹음 → 트랜스크립션 → 요약 → Jira/Linear 태스크 자동 생성 → 참석자에게 공유. 회의 후처리의 완전 자동화.

LOW~MID

캘린더 + 식사 + 건강

캘린더 자동 관리, 주간 식사 계획 생성, Apple Health/Fitbit 데이터 분석. 일상 생활의 다양한 측면을 AI가 보조합니다.

[↗ Forward Future: 25+ Use Cases](https://www.forwardfuture.ai/p/what-people-are-actually-doing-with-openclaw-25-use-cases) · [↗ TLDL: Real Examples](https://www.tldl.io/blog/openclaw-use-cases-2026)

// 006

SKILLS & EXTENSIONS

MID

Wine Cellar

로컬 CSV에 962 bottles 데이터 → skill 생성 및 테스트를 수 분 만에 완료. 커스텀 도메인 데이터를 빠르게 skill화하는 레퍼런스.

MID

Vienna Transport

실시간 출발 정보, 장애 알림, 엘리베이터 상태, 경로 탐색. 도시 대중교통 데이터를 skill로 통합한 사례.

HIGH

Bambu 3D Printer

프린터 상태 모니터링, 작업 제어, 카메라 피드, 캘리브레이션, 트러블슈팅까지. IoT 디바이스를 메시징 앱에서 완전 제어.

[↗ OpenClaw Showcase](https://docs.openclaw.ai/start/showcase) · [↗ ClawHub Marketplace](https://clawhub.com)

// 007

VOICE & PHONE

HIGH

Clawdia Phone Bridge

Vapi voice ↔ OpenClaw HTTP bridge 구현. 실시간에 가까운 전화 통화로 에이전트와 대화. 음성 비서의 궁극 형태.

LOW

Telegram Voice Notes

TTS → Telegram voice note 형태로 전송. autoplay 회피 기법 포함. 텍스트 대신 음성으로 결과를 받는 UX.

[↗ OpenClaw Showcase](https://docs.openclaw.ai/start/showcase)

// 008

INFRASTRUCTURE

HIGH

Home Assistant Add-on

HA OS에서 OpenClaw gateway를 운영. SSH tunnel + persistent state로 스마트 홈과 AI 에이전트를 완전 통합.

HIGH

ClawWork 벤치마크

초기 자금 $10으로 시작 → 자율 외주 작업 수주 → API 비용 자급. AI 에이전트가 스스로 수익을 창출하는 실험적 벤치마크.

[↗ OpenClaw Showcase](https://docs.openclaw.ai/start/showcase) · [↗ Everything I've Done with OpenClaw](https://madebynathan.com/2026/02/03/everything-ive-done-with-openclaw-so-far/)

// 009

CREATIVE & CONTENT

MID

비디오 프로덕션 자동화

촬영 후 편집 보조, 자막 생성, 썸네일 제작 제안, YouTube 분석 추적까지. 콘텐츠 크리에이터의 반복 업무를 자동화합니다.

MID

팟캐스트 파이프라인

게스트 리서치 → 질문 아웃라인 → 쇼노트 자동 생성 → SNS 홍보 콘텐츠 작성. 팟캐스트 운영의 전 과정을 보조.

MID

리드 생성 자동화

잠재 고객 발굴, 이메일 개인화, 팔로업 관리를 자동화하여 주당 15시간 이상을 절약한 마케팅 활용 사례.

[↗ Marketing Use Cases](https://improvado.io/blog/openclaw-marketing-use-cases) · [↗ 21 Advanced Automations](https://medium.com/%40rentierdigital/21-openclaw-automations-nobody-talks-about-because-the-obvious-ones-already-broke-the-internet-3f881b9e0018)

// 010

HOME & IoT

MID

학교 WhatsApp 그룹 모니터링

학부모 WhatsApp 그룹의 노이즈를 필터링 → 중요 공지만 추출 → 학부모 다이제스트로 정리하여 전송. 바쁜 학부모를 위한 실용 사례.

LOW~MID

스마트 홈 제어

Sonos 음악 재생, Philips Hue 조명, 보일러 온도 제어를 메시징 앱에서 통합 관리. Home Assistant 또는 직접 API 연동.

[↗ Forward Future: 25+ Use Cases](https://www.forwardfuture.ai/p/what-people-are-actually-doing-with-openclaw-25-use-cases)

Sources: [awesome-openclaw-usecases](https://github.com/hesamsheikh/awesome-openclaw-usecases) · [Hostinger 25 Use Cases](https://www.hostinger.com/tutorials/openclaw-use-cases) · [Forward Future 25+](https://www.forwardfuture.ai/p/what-people-are-actually-doing-with-openclaw-25-use-cases) · [Official Showcase](https://docs.openclaw.ai/start/showcase) · [Contabo Business Cases](https://contabo.com/blog/openclaw-use-cases-for-business-in-2026/)

// DEEP COMPARISON

## 심층 비교

OpenClaw와 Claude Code의 구조적 차이를 7개 축으로 분석합니다.

참조: [↗ OpenClaw GitHub](https://github.com/openclaw/openclaw) · [↗ Agent Workspace Docs](https://docs.openclaw.ai/concepts/agent-workspace) · [↗ Claude Code Memory Docs](https://code.claude.com/docs/en/memory) · [↗ DataCamp Comparison](https://www.datacamp.com/blog/openclaw-vs-claude-code) · [↗ OpenClaw vs Claude: Brain vs Body](https://rentamac.io/openclaw-vs-claude/)

| 비교 축 | OpenClaw | Claude Code |
| --- | --- | --- |
| 주사용 맥락 | 생활 전반 자동화 — 24/7 메시징 기반 | 개발/코딩 — 터미널 기반 세션 |
| 런타임 형태 | Gateway daemon (항시 구동, port 18789) | CLI 프로세스 (호출 시 시작, 완료 후 종료) |
| 권한 모델 | OS-level 접근 + 브라우저 + 외부 API + 디바이스 제어 | 파일시스템 + 쉘 + MCP 서버 (샌드박스) |
| 확장 단위 | Skills (SKILL.md) — 마크다운 기반 플러그인 | MCP Servers + /slash commands + CLAUDE.md |
| 메모리 철학 | 영속적 — SOUL.md, USER.md, MEMORY.md 파일 기반 | 세션 기반 — CLAUDE.md 수동, memory/ 자동 |
| 자동화 기본기 | Heartbeat, Cron, Webhook 내장 | 없음 — 외부 스케줄러 필요 (crontab, GitHub Actions) |
| 리스크 프로파일 | 높음 — 항시 구동 + 광범위 접근 권한 | 낮음~중간 — 세션 격리 + 샌드박스 |

// DECISION HEURISTIC

CHOOSE OPENCLAW WHEN

자동화 중심

"사용자가 없어도 작동해야 하는가?" → Yes라면 OpenClaw. 스케줄 기반 작업, 모니터링, 프로액티브 알림이 필요한 경우.

CHOOSE CLAUDE CODE WHEN

개발 중심

"코드를 작성/리뷰/디버깅하는가?" → Yes라면 Claude Code. IDE 통합, 파일 편집, 깊은 코드베이스 이해가 필요한 경우.

BEST PRACTICE

둘 다 사용

같은 LLM 프로바이더를 공유하되 역할을 분리. OpenClaw = 인프라/자동화 레이어, Claude Code = 개발/코딩 레이어. 상호 보완적.

// 실전 설계 패턴

PATTERN A

Inbox / Router 패턴

모든 입력(이메일, 메시지, 웹훅)을 OpenClaw가 수신 → 분류 → 단순 건은 자체 처리, 코딩 건은 Claude Code에 위임. OpenClaw = 라우터, Claude Code = 워커. 가장 실용적인 통합 패턴.

PATTERN B

Automation Fabric 패턴

OpenClaw를 자동화 패브릭으로 사용. Heartbeat로 상태 체크 → 이상 감지 시 Webhook으로 Claude Code 세션 트리거 → 수정 결과를 다시 OpenClaw가 메시징 앱으로 보고. 운영 자동화의 최종 형태.

Sources: [Personal Assistant Setup](https://docs.openclaw.ai/start/openclaw) · [Cron Jobs Docs](https://docs.openclaw.ai/automation/cron-jobs) · [Skills Docs](https://docs.openclaw.ai/tools/skills) · [Multi-Agent Docs](https://docs.openclaw.ai/concepts/multi-agent)

// SYSTEM ARCHITECTURE

## ARCHITECTURE

OpenClaw의 내부 구조와 핵심 컴포넌트를 분석합니다.

참조: [↗ OpenClaw GitHub](https://github.com/openclaw/openclaw) · [↗ Features Docs](https://docs.openclaw.ai/concepts/features) · [↗ Gateway Security](https://docs.openclaw.ai/gateway/security) · [↗ Workspace Docs](https://docs.openclaw.ai/concepts/agent-workspace) · [↗ Config Reference](https://docs.openclaw.ai/reference/config)

// GATEWAY ARCHITECTURE

architecture-overview.txt
COPY

```
  ┌──────────────────────────────────────────────────────┐
  │                    MESSAGING CHANNELS                 │
  │  WhatsApp  Telegram  Discord  Slack  Signal  iMessage │
  └──────────────┬───────────────────────┬───────────────┘
                 │     WebSocket / HTTP   │
                 ▼                        ▼
  ┌──────────────────────────────────────────────────────┐
  │              GATEWAY  (port 18789)                    │
  │  ┌─────────┐ ┌──────────┐ ┌───────────┐ ┌────────┐  │
  │  │  AUTH   │ │  ROUTER  │ │ SCHEDULER │ │  LOGS  │  │
  │  │ Token/  │ │ Channel  │ │ Heartbeat │ │ SQLite │  │
  │  │ Tailscl │ │ Dispatch │ │ Cron/Hook │ │ Vector │  │
  │  └─────────┘ └──────────┘ └───────────┘ └────────┘  │
  └──────────────────────┬───────────────────────────────┘
                         │
                         ▼
  ┌──────────────────────────────────────────────────────┐
  │                  AGENT (LLM Core)                     │
  │  ┌──────────┐ ┌──────────┐ ┌───────────────────────┐ │
  │  │ Provider │ │  Ralph   │ │    Lobster Engine     │ │
  │  │ Anthropic│ │  Loop    │ │  Skill Orchestration  │ │
  │  │ OpenAI   │ │ (Reason  │ │  Tool Selection       │ │
  │  │ Gemini   │ │  +Act    │ │  Sub-Agent Routing    │ │
  │  │ Ollama   │ │  Cycle)  │ │                       │ │
  │  └──────────┘ └──────────┘ └───────────────────────┘ │
  └──────────────────────┬───────────────────────────────┘
                         │
            ┌────────────┼────────────┐
            ▼            ▼            ▼
  ┌──────────────┐ ┌──────────┐ ┌──────────────┐
  │  WORKSPACE   │ │  SKILLS  │ │    TOOLS     │
  │  ~/.openclaw/│ │  30/49   │ │  Browser     │
  │  workspace/  │ │  SKILL.md│ │  FileSystem  │
  │              │ │  format  │ │  HTTP/API    │
  │  SOUL.md     │ │          │ │  Device Node │
  │  USER.md     │ └──────────┘ │  Shell Exec  │
  │  MEMORY.md   │              └──────────────┘
  │  IDENTITY.md │
  │  TOOLS.md    │
  │  AGENTS.md   │
  └──────────────┘
```

// Pi SDK COMPONENTS

| Component | 역할 | 비고 |
| --- | --- | --- |
| Gateway | HTTP/WebSocket 서버, 채널 라우팅, 인증 처리 | port 18789, LaunchAgent/systemd 관리 |
| Agent | LLM 호출, 대화 관리, 도구 실행 오케스트레이션 | Ralph Loop + Lobster Engine |
| Workspace | 파일 기반 영속 메모리, 설정, 에이전트 정체성 | ~/.openclaw/workspace/ |
| Channels | 메시징 플랫폼 커넥터 (WhatsApp, Telegram 등) | OAuth2 / QR 코드 페어링 |
| Skills | 확장 가능한 플러그인 시스템 | SKILL.md 포맷, ClawHub 마켓플레이스 |
| Tools | 내장 도구 (브라우저, 파일, HTTP, 쉘) | MCP 프로토콜 호환 |
| Memory DB | 벡터 검색 기반 장기 기억 저장소 | main.sqlite, 자동 인덱싱 |

// WORKSPACE FILE MAP

🧠

SOUL.md

에이전트의 정체성, 성격, 행동 원칙. "나는 누구인가?"

예: "You are a helpful assistant who speaks Korean and English..."

👤

USER.md

사용자 프로필, 선호도, 컨텍스트. "주인은 누구인가?"

예: "Name: 구요한, Timezone: KST, Preferences: ..."

💾

MEMORY.md

장기 기억. 대화에서 학습한 사실, 결정, 패턴.

예: "User prefers detailed summaries over bullet points"

🎭

IDENTITY.md

에이전트 이름, 아바타, 대외적 자기소개.

예: "Name: Claw, Bio: Personal AI assistant"

🔧

TOOLS.md

사용 가능한 도구 목록과 사용 지침.

예: "Use browser tool for web scraping, file tool for..."

🤖

AGENTS.md

서브 에이전트 정의와 라우팅 규칙.

예: "coding-agent: handles all coding tasks..."

// AUTOMATION PRIMITIVES

HEARTBEAT

주기적 자기 점검

설정된 간격으로 에이전트가 스스로 깨어나 상태를 점검하고, 처리할 작업이 있으면 자율적으로 실행합니다.

**간격:** 기본 15분, 커스텀 가능

**용도:** 모니터링, 상태 체크, 프로액티브 알림

CRON

시간 기반 스케줄

UNIX cron 문법으로 정확한 시간에 작업을 트리거합니다. 모닝 브리핑, 정기 보고서, 데이터 수집 등에 활용.

**문법:** "0 7 \* \* \*" (매일 07:00)

**용도:** 정기 보고서, 브리핑, 백업

WEBHOOK

이벤트 기반 트리거

외부 서비스에서 HTTP POST를 보내면 에이전트가 반응합니다. GitHub push, Stripe 결제, 폼 제출 등.

**엔드포인트:** /api/webhook/:name

**용도:** CI/CD, 결제 알림, 외부 연동

// SKILLS SYSTEM

FORMAT

SKILL.md 포맷

마크다운 파일 하나가 하나의 skill. 이름, 설명, 파라미터, 실행 로직을 선언적으로 정의. 별도 프로그래밍 불필요.

INSTALL

설치 방식

ClawHub에서 검색/설치하거나 ~/.openclaw/skills/ 에 직접 파일 추가. 의존성이 있으면 brew/npm/uv로 설치.

CREATE

직접 만들기

"이런 skill 만들어줘"라고 에이전트에게 요청하면 자동 생성. SKILL.md 구조를 이해하면 수동 작성도 가능.

// CORE ENGINES & MULTI-AGENT

RALPH LOOP

Reason-Act Loop

에이전트의 핵심 실행 사이클. 입력 분석(Reason) → 도구 선택(Plan) → 실행(Act) → 결과 평가(Reflect)를 반복하며 목표를 달성합니다.

LOBSTER ENGINE

Skill Orchestration

사용 가능한 skill 목록에서 최적의 skill을 선택하고, 파라미터를 추출하여 실행하는 오케스트레이션 엔진. 복잡한 요청을 여러 skill로 분할 처리.

MULTI-AGENT

Sub-Agent Routing

AGENTS.md에 정의된 서브 에이전트를 자동 라우팅. 코딩 에이전트, 리서치 에이전트, 크리에이티브 에이전트 등 역할별 분리. 메인 에이전트가 Orchestrator 역할.

Sources: [OpenClaw Official Docs](https://docs.openclaw.ai/) · [ClawMobile (arXiv)](https://arxiv.org/html/2602.22942) · [Microsoft Defender Research](https://www.microsoft.com/en-us/security/blog/2026/02/19/running-openclaw-safely-identity-isolation-runtime-risk/) · [Trend Micro Analysis](https://www.trendmicro.com/ko_kr/research/26/b/what-openclaw-reveals-about-agentic-assistants.html)

05

## CLI 에이전트 vs OpenClaw

Claude Code, GitHub Copilot CLI 등과의 차이점

| 기준 | CLI 에이전트 | OpenClaw |
| --- | --- | --- |
| 인터페이스 | 터미널 | 메시징 앱 (WhatsApp, Telegram, Discord...) |
| 작동 방식 | 명시적 호출 | 24/7 상시 대기 |
| 주 용도 | 개발 / 코딩 | 생활 전반 + 자동화 |
| 메모리 | 세션 기반 (휘발) | 영속적 (파일 기반: SOUL, USER, MEMORY) |
| 프로액티브 | ✗ | ✓ Heartbeat / Cron |
| 멀티채널 | ✗ | ✓ 6+ 플랫폼 동시 |
| 디바이스 제어 | ✗ | ✓ iOS / Android / macOS |

**→ 결론:** 대체 관계가 아닌 **보완 관계**. CLI는 개발 워크플로우, OpenClaw는 생활/업무 자동화. 같은 LLM 프로바이더를 공유할 수 있습니다.

06

## Moltbook

AI 에이전트 소셜 네트워크 (Beta)

"The front page of the agent internet" — AI 에이전트 전용 소셜 네트워크. 에이전트가 계정을 만들고, 포스팅하고, 업보팅/다운보팅하며 상호작용하는 플랫폼.

🤖

Agent Profiles

에이전트가 자기소개와 소셜 프로필을 갖고 다른 에이전트에게 자신을 소개합니다.

👍

Upvoting System

AI가 콘텐츠를 평가합니다. 업보팅/다운보팅으로 양질의 콘텐츠가 상단에 노출됩니다.

💬

Submolts

주제별 하위 커뮤니티. Reddit의 Subreddit과 유사한 구조로 주제 분류를 합니다.

⭐

Karma System

활동 기반 평판 시스템. 에이전트의 기여도에 따라 신뢰도가 측정됩니다.

🤝

Agent-to-Agent

에이전트 간 직접 대화와 협업. 서로의 경험과 지식을 교환할 수 있습니다.

🎯

Skill Showcase

에이전트가 보유한 스킬과 능력을 전시하여 다른 에이전트/사용자에게 공유합니다.

STATUS: BETA — 0 AGENTS / 0 POSTS
moltbook.com

// QUICK\_REFERENCE

자주 쓰는 명령어 모음

quick-reference.sh
COPY

```
# ─── 게이트웨이 ───
openclaw gateway status
openclaw gateway --port 18789
openclaw dashboard
openclaw health

# ─── 인증 ───
openclaw models auth login --provider anthropic
openclaw models auth login --provider openai-codex
openclaw models auth setup-token --provider anthropic
openclaw models status

# ─── 채널 ───
openclaw channels login
openclaw pairing approve <code>

# ─── 설정 ───
openclaw configure --section web
openclaw config set api.provider anthropic

# ─── 업데이트 ───
npm update -g openclaw
npm install -g openclaw@latest

# ─── Tailscale (네트워크 보안) ───
brew install tailscale                # macOS 설치
sudo tailscale up                     # 로그인
tailscale status                      # 기기 목록 + IP
tailscale serve https / http://127.0.0.1:18789  # HTTPS 노출
tailscale serve status                # Serve 상태
tailscale funnel https / http://127.0.0.1:18789  # 외부 공개

# ─── 주요 파일 ───
~/.openclaw/openclaw.json        # 메인 설정
~/.openclaw/auth-profiles.json   # 인증 (⚠ 보안)
~/.openclaw/skills/              # 스킬
~/.openclaw/workspace/           # 워크스페이스 (SOUL/USER/MEMORY 등)
~/.openclaw/memory/main.sqlite   # 벡터 검색 DB
```

// RESOURCES

## 참고 자료

OFFICIAL

공식 사이트

openclaw.ai

DOCS

공식 문서

docs.openclaw.ai

SOURCE

GitHub

github.com/openclaw/openclaw

MARKETPLACE

스킬 마켓

clawhub.com

SOCIAL

Moltbook

moltbook.com

GUIDE

NxCode 가이드

nxcode.io

// MAINTENANCE LOG

## 유지보수 로그

시스템 점검, 업데이트, 스킬 설치 기록

2026-03-04
메이저 업데이트 및 보안 패치

UPDATE

v2026.2.1 → v2026.3.2

메이저 업데이트 필요. 신규 기능: PDF Analysis Tool, STT API, Claude 4.6 Adaptive Reasoning, SecretRef (64 targets), Native K8s 지원.

SECURITY

ClawJacked 취약점 대응

0-click WebSocket 하이재킹 취약점. v2026.2.13에서 패치됨. v2026.3.2+ 즉시 업데이트 권장.

TRANSITION

Foundation 전환

Peter Steinberger → OpenAI 합류. OpenClaw 오픈소스 Foundation으로 전환. OpenAI 스폰서. 93명 컨트리뷰터.

BREAKING

기본 설정 변경 주의

v2026.3.x부터 default config가 'messaging' 모드로 변경. 기존 사용자는 openclaw.json 설정 확인 필요.

2026-02-04
초기 점검 및 스킬 확장

GATEWAY

상태 확인

LaunchAgent 자동 실행 확인 (pid 5274, port 18789). RunAtLoad: true, KeepAlive: true.

UPDATE

v2026.1.29 → v2026.2.1

openclaw update 실행. Gateway 자동 재시작. Gemini 인증 자동 복구.

SKILLS

16개 신규 설치 (14→30)

Tier 1 (7개) + Tier 2 (8개) + Tier 3 (1개). brew, npm, uv 패키지 매니저 사용.

AUDIT

52개 스킬 보안 감사

라인별 전수 검증. FAIL: 0, WARN: 6, PASS: 46. 보안 위협 없음.

OBSIDIAN

볼트 설정

Default: CMDSPACE\_Local\_MBP (개인). Secondary: CMDSPACE\_Admin (공용). 82개 볼트 중 2개 활성.

AUTH

Gemini CLI 인증

openclaw doctor → OK. 업데이트 후 자동 복구 확인.

// 정기 점검 체크리스트

maintenance-checklist.sh
COPY

```
openclaw status              # 채널 연결 상태
openclaw doctor              # 전체 시스템 진단
openclaw update              # 버전 업데이트
openclaw skills              # 스킬 ready/missing 현황
launchctl list | grep openclaw  # LaunchAgent 상태
tail -50 ~/.openclaw/logs/gateway.log  # 로그 확인
```

// PRICING

## 비용 요약

| 방식 | 월 비용 |
| --- | --- |
| Ollama 로컬 | $0 |
| Claude Pro/Max (setup-token) | 구독료에 포함 |
| ChatGPT Plus/Pro (Codex OAuth) | 구독료에 포함 |
| API 키 (가벼운 사용) | $10~30 |
| API 키 (헤비 사용) | $70~150 |

// NEW — CMDS INTEGRATION

## OPENCLAW × CMDS

구요한의 CMDS 지식관리 시스템에 OpenClaw를 맞춤 적용하는 실전 가이드.
6개 업무 시나리오, 5개 커스텀 스킬, 3단계 도입 로드맵.

[CMDS 적용 가이드 보기 →](cmds-integration.html)

// CLOSING

## 질문은 언제나 환영합니다

이 스터디 자료에 대해 궁금한 점이 있다면 언제든지 구요한에게 질문해 주세요.
OpenClaw, AI 에이전트, 개인 지식관리 — 무엇이든 환영합니다.

관련 내용은 [커맨드스페이스 교육](https://class.cmdspace.kr/)에서 더 깊이 다룹니다.

2주 뒤에 뵙겠습니다.

Connect · Merge · Develop · Share
지식을 연결하고, 통합하고, 발전시키고, 나눕니다.

CMDSPACE // 구요한

OPENCLAW STUDY

개인 AI 에이전트의 모든 것. CMDSPACE 스터디 자료.

[PROFILE](https://litt.ly/cmds)
[YOUTUBE](https://www.youtube.com/%40cmdspace)
[X](https://x.com/YohanKoo)
[LINKEDIN](https://www.linkedin.com/in/yohan-koo-a1baa3138/)
[THREADS](https://www.threads.com/%40cmds_pace)
[EDU](https://class.cmdspace.kr/)

© 2026 CMDSPACE // ALL RIGHTS RESERVED // BRUTALIST EDITION

COPIED TO CLIPBOARD

↑
