---
title: talk-2026-꿈도환승-multi-agent
source: https://dream.cmdspace.work/
author: 구요한 (CMDSPACE)
fetched: 2026-08-28
note: markitdown HTML→MD 자동 변환 스냅샷. 정확한 원문은 source URL 참조.
---

[![CMDSPACE](/assets/logos/cmds-logo-round.png) CMDSPACE](#s0)

▶
◐

2026 꿈도 환승이 되나요 · Part 1

# 저는 2명입니다. 그런데 혼자 일하지 않습니다.

두 명짜리 회사가, 하네스 위에서, 서비스 함대를 만들고 다듬는 법.

CmdMDCmdTrace
cmds-sharecmds-eagle
NetHelmPlaud
+ 위키 볼트 · vault-map · omnisearch · 지식의 해상도

스크롤↓또는 발표 모드P

명제

## 작은 회사의 한계는 사람으로 늘리지 않는다. 하네스로 늘린다.

오늘의 슬로건은 "일하는 방식, AI로 환승하다". 환승의 핵심은 사람을 더 뽑는 것도, 더 빠른 도구로 갈아타는 것도 아니다. 세 층으로 연다 — 하네스, 함대, 그 너머.

① 하네스 — 볼트 + 위키 + 스키마
② 함대 — 앱·서비스
③ 너머 — 연구·엣지

ACT 1 · 하네스

## 바닥엔 두 개의 볼트가 있다.

메인 볼트 · 마더십

### 10,000+ 노트 = 기억

3년 넘게 쌓아온 개인 지식의 원본. 모든 작업의 substrate.

앱이 아니라 OS. 껐다 켜는 게 아니라, 늘 돌아간다.

위키 볼트 · LLM Wiki 위성

### 컴파일된 지식

AI가 외부 자료를 읽고 정리해 쌓는 Karpathy 패턴의 위키. 8,400+ 문서가 복리로 누적.

검색은 휘발성, 위키는 자산. 그래서 2명이 대기업과 같은 링에 선다.

핵심

App은 업데이트된다. OS는 내가 업데이트한다.

"ChatGPT가 다 검색해주는데 왜 모으냐"는 질문에 대한 답 — 검색은 정보 소비, 볼트는 자산 형성.

ACT 1 · 하네스

## 그 위에 스키마가 얹힌다.

AI 팀원이 매일 아침 출근할 때 읽는 사규집. 사람 신입에겐 매번 설명해야 하는 걸, 에이전트는 세션을 열 때마다 스스로 읽고 들어온다.

* 9 시스템 파일

  공유 운영 매뉴얼. CLAUDE·AGENTS·DESIGN… precedence 1~9. 누가 출근하든 자기 매뉴얼.
* 8 슬래시 명령

  connect·merge·develop·share + query·lint·status·inbox. "이건 무슨 일인가"를 먼저 묻는다.
* 스킬 62 · 에이전트 6

  반복을 자동화하는 실행 레이어. 룰 8개가 모든 산출물의 품질을 강제.

[![vault-map.cmdspace.work — 두 볼트·룰·명령·스킬·에이전트 전체 시스템 지도](/assets/shots/vault-map.png)](https://vault-map.cmdspace.work)

전체 지도 [vault-map.cmdspace.work ↗](https://vault-map.cmdspace.work) · [system ↗](https://system.cmdspace.work) · [llm-wiki ↗](https://llm-wiki.cmdspace.work)

ACT 1 · 브릿지 · 오늘 만든 것

## 내 볼트가 구글 옆에서 답한다.

구글에 검색하면 왼쪽엔 웹 결과, 오른쪽엔 내 볼트가 같이 답한다. 두 개의 볼트가 동시에, 메인은 빨강·위키는 초록으로 구분되어.

![구글에서 grenadier 검색 시, 오른쪽 사이드바에 위키 볼트(초록)와 메인 볼트(빨강) 노트가 동시에 표시되는 omnisearch](/assets/shots/omnisearch-demo.png)

볼트가 쿼리 가능한 지식 서비스가 되고, 브라우저는 그 클라이언트일 뿐 · 하네스 위에서 기억이 서비스가 되는 순간

ACT 2 · 함대

## 하네스 위에서 만든 서비스들.

![CmdTrace 세션 관제탑 UI](/assets/shots/cmdtrace.png)

네이티브 macOS

### CmdTrace

AI 코딩 세션(클로드코드·코덱스…) 관제탑. 검색·태그·재개.

이 발표가 캐낸 세션을 보는 바로 그 도구 (메타)

[cmdtrace.cmdspace.work ↗](https://cmdtrace.cmdspace.work)

![cmds-eagle 플러그인 화면](/assets/shots/cmds-eagle.png)

Obsidian 플러그인

### cmds-eagle

Eagle 에셋 라이브러리를 볼트와 연결. 검색·임베드·클라우드 업로드.

공식 커뮤니티 플러그인 등재 — 외부 심사 통과한 진짜 제품

공식 등재

![plaud.cmdspace.work 랜딩](/assets/shots/plaud.png)

5축 제품

### Plaud Note Manager

음성 녹음을 볼트로. 하나의 코어를 Web·Desktop·MCP·Skill·App이 공유.

이중 STT 교차검증으로 정확한 회의록 자동 착지

[plaud.cmdspace.work ↗](https://plaud.cmdspace.work)

네이티브 macOS

### CmdMD

review-first 마크다운 에디터. 위키링크·콜아웃·Mermaid·KaTeX.

발주서 한 줄 → 자가독해·리팩토링·test 52·배포

Swift / SwiftUI의존성 0

Obsidian 플러그인

### cmds-share

노트를 1커맨드로 웹 공개. 백엔드 5종 + 종단간 암호화 + CMS 뷰.

노트 하나 → 공개 링크 하나, 한 커맨드

MIT © Yohan Koo

네이티브 macOS

### NetHelm

멀티 회선(유선 > 스타링크 > 테더링) 자동 전환 메뉴바 앱.

내 짜증에서 태어남 · 위치권한 없이 MAC 지문으로 회선 식별

Swift / Network

ACT 2 · 함대 · 공통 패턴

## 발주서는 늘 한 줄.

"마크다운 읽는 앱, **전면적으로 다 개선해줘.** UI도 다 뜯어고쳐도 좋아. **진행해.**"

에이전트가 문서를 스스로 다 읽고, 리팩토링하고, 빌드하고, 테스트하고, 배포까지 끝낸다. 전부 내 볼트와 하네스 위에서 자란다 — 하네스가 없으면 흩어진 앱 열두 개, 하네스가 있으니 하나의 생태계.

SF 같은 실화

AI가 죽은 AI의 부검을 했다.

CmdMD를 처음 만든 Fable 5 모델을 못 쓰게 되자 → "사라진 그 모델이 한 일을 원본 로그에서 복원해줘" → 158번의 작업이 전부 되살아났다.

ACT 2 · 범위 · 함대는 코드만이 아니다

## 같은 시스템으로 최고경영진을 가르치고, 그들의 하네스를 짓는다.

교육

### LG 회장단 · 전체 임원 교육

대한민국 최정상 기업의 회장단과 전 임원을 대상으로 한 에이전틱 AI·지식관리 교육.

코칭

### 각사 CEO 1:1 AI 코칭

경영진 개개인의 업무 맥락에 맞춘 1:1 AI 활용 코칭. 강의가 아니라 맞춤 동행.

구축

### C-level 개인 CMDS 시스템 구축

임원 개인의 지식 운영체제(볼트 + 하네스)를 직접 설계·구축. 가르치는 걸 넘어, 그들의 하네스를 짓는다.

결과

### 강의 → 시스템 → 자생

한 번의 교육이 아니라, 경영진이 스스로 굴리는 운영체제로 남긴다.

핵심

저는 도구 사용법을 가르치지 않습니다. 그들의 하네스를 짓습니다.

같은 스키마·같은 운영체제가, 2인 회사의 함대도 만들고 대기업 회장단의 지식 시스템도 만든다.

ACT 3 · 연구와 비전

## 생각 자체도 제품으로.

![resolution.cmdspace.work — 지식의 해상도](/assets/shots/resolution.png)

멀티모달 · live

### 지식의 해상도

받아들이고·정리하고·내보내는 세 국면의 프레임워크를 글 + 오디오 + 쇼츠 13편으로 동시 출력.

포맷이 사고를 강제한다 — 어디에 담느냐가 무슨 일을 할 수 있는지를 결정

[resolution.cmdspace.work ↗](https://resolution.cmdspace.work)

![9yohan.cmdspace.work — 9요한 별자리](/assets/shots/9yohan.png)

비전 · 설계 단계

### 9Yohan

회사의 9개 운영 부문을 역사 속 9명의 "요한"에게 맡기는 멀티에이전트 구조.

조직표가 곧 에이전트 팀이 된다 (아직 설계 단계 — 방향은 분명)

[9yohan.cmdspace.work ↗](https://9yohan.cmdspace.work)

ACT 4 · 엣지

## 에디터를 벗어난 에이전트.

운전하면서 음성으로 명령하고, 또 다른 에이전트가 결과를 두세 문장으로 읽어준다. 손은 운전대에, 결정은 귀로.

서울 → 원주 주행 텔레메트리

"MOVING\_TOO\_FAST\_FOR\_POLICY"

접시에 직접 물었더니 자백했다. "너무 빨리 달려서 정책상 내가 껐다." 끊김의 70%가 가림이 아니라 의도적 차단. 측정을 넘어 원인까지 캐냈다.

[![starlink.cmdspace.work — 주행 텔레메트리 대시보드](/assets/shots/starlink.png)](https://starlink.cmdspace.work)

클로징

## 환승의 핵심은 도구가 아니라 원본을 쥐는 것.

원본 포맷을 조직이 쥐면, 내 사고방식까지 조직이 쥔다. 나는 내 원본을 마크다운으로, 내 손으로 쥐고 있다. 그래서 2명짜리 회사가 대기업의 포맷에 휘둘리지 않고, 결과물만 맞춰주며 일한다.

take-home

도구를 바꾸기 전에, 당신의 원본을 먼저 쥐세요.

그 위에 하네스를 깔면, 두 명도 함대가 됩니다.

아웃트로 · 환승의 목적지

## 환승의 진짜 목적지는, 더 넓은 삶.

하네스가 반복을 가져가면, 저에게는 삶이 남습니다. 이번 여름 북미 서부로 — 밴쿠버 보트 숙소와 시애틀 하우스 파티에서 노래하고, 샌프란시스코·LA까지 가는 길마다 한인·글로벌 기업 사람들과 지식관리·옵시디언·AI를 나눕니다.

[![](/assets/video/outro-poster.png)](/assets/video/outro.mp4)

내 클론 보이스로 만든 아웃트로 인포그래픽 · 59초 ▶

고백

## 이 사이트도 에이전트가 만들었습니다.

제가 오케스트레이터를 맡고, AI 에이전트들이 제 지난 두 달치 작업을 스스로 다 읽고, 정리하고, 무대에 올릴 이야기를 뽑아 이 dream.cmdspace.work로 만들었습니다. 지금 이 강연 자체가, 30분 동안 말씀드린 그 방식으로 만들어졌습니다.

### 저는 2명입니다. 그런데 혼자 일하지 않습니다.

[cmdspace.work ↗](https://cmdspace.work)
[시스템 파일 ↗](https://system.cmdspace.work)
[LLM Wiki ↗](https://llm-wiki.cmdspace.work)

구요한 · CMDSPACE (커맨드스페이스) · 2026 꿈도 환승이 되나요 컨퍼런스 · 일하는 방식, AI로 환승하다

01 / 11
