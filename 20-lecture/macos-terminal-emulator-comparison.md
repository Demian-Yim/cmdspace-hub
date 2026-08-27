---
title: macos-terminal-emulator-comparison
source: https://terminal.cmdspace.work/
author: 구요한 (CMDSPACE)
fetched: 2026-08-28
note: markitdown HTML→MD 자동 변환 스냅샷. 정확한 원문은 source URL 참조.
---

**Terminal Guide 2026** · 7 apps · AI agent · SSH · WSL 기준 종합 비교 · 2026-07 업데이트

![CMDSPACE](/assets/logos/cmds-logo-round.png)

# 터미널 앱 종합 비교 2026

tmux · Zellij · Herdr · Cmux · Orca · Warp · Ghostty — AI 코딩 에이전트 시대, 사용성 · 플랫폼 · SSH · WSL · API 기준으로 7종을 한눈에.

by [@YohanKoo](https://x.com/YohanKoo) · [CMDSPACE](https://litt.ly/cmds)

7

Apps

8

비교 축

3

Muxer 딥다이브

2026.07

기준

종합 비교
앱별 프로필
Muxer 3파전
플랫폼 · API
WSL 가이드
시나리오별 추천

## Master Comparison — 7 Apps

원래 조사했던 6개 앱(Cmux · Orca · Herdr · Warp · Ghostty · Zellij)에 **tmux**까지 포함해 **사용성 · 플랫폼 · AI 에이전트 · SSH · WSL · API** 중심으로 정리했습니다.

| 앱 | Type | Mac/Win/Linux/WSL | 학습 곡선 | AI Agent | SSH·Remote | API | 리소스 | Best Use (5점) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| tmux | Classic Multiplexer | ★ / ★(WSL) / ★★★ / ★★★★★ | ★★★★★ 가파름 | ★★★★★ | ★★★★★ 왕 | ★★★★★ scripting | ★★★★★ 최저 | 서버·SSH·프로덕션 5/5 |
| Zellij | Modern Multiplexer | ★★★ / ★★(WSL) / ★★★★★ / ★★★★★ | ★★★★★ discoverable | ★★★★★ | ★★★★★ | ★★★★★ WASM | ★★★★★ | 일상 workspace·plugin 4.5 |
| Herdr | Agent Multiplexer | ★★★ / ★★(beta) / ★★★★★ / ★★★★★ | ★★★★★ Agent TUI | ★★★★★ | ★★★★★ thin remote | ★★★★★ socket | ★★★★★ | AI herd·remote·WSL 5/5 |
| Cmux | GUI Agent Terminal | ★★★★★ / 개발중 / 개발중 / ★★★ | ★★★★★ GUI | ★★★★★ | ★★★★★ workspace | ★★★★★ socket+CLI | ★★★★★ | Mac AI parallel 4.5 |
| Orca | Full ADE (IDE-like) | ★★★★★ / ★★★★★ / ★★★★★ / ★★★★ | ★★★★★ Visual | ★★★★★ | ★★★★★ worktree | ★★★★★ CLI+RPC | ★★★★★ | End-to-end agent workflow 5/5 |
| Warp | AI Modern Terminal | ★★★★★ / ★★★★★ / ★★★★★ / ★★★★ | ★★★★★ Blocks+AI | ★★★★★ | ★★★★★ extension | ★★★★★ SDK | ★★★★★ | Daily + cloud + UX 4.5 |
| Ghostty | High-perf Emulator | ★★★★★ / 예정 / ★★★★★ / ★★★★ | ★★★★★ Native | ★★★★★ | ★★★★★ +ssh wrapper | ★★★★★ lib | ★★★★★ 최고 | Speed base 4/5 |

### 핵심 인사이트 (사용성 중심)

1. tmux — 배우기 어렵지만 한 번 익히면 평생

Prefix key·config가 가장 큰 단점. 하지만 어디서나 있고 가장 안정적이며 scripting 무한. agent state가 없어 AI 워크플로우에서는 Herdr/Zellij로 대체하는 추세.

2. Zellij — tmux의 "사용성 개선판"

키 힌트·floating panes·WASM으로 "현대 tmux" 느낌. WSL·서버 모두 잘 됨. tmux 사용자 70%가 "전환 후 후회 안 함" 후기.

3. Herdr — AI 에이전트 시대에 가장 특화

에이전트 상태 표시 + agents가 직접 조작 가능. WSL·remote에서 "진짜 편함". tmux처럼 가볍지만 agent-aware.

4. Cmux / Orca / Warp — GUI·IDE 계열

Mac/Windows 네이티브 강점. tmux/Zellij와 함께 쓰는 경우 많음 (예: Cmux + tmux attach).

5. Ghostty — 속도·렌더링 최고

멀티플렉서가 아니므로 Zellij/Herdr과 조합이 최강.

### 전체 순위 — AI · WSL · Remote 사용자 기준

1

**Herdr** — agent + remote

2

**Orca** — full workflow

3

**Zellij** — versatile

4

**Warp** — daily + cloud + UX

5

**Cmux** — Mac AI parallel

6

**Ghostty** — speed base

7

**tmux** — legacy · server (여전히 왕)

Insight

모든 앱이 **상호 보완적**입니다 — 로컬은 Warp/Cmux/Orca, WSL은 Herdr/Zellij, 서버는 tmux. 이렇게 섞어 쓰는 사람이 많습니다.

## 앱별 프로필 — 7 Apps

tmux Classic Multiplexer
SERVER KING

**Ubiquitous** — 거의 모든 Linux 서버에 미리 설치. detach/reattach의 원조로 SSH가 끊겨도 세션이 살아있음. `send-keys`·`new-window`로 scripting 천재, TPM으로 100+ plugin.
약점: Prefix key(Ctrl+b), discoverability 0, config 복잡, agent 상태를 눈으로 확인 불가.

극저 리소스TPM plugins[GitHub ↗](https://github.com/tmux/tmux)

Zellij Modern Multiplexer · Rust
EASY START

tmux 현대판. **키 힌트로 외울 필요 없는 discoverable UI**, floating/stacked panes, KDL layouts, WASM plugin 생태계, web client(URL 공유·multiplayer). Session resurrection으로 persistence 강력.
약점: tmux보다 리소스 약간 높음, remote마다 설치 필요.

WASM pluginsWeb client[zellij.dev ↗](https://zellij.dev)

Herdr Agent Multiplexer · Rust single binary
AI SPECIALIZED

기존 터미널 안에서 동작하는 **agent multiplexer**. 에이전트별 real PTY + 상태 UI(working·blocked·done·idle), mouse-first TUI(phone SSH OK). `--remote user@host`로 서버 실행 후 어디서나 attach.
JSON socket + CLI로 **agents가 Herdr을 직접 제어**. 약점: 순수 TUI(GUI polish 없음), Windows preview.

No account · telemetrySingle binary[herdr.dev ↗](https://herdr.dev)

Cmux GUI Agent Terminal · macOS native
MAC NATIVE

Ghostty lib 기반 Swift/AppKit 네이티브. **AI 에이전트 멀티태스킹 최적화** — vertical tabs + sidebar(git·ports·noti), agent notification rings, embedded scriptable browser(DOM snapshot·JS eval), session restore. Unix socket + CLI로 agents가 직접 조작.
약점: macOS 중심(Win/Linux 개발 중), live persistence는 tmux 조합 필요.

iOS companionEmbedded browser[cmux.com ↗](https://cmux.com)

Orca Agent Development Environment
FULL ADE

IDE-like ADE. **git worktree별 isolated agents** + 터미널(infinite splits) + built-in editor + Chromium browser(design mode) + PR diffs. SSH worktrees로 remote agents + local editor 동기화, port forwarding. 모바일 companion으로 원격 감시.
약점: 순수 터미널보다 무거움.

Mobile apporca-cli + RPC[onorca.dev ↗](https://onorca.dev)

Warp AI Modern Terminal · Rust
BEST UX

Command blocks + AI Agent Mode + file tree·editor·indexing + Oz cloud(local↔cloud handoff). SSH extension으로 **remote에서도 blocks·AI·indexing 전부 작동**. Cross-platform 완비, open-source 전환.
약점: 일부 AI·cloud 기능 account 필요.

Oz SDKTeam collab[warp.dev ↗](https://warp.dev)

Ghostty High-perf Emulator · Zig GPU
SPEED BASE

초고속·고정확성 **순수 에뮬레이터**. Native UI, Kitty protocols, `+ssh` wrapper(terminfo 자동 설치·env forwarding). libghostty로 embed 가능 — Cmux·Orca가 실제로 이 위에 지어짐.
약점: muxer 별도 필요, Windows 미지원(예정).

libghosttyKitty graphics[ghostty.org ↗](https://ghostty.org)

## 멀티플렉서 3파전 — tmux vs Zellij vs Herdr

tmux는 여전히 "서버·SSH·프로덕션의 절대 강자"지만, 현대 AI 에이전트 워크플로우에서는 **사용성**에서 많이 뒤처집니다.

| 항목 | tmux (클래식) | Zellij (현대 범용) | Herdr (에이전트 특화) | 승자 |
| --- | --- | --- | --- | --- |
| 학습 곡선 | ★★★★★ 매우 가파름 | ★★★★★ discoverable | ★★★★★ agent workflow | Zellij / Herdr |
| 일상 UX | 수동·텍스트 중심 | Floating panes·mouse·layout | Agent sidebar·mobile OK | Zellij |
| Agent / AI | ★★★★★ 수동 script | ★★★★★ plugin 확장 | ★★★★★ state + 직접 제어 | Herdr 압승 |
| Remote / SSH | ★★★★★ detach 원조 | ★★★★★ web client | ★★★★★ thin client·phone | tmux = Herdr |
| Config / Script | ★★★★★ .tmux.conf | ★★★★★ KDL + WASM | ★★★★★ JSON socket | tmux (power) |
| Plugin 생태계 | ★★★★★ TPM 100+ | ★★★★★ WASM 성장 중 | ★★★★★ CLI 중심 | tmux |
| 리소스 | ★★★★★ 극저 | ★★★★★ | ★★★★★ single binary | tmux / Herdr |
| WSL·서버 호환 | ★★★★★ 기본 설치 | ★★★★★ 설치 필요 | ★★★★★ 완벽 | tmux (ubiquitous) |
| 2026 AI workflow | 수동 hooks·script | plugin으로 어느 정도 | Built-in state + orchestration | Herdr |

### tmux 상세 — 현대 관점

**강점 (여전히 쓰는 이유)**

* **Ubiquitous** — 거의 모든 Linux 서버에 미리 설치. `apt install`조차 불필요한 경우가 많음
* **Detach/Reattach의 왕** — SSH 끊겨도 세션 유지. 프로덕션·장기 빌드의 표준
* **Scripting** — `tmux send-keys`·`new-window`·`choose-tree`로 자동화 쉬움
* **TPM** — resurrect·continuum·yank·sensible 등 100+ plugin 1초 설치

**약점 (현대 사용자들이 불편해하는 점)**

* Prefix key(Ctrl+b) — 손가락 아프고 Vim·Emacs와 충돌
* Discoverability 0 — 키를 외워야 함, 도움말 없음
* Config 복잡 — `.tmux.conf` 작성→reload 반복, 초보 포기율 높음
* Agent workflow — Claude Code 여러 개 돌릴 때 상태를 눈으로 확인 불가

> "서버 50대 관리할 때는 tmux가 아직 제일 안정적" · "로컬·AI 작업은 Zellij/Herdr로 넘어감" · "Herdr로 넘어가니 agent 상태 보는 게 너무 편해져서 tmux 돌아가기 싫음" **— 2026 사용자 후기**

### tmux → Herdr/Zellij 전환 팁

* tmux config에 `set -g prefix C-a` + mouse on 등 기본 개선
* `tmux-resurrect` + `tmux-continuum` 필수 설치
* Nested 사용 — tmux 세션 안에 Herdr/Zellij 실행하며 점진 전환
* 로컬은 Zellij/Herdr, 서버는 tmux 유지

한 줄 결론

**tmux** = 신뢰할 수 있는 만능 도구 · **Zellij** = tmux를 편하게 쓰고 싶은 사람의 업그레이드 · **Herdr** = AI 에이전트 시대의 신무기. WSL + AI 에이전트 + remote 서버 환경이면 **Herdr → Zellij → tmux** 순으로 테스트 추천.

## 플랫폼 · API · 에이전트 호환성

| 도구 | Mac | Windows | Linux | API / Programmability | Claude Code 등 호환 | 주요 Integration |
| --- | --- | --- | --- | --- | --- | --- |
| Cmux | ✅ Native 최고 | ⚠️ 개발 중 | ⚠️ 개발 중 | ★★★★★ Unix socket + CLI (pane·browser·screen 전체 제어) | ★★★★★ hooks·teams·notification rings | Embedded browser · iOS · tmux attach · OSC |
| Orca | ✅ Full | ✅ Full | ✅ Full | ★★★★★ orca-cli + RPC | ★★★★★ isolated worktree + parallel | Git worktree · editor · Chromium · Linear/PR · mobile |
| Herdr | ✅ Stable | ⚠️ Beta | ✅ Stable | ★★★★★ JSON socket + CLI (agents 직접 제어) | ★★★★★ real PTY + state detect + wait API | Any shell·TUI · clipboard sync · phone SSH |
| Warp | ✅ Full | ✅ Full | ✅ Full | ★★★★★ Oz SDK/CLI + workflows | ★★★★★ Agent Mode + remote extension | File tree · Oz cloud · blocks · team Drive |
| Ghostty | ✅ Native 최고 | ❌ 예정 | ✅ Full | ★★★★★ libghostty + AppleScript | ★★★★★ 100% 호환, 특화 없음 | Kitty protocols · +ssh · lib embed |
| Zellij | ✅ Full | ✅ WSL + preview | ✅ Full | ★★★★★ WASM plugin + KDL + CLI | ★★★★★ plugins으로 확장 | Web client · floating panes · tmux mode |
| tmux | ✅ | WSL | ✅ 기본 설치 | ★★★★★ shell scripting 무한 | ★★★★★ 수동 script 필요 | TPM · resurrect · continuum · 모든 서버 |

### API 상세 — agents가 앱을 조작하는 수준

Cmux / Herdr — 최상위

Socket으로 pane 생성·input·read·wait. Claude Code가 앱을 "remote control" 가능한 수준.

Orca

orca-cli + RPC — worktree·snapshot·browser click까지 자동화.

Warp

Oz SDK + workflows — cloud handoff·multi-agent routing.

Zellij / Ghostty

Zellij는 WASM plugin으로 UI·로직 확장. Ghostty는 libghostty(C API) — Cmux가 실제 사용 예시.

호환성 참고

모든 도구가 "any CLI agent"를 지원합니다 — Claude Code 외에 Codex·Cursor·Aider·Goose 등 동일하게 잘 됨. 특히 Cmux·Orca·Herdr는 **여러 세션을 동시에 보고 관리**하는 데 압도적.

## WSL 가이드 — Windows에서 AI 에이전트 돌리기

WSL2는 Windows에서 Linux 네이티브 환경을 제공해 에이전트 작업에 매우 강력합니다. Herdr·Zellij와 가장 잘 맞고, 서버와 거의 동일한 경험을 줍니다.

### 1. WSL 설치 (1분)

Copy

```
# PowerShell 관리자 권한으로 실행 → 재시작
wsl --install

# 세밀 설치
wsl --install -d Ubuntu
wsl --set-default-version 2
```

### 2. 기본 준비 (한 번만)

Copy

```
sudo apt update && sudo apt upgrade -y
sudo apt install -y curl git unzip build-essential

# Rust (Herdr·Zellij용)
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y

# Herdr 설치 (WSL 최적)
curl -fsSL https://herdr.dev/install.sh | sh

# Zellij 설치
cargo install zellij
```

### 3. 사례 1 — Herdr + Claude Code 병렬 (가장 추천)

Copy

```
herdr
herdr workspace create --label claude1 --cwd ~/project1
herdr pane run "claude code --model sonnet"   # 에이전트1
herdr pane run "claude code --model opus"     # 에이전트2

# 상태 모니터링 + agents가 Herdr 제어
herdr wait agent-status 1-1 --status done
```

WSL 안 persistent PTY → Windows를 꺼도 에이전트 계속 실행.

### 4. 사례 2 — Zellij layout으로 에이전트 멀티플렉싱

Copy

```
zellij --layout agents.kdl

# agents.kdl
tab name="Agents" {
  pane split_direction="vertical" {
    pane command="claude code"
    pane command="aider --model claude"
  }
}
```

### 5. Windows 네이티브 앱 연동

* **Orca Windows** — SSH worktree로 WSL 연결
* **Warp Windows** — WSL 프로필 추가, blocks·AI 기능 유지
* **Windows Terminal** — 기본 프로필을 Ubuntu로, WSL 자동 실행

### 6. 문제 해결 · 팁

Copy

```
# Virtualization 오류 → BIOS에서 Intel VT-x / AMD SVM 켜기
# 설치 0% 멈춤
wsl --install --web-download -d Ubuntu
# WSL1로 설치됨
wsl --set-version Ubuntu 2

# 메모리 제한 — C:\Users\{name}\.wslconfig
[wsl2]
memory=8GB
swap=4GB
```

한 줄 요약

**Herdr를 WSL에 설치 → `herdr` 실행 → Claude Code 여러 개 띄우기** — 2026년 현재 Windows 사용자에게 가장 강력한 워크플로우.

## 시나리오별 최종 추천

Mac 중심 + AI 병렬

**Cmux** 또는 **Orca + Ghostty**

Windows + WSL + remote 서버

**Herdr** (1순위) → **Zellij**

순수 서버 · minimal 환경

**tmux** — 여전히 왕

일상 + UX + cloud

**Warp**

최고 성능 기반

**Ghostty + Herdr** 또는 **Ghostty + Zellij**

초보자

**Zellij** 또는 **Warp**

최강 조합

**Ghostty (base) + Herdr (agent) + tmux (legacy server)**

### 멀티플렉서 선택 — 상황별

| 상황 | 추천 | 이유 |
| --- | --- | --- |
| 서버·프로덕션·minimal env | tmux | 어디서나 있고 가장 안정적 |
| AI 에이전트 여러 개 + 상태 관리 | Herdr | Built-in state + agent control |
| 예쁜 UI + layout + plugin | Zellij | 학습 쉬움 + modern feel |
| tmux + 현대 도구 혼용 | Zellij + tmux (nested) | Zellij 안에서 tmux attach 가능 |
| WSL의 Windows 사용자 | Herdr 먼저 → Zellij | WSL에서 가장 자연스럽게 동작 |

### 공식 링크

[herdr.dev](https://herdr.dev)
[zellij.dev](https://zellij.dev)
[cmux.com](https://cmux.com)
[onorca.dev](https://onorca.dev)
[warp.dev](https://warp.dev)
[ghostty.org](https://ghostty.org)
[tmux](https://github.com/tmux/tmux)

모든 정보는 2026년 7월 공식 문서·GitHub·커뮤니티·사용자 후기 기반. 대부분 무료·오픈소스(일부 Pro tier)라 바로 테스트 추천.

[CMDSPACE](https://litt.ly/cmds) · [@YohanKoo](https://x.com/YohanKoo) · [cmdspace.work](https://cmdspace.work)

Connect · Merge · Develop · Share
