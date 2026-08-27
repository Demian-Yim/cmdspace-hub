---
title: cmds-gobi-cohort-1
source: https://cohort.cmdspace.work/
author: 구요한 (CMDSPACE)
fetched: 2026-08-28
note: markitdown HTML→MD 자동 변환 스냅샷. 정확한 원문은 source URL 참조.
---

[![CMDS](/assets/logos/cmds-logo-round.png)
CMDS × GOBI Cohort 1기](/)

[시간표](#schedule)
[개념 8](#concepts)
[가이드 2](#guides)
[시작하기](#quickstart)
[GitHub](https://github.com/johnfkoo951/cmds-vault)
[강의 자료 받기 →](#quickstart)

CMDS × GOBI Cohort 1기 · Session 1 (2026-05-02)

# 지식을 컨텍스트로 채우는 첫 90분.

PKM 이론 · 마크다운 · 메타데이터 · 옵시디언 · CMDS 시스템 · AI 협업 · 다차원 분류 · 멀티볼트 — 8개 개념과 2개 실습 가이드. 1주차 사전 학습부터 사후 레퍼런스까지 한 페이지에서. 강의 후 자가 진행할 때도 그대로 펼쳐서 보세요.

[지금 시작](#quickstart)
[개념 8 둘러보기](#concepts)
[cmds-vault](https://github.com/johnfkoo951/cmds-vault)

8

개념 (Concepts)

2

실습 가이드

120

분 (Session 1)

12

주차 코호트

📅**2026-05-02 (토)** 90분 강의

👥 Foundation · Advanced · 비동기 3트랙

🛠 Obsidian + Claude Code + cmds-vault

강사: 구요한 + 김진영

Session 1 Key Takeaway · 5가지

## 학생이 가지고 가야 할 다섯 가지.

개별 강의 자료 안 만듦 (라이브 시연). 이 사이트가 학생 핸드아웃이자 강사 백업 자료. 다 못 따라잡아도 **이 5가지만**은 머릿속에 두고 종료.

01

마크다운 = 통신 규격

`.md`로 기록된 것만 AI가 자유롭게 처리. PPT·HWP·DOCX는 \*퍼블리케이션 포맷\*에 불과.

02

메타데이터가 KEY

본문보다 frontmatter(YAML)가 AI에게 더 중요. **Progressive Disclosure**: AI는 메타부터 읽고 어디를 깊게 볼지 결정.

03

PKM = 다차원

폴더는 mutually exclusive 분류만, 그 외는 태그·메타·링크. CMDS 9 카테고리는 *체계*이지 *유일한 분류*가 아님.

04

AI 협업 = 맥락 전달

프롬프트 엔지니어링이 아니라 **컨텍스트 엔지니어링**. 내 볼트의 메타·노트가 AI의 확률값.

📘

W1 산출물

cmds-vault 클론 → 시스템 파일 8개 이해 → **Claude Code 온보딩 인터뷰**로 본인 컨텍스트 채워오기.

3-Layer 분리

## 실행 / 안내 / 디자인 — 위치가 다르면 역할이 다르다.

코호트 자료는 세 곳에 분리 배포됩니다. 학생은 **실행 스킬**(cmds-vault)과 **학생 가이드**(이 사이트)만 보면 됨.

🤖

Layer 1 · 실행

### cmds-onboarding 스킬

Claude Code 가 실제로 \*읽고 따라하는\* 명령어·흐름. 학생 PC에서 실행됨.

`cmds-vault/90. Settings/91. Skills/
cmds-onboarding/SKILL.md`

🛠

Layer 2 · 안내 (여기)

### 학생 가이드

학생이 **강의 전·후 보는** 진행 흐름과 콘텐츠. 이 사이트.

`cohort.cmdspace.work
(8 Concepts + 2 Guides)`

🎨

Layer 3 · 디자인

### 시나리오 디자인 노트

구요한 본인이 보는 \*왜 그렇게 설계했는가\* 기록. walkthrough · edge case · iteration log.

`마더십 볼트 / 03-onboarding-
scenario.md (디자이너 전용)`

Session 1 시간표

## 120분 · 5부 흐름.

총 120분이 빠듯하므로 시간 큐 엄격히. 시연이 길어지면 **4부 실습 시간이 깎이지 않게** 시연 부분을 자르자. 각 부 우측 링크는 해당 강의 자산으로 직접 이동.

| 분 | 파트 | 진행 | 내용 / 자산 |
| --- | --- | --- | --- |
| 0–15 | 0부 도입 | Jin | 코호트 설립 목적, PKM 배경·철학, Gobi 스페이스 소개 · [→ 01 PKM 개론](#concept-01) |
| 15–35 | 1부 PKM 이론 | 구요한 | 마크다운 → 메타데이터 → 다차원 분류 · [→ 02](#concept-02) · [→ 03](#concept-03) · [→ 05](#concept-05) |
| 35–55 | 2부 CMDS 시연 (1) | 구요한 | 9 카테고리 + 8 시스템 파일 라이브 투어 · [→ 06](#concept-06) · [→ 04](#concept-04) |
| 55–75 | 3부 CMDS 시연 (2) | 구요한 | 실제 사용 사례 — LG 연표 / 더베러 글 / Mermaid / 리서치 파이프라인 · [→ 07](#concept-07) |
| 75–80 | 휴식 (5분) | — | — |
| 80–105 | 4부 실습 ⭐ | 모두 | cmds-vault 클론 → Claude Code 온보딩 인터뷰 · [→ G1 클론 가이드](#guide-01) · [→ G2 온보딩](#guide-02) |
| 105–115 | 5부 멀티볼트 + 과제 | 구요한 | 2주차 LLM Wiki 위성 볼트 사전 안내, W1 과제 · [→ 08 멀티볼트](#concept-08) |
| 115–120 | 마무리 + Q&A | Jin + 구요한 | 토론 1–2개 / 카톡방 비동기 이관 |

Concepts · 8

## 개념 8 — 탭으로 펼쳐보기.

각 개념은 강의 시간 내 **5–7분 핸드아웃** 분량. 강의 전 사전 학습 / 강의 후 복습 / 향후 LG 임원 교육·차의대 수업 재활용 가능한 영구 자산.

01PKM 개론
02마크다운
03메타데이터
04옵시디언
05다차원 분류
06CMDS 시스템
07AI 협업 환경
08멀티볼트

Concept 01 · 📚 601

### 지식관리 개론 — PKM in AI Era

**세션 매핑**: Session 1 1부 도입 (5분 핸드아웃 기준)

⭐ Key Takeaway

공개 지식의 가치는 AI가 가져갔다. 남은 차별화 자원은 *고유한 경험·판단·맥락*이며, 이를 잡아두는 도구가 PKM이다.

#### 1. PKM은 왜 다시 중요한가

##### (a) 공개 지식의 가치 함락

* 검색·요약·정리 등 *공개 지식의 가공*은 AI가 평균 이상으로 해낸다
* 위키·블로그·교과서에 있는 정보를 외워두는 것의 시장 가치는 0에 수렴
* 따라서 차별화는 **AI가 가져갈 수 없는 영역**에서만 가능

##### (b) 그럼 차별화는 어디서 오는가

사람이 소유한 채로 남는 자산:

* **경험 데이터**: 미팅·관찰·프로젝트 기록 — 본인만 본 장면
* **자기 사고**: 메모·일기·대화에 담긴 자기 해석
* **맥락**: 어떤 상황에서, 누구와, 어떤 문제로 이걸 만났는지
* **취향·관점**: 내가 좋다고 판단하는 기준 자체

##### (c) 결론

PKM은 *"검색 시대"의 정리 도구*가 아니라 ***"AI 시대"의 차별화 자산을 축적하는 시스템***이다.

#### 2. 정보 수집의 원칙 — 무엇을 흡수할 것인가

##### (a) 신호 vs 노이즈

* 모든 걸 모을 수는 없다. 모아도 의미 없음
* **개인 PKM Mission**이 필터: 본인이 풀고 싶은 핵심 문제·관심사
* 정보 수집·분류·연결의 기준점은 *Mission* 한 줄에서 나온다

##### (b) Capture-First 원칙

* **일단 잡고, 분류는 나중에**. 분류하느라 못 잡으면 본말전도
* 옵시디언의 `00. Inbox/`, 카톡 '나에게 보내기', Apple Notes — 어느 도구든 *일단 잡는 입구*가 있어야 함
* 단, 입구가 너무 많으면 분산. **입구 1–2개로 수렴**

##### (c) 흡수 4 카테고리

| 카테고리 | 예시 |
| --- | --- |
| 외부 지식 | 책·논문·기사·강의 |
| 자기 사고 | 메모·일기·대화 메모 |
| 경험 데이터 | 프로젝트 기록·미팅·관찰 |
| AI 산출 | 요약·분석·생성된 결과물 |

#### 3. PKM 프레임워크 빠른 투어

학생이 *각 프레임워크의 1차 차이점만* 알면 충분.

##### (a) Zettelkasten (Niklas Luhmann)

* 원조. 노트 간 *링크*가 1급 시민
* 원자적(atomic) 노트 + 자기 언어로 재서술
* 옵시디언이 가장 잘 구현하는 모델

##### (b) PARA / BASB (Tiago Forte)

* 행동 지향. **P**rojects · **A**reas · **R**esources · **A**rchives
* 노션이 가장 잘 구현하는 모델 (프로세스 매뉴얼)
* 약점: *미세 지식 재발굴*이 어려움 (단편 이벤트 검색 한계)

##### (c) LYT (Linking Your Thinking, Nick Milo)

* MOC(Maps of Content) 중심
* 폴더 대신 *큐레이션 노트*로 위계 형성

##### (d) CMDS (구요한) ← 본 코호트 채택

* **Connect → Merge → Develop → Share** 4단계 파이프라인
* 100–900 카테고리 (도서관 Decimal System 모방)
* 한국어 PKM 환경에 최적화
* AI 친화적 메타데이터 + 마크다운 우선

#### 4. PKM의 목표는 사람마다 다르다

* **출판** — 책·뉴스레터·아티클 (본 코호트 1차 권장)
* **업무 효율** — 회의록·보고서 자동화
* **학습** — 새 분야 시스템 학습
* **사고 정리** — 본인 머릿속 구조 외부화
* **재미** — 큐레이션·취향 아카이브

→ 본 코호트의 1차 권장은 **출판(책쓰기)**이지만, 다른 목표를 가진 학생도 *볼트 컨텍스트가 자기 맥락으로 채워지면* 어떤 목표든 강화됨.

#### 5. 토론 질문 (선택)

* **🥊 "공개 지식의 가치 함락"은 정말 일어나고 있는가?** "AI가 정리해주는 능력 자체"가 새로운 공개 지식이 되어 가치를 유지하는 것은 아닌가?
* **🔬 본인의 PKM Mission을 한 줄로 적으면?** 그 한 줄이 다음 12주 동안 정보를 거르는 기준이 될 수 있는가?

Concept 02 · 📚 601

### 마크다운 — AI 시대의 통신 규격

**세션 매핑**: Session 1 1부 (1)(2) — 마크다운 핵심 메시지 + 5분 라이브 데모 · **코호트의 한 단어**: 강의가 끝나도 딱 하나 가져가야 한다면 → **마크다운**

⭐ Key Takeaway

마크다운은 사람도 읽고 AI도 처리하는 유일한 표준이며, 메타데이터까지 함께 담을 수 있는 사실상 유일한 범용 포맷이다.

#### 1. 왜 지금 마크다운인가

##### (a) 마크업 랭귀지의 계보

* **HTML** (Hypertext Markup Language) — 웹 표준
* **XML** (Extended Markup Language) — DOCX·HWPX·PPTX의 내부 구조
* **마크다운(.md)** — 마크업 랭귀지 *톤다운* 버전. 사람도 읽고 AI도 처리

##### (b) 비교표

| 포맷 | AI 가독 | 사람 가독 | 메타 | 전용 프로그램 |
| --- | --- | --- | --- | --- |
| HWP / DOCX / PPTX | △ | ✅ | △ | ✅ 필요 |
| HTML / XML | ✅ | ✗ 노이즈 | ✅ | ✗ |
| PDF | △ | ✅ | △ | ✗ |
| **마크다운(.md)** | ✅ | ✅ | ✅ | ✗ |

→ 마크다운의 **유일한** 강점: human-friendly + machine-readable + AI-friendly + metadata-capable + format-portable.

##### (c) AI들이 모두 마크다운으로 출력하는 이유

* ChatGPT / Claude / Gemini / Grok 등 모든 LLM이 *공통 출력 포맷*으로 마크다운 채택
* 우연이 아니라 *사람과 AI가 동시에 보기 편한 유일한 합의점*이기 때문

##### (d) 정부·산업 채택

* **2026년 3월 초**, 국가 AI 전략위원회가 **공식 보고 포맷의 표준**으로 마크다운 채택
* 마이크로소프트·한컴 등 모든 문서 제조사가 자사 포맷 → 마크다운 변환 툴 출시 중

##### (e) PPT/HWP의 운명

* PPT/HWP/PDF는 **퍼블리케이션 포맷** — 사람이 보기 위해 *한 번 출력한* 형식
* 한 번 출력되면 AI 워크플로에 *재투입하기 어려움* → AX(AI 전환)의 결정적 병목
* "조직의 모든 보고가 PPT면 AX는 못 한다" — 사용자 LG 임원 교육 발언

#### 2. 핵심 문법 — 5분 라이브 데모

##### (a) Heading (`#`)

markdown

```
# 제목             → Heading 1 (문서 최상위)
## 챕터            → Heading 2
### 섹션           → Heading 3 ... 6레벨까지
```

AI는 이 위계로 문서 구조를 파악.

##### (b) 강조

| 입력 | 결과 |
| --- | --- |
| `**볼드**` | **볼드** |
| `*이탤릭*` | *이탤릭* |
| `***볼드+이탤릭***` | ***볼드+이탤릭*** |

##### (c) 리스트 + 들여쓰기

markdown

```
- 장 볼 것들
  - 우유
  - 식빵
- 좋아하는 음식
  - 치킨
  - 피자
```

→ AI 편집기에서 **Tab 키 안 먹음** → **스페이스바 2~4칸**으로 들여쓰기.

##### (d) Backtick (`` ` ``) — Esc 키 아래, Tab 키 위

| 입력 | 의미 |
| --- | --- |
| `` `키워드` `` (단일) | AI가 키워드로 인식, 임의 변경 X |
| ```` ``` ```` (삼중) → 본문 → ```` ``` ```` | 코드 블록. 자료의 시작·끝 명확히 구분 |

→ **삼중 백틱 활용 예시**: 회의록 + 작년 인사말 + 전임 원장 인사말 3개를 AI에게 줄 때, 각각을 코드 블록으로 감싸면 AI가 *어디서부터 어디까지가 무슨 자료인지* 명확히 인식.

##### (e) 위키링크 (`[[]]`) — 옵시디언 확장

* 표준 마크다운은 아니지만 옵시디언·Bear·Logseq 등이 채택
* 같은 볼트 내 다른 노트로 즉시 링크

#### 3. 메타데이터(Frontmatter) — 본문 위 YAML

yaml

```
---
type: note
aliases: [별칭]
description: "1–2문장 영어 LLM 힌트"
author:
  - "[[구요한]]"
date created: 2026-05-02
date modified: 2026-05-02
tags: [pkm, markdown]
---

본문 시작…
```

#### 4. 자주 묻는 질문

**Q. 마크다운 직접 쓰기 어렵다면?** → 차선책: **Google Docs**. 입력 후 *마크다운 다운로드* 가능. 핵심 아젠다만 마크다운으로 보존하면 됨.

**Q. PDF는?** → *읽기*는 Claude Code가 OCR로 다 해냄. 단, 옵시디언 볼트에 *직접 넣지는 말 것* — 검색·메타 처리가 어려워짐. **메타 정보만** 옵시디언에, 본문은 외부 도구(Bookends/Zotero)에.

**Q. HWP 중심 기관에서 어떻게 시작?**

* 단계 1: 모든 HWP → **HWPX**(XML 기반)로 전면 교체
* 단계 2: 헤딩 스타일을 *명시적으로 적용* (글자 크기 조절 X)
* 단계 3: 마크다운 변환 툴 활용 (한컴이 출시 중)

Concept 03 · 📚 601

### 메타데이터 설계 원리

**세션 매핑**: Session 1 1부 (3) — 메타데이터 = 빙산의 일각 · **한 문장**: 본문보다 메타데이터가 AI에게 더 중요하다.

⭐ Key Takeaway

메타데이터는 AI가 *어디를 깊게 볼지 결정하는 카탈로그*다. 본문 1만 줄보다 잘 정돈된 frontmatter 7줄이 AI 활용의 90%를 결정한다.

#### 1. Progressive Disclosure (점진적 공개)

##### (a) 컨텍스트 윈도우의 한계

* 모든 LLM은 *기억할 수 있는 토큰 수*가 제한 (모델별 상이)
* 옵시디언 볼트에 1만 개 노트가 있어도 *모두 다 읽을 수는 없음*
* 따라서 *효율적 읽기*가 필수

##### (b) AI는 메타데이터부터 읽는다

* 노트의 frontmatter(YAML 영역)는 **빙산의 일각** — 본문 진입 전 먼저 스캔
* 메타로 *어떤 종류의 노트인지·언제 쓴 건지·누가 작성했는지·어떤 주제인지* 파악
* *"이 노트는 깊게 볼만한가?"* 를 메타로 1차 판단 → 필요한 노트만 본문 진입

##### (c) 비유

* 조직에서 *누구한테 무슨 일을 시킬지* 머릿속에 있는 그 정보 = 각 사람의 메타데이터
* *카탈로그/제품 설명서*만 보고 사야 할 제품을 결정하는 것과 같음
* 도서관에서 *카드 카탈로그*로 책을 찾는 것과 같음

→ "AI가 별거 없다 = 내가 쓴 말 별거 없다" — 메타데이터를 안 쓰면 AI는 *맥락 없는 텍스트 더미*를 받는 것

#### 2. CMDS 7 필수 프로퍼티

yaml

```
---
type:           # note / meeting / terminology / curriculum 등
aliases: []     # 별칭 (배열)
description: "" # ⭐ 영어 1–2문장, LLM 관련성 힌트
author:
  - "[[구요한]]"
date created:   # YYYY-MM-DD (ISO 8601)
date modified:  # YYYY-MM-DD
tags: []        # 주제 태그
---
```

##### (a) `type` — 노트의 종류

* 노트가 *어떤 클래스인지* 명시. AI가 처리 패턴을 다르게 적용
* 흔한 값: `note` / `meeting` / `terminology` / `people` / `curriculum` / `channel` / `manuscript` / `moc` / `CMDS`

##### (b) `description` — 영어 1–2문장 LLM 힌트 ⭐ 가장 중요

**원칙**:

* **영어** (한국어 X)
* 1–2문장
* "스킬 설명" 스타일: 무엇 + 언제 참조해야 하는지
* **반드시 큰따옴표 `"..."` 로 감쌀 것** (안에 `:` 나 `#` 들어가면 YAML 파서 깨짐)

**좋은 예시**:

yaml

```
description: "Meeting minutes from 2026-04-07 LG AX camp retrospective. Contains CEO feedback summary and next-action items."
```

**나쁜 예시**:

yaml

```
description: "회의록입니다"        # 한국어 + 비기능
description: This is a note        # 큰따옴표 누락 → YAML 파서 위험
```

##### (c) `date created` / `date modified`

* ISO 8601 (`YYYY-MM-DD`)
* AI가 *최신성*으로 검색·소팅 가능 → "최신 글 10개만 학습해" 같은 명령 가능

##### (d) `author` — 배열 + 큰따옴표 wikilink

yaml

```
author:
  - "[[구요한]]"
  - "[[김진영]]"
```

#### 3. CMDS 선택 프로퍼티

| 필드 | 가리키는 곳 | 예시 |
| --- | --- | --- |
| `CMDS` | 📚 subcategory (2nd-level, N01–N99) | `"[[📚 601 Knowledge Management]]"` |
| `index` | 🏷 Index 노트 | `"[[🏷 Lecture Notes]]"` |
| `status` | 5종 표준값 | `unread` / `reading` / `inProgress` / `completed` / `archived` |
| `published` | Boolean | `true` / `false` (writer 스킬이 필터링) |

##### ⚠️ `CMDS:` vs `index:` 방향 규칙 (자주 헷갈림)

| 프로퍼티 | 대상 | OK | NG |
| --- | --- | --- | --- |
| `CMDS:` | **📚 subcategory** | `"[[📚 601 Knowledge Management]]"` | `"[[📖 100 Themes]]"` (📖는 frontmatter X) |
| `index:` | **🏷 Index 노트** | `"[[🏷 Research Notes]]"` | `"[[📚 102 Topics]]"` (📚는 CMDS 필드) |

#### 4. 카멜케이스 규칙

* 복합어 필드는 카멜케이스: `myRate`, `totalPage`, `startReadDate`
* ⚠️ `rating` 사용 금지 → 반드시 `myRate`

#### 5. 메타데이터가 *결정적*인 이유 — 사용자 사례 3가지

##### (a) "심평원이랑 1분기 했던 연구 다 가져와봐"

* 모든 연구 노트에 `coworker`, `period`, `topic` 메타가 있어야 가능
* 메타 없으면 본문 검색만 → 1만 노트면 사실상 불가

##### (b) writer 스킬 (publish=true 필터)

* 사용자가 *발행한 글*만 학습시키는 스킬
* frontmatter에 `published: true` 가 있어야 작동
* 새 글 추가될 때마다 *자동*으로 최신 학습 풀에 반영

##### (c) Claude Code "LG 관련 문서 정리해줘" → 1–2분 만에 연표

* 모든 미팅 노트의 `attendees`, `date`, `organization` 메타로 시기별 정렬
* 메타 없으면 *Regex 검색 + 수동 분류*로 1시간+ 소요

Concept 04 · 📚 501

### 옵시디언의 장점 — 왜 3세대인가

**세션 매핑**: Session 1 2부 도입 — *옵시디언 vs 노션 vs 에버노트* · **한 문장**: 노션의 AI 협력 가능성이 1이라면, 옵시디언은 100이다.

⭐ Key Takeaway

옵시디언은 마크다운 + 로컬 파일 + 위키링크 + 플러그인 생태계의 결합으로, AI 시대 PKM 도구로서 *체급이 다른* 선택지다.

#### 1. 노트 도구의 세대 구분

| 세대 | 대표 도구 | 핵심 가치 | 한계 |
| --- | --- | --- | --- |
| **1세대** | 에버노트 | 디지털 노트 테이킹 | 데이터 락인, 마크다운 미지원 |
| **2세대** | 노션 | DB + 협업 + 매뉴얼화 | **미세 지식 재발굴 어려움** + 클라우드 의존 + 1만+ 시 렌더 느림 |
| **3세대** | **옵시디언** | 마크다운 + 위키링크 + 로컬 + 플러그인 | 진입 곡선 (CLI 친화 ↔ 비개발자 거리감) |

#### 2. 옵시디언의 5대 장점

##### (1) 마크다운 + 로컬 파일 = 데이터 주권

* 모든 노트가 `.md` 파일로 *내 컴퓨터에* 저장
* 옵시디언이 사라져도 *마크다운 에디터*만 있으면 모든 데이터 그대로 사용 가능
* Vendor lock-in 없음. 미래 호환성 보장

##### (2) 위키링크 = 노트 간 연결을 1급 시민으로

* `[[노트명]]` 한 번이면 양방향 링크 자동 생성
* 한 노트를 수정하면 *해당 노트를 참조하는 모든 노트*가 자동 인지
* 결과: 뇌의 뉴럴 네트워크처럼 *노트 그래프* 형성

example

```
[[구광모]] 검색 → 미팅 노트 + 교육 이력 + 관련 인물 + 프로젝트 한 번에 surface
```

##### (3) 메타데이터 친화 = AI 활용의 결정적 차이

* frontmatter(YAML) 표준 지원
* 데이터뷰(Dataview) 플러그인으로 *노트를 DB로 사용 가능*
* AI에게 메타로 필터링 가능 ("publish=true인 글만 읽어")

##### (4) 플러그인 생태계 = 2,700+개 + 자체 제작 가능

* **Import 플러그인**: Notion / Evernote / Apple Note / Google Keep / OneNote / CSV → 마크다운 변환
* **Dataview**: 노트 쿼리 (DB 기능)
* **Templater**: 동적 템플릿 + 변수 자동 입력
* **Excalidraw / Excalibrain**: 시각적 사고
* **Smart Connections**: AI 기반 노트 연결
* **Calendar / Chronology**: 날짜 기반 탐색
* 본인 플러그인 직접 개발 가능 (사용자도 5개 직접 제작)

##### (5) 엔터프라이즈 무료 + 사내망 SYNC 가능

* 기존 유료 엔터프라이즈 요금제가 *무료로 풀림*
* 오픈소스는 아님. 단, **모든 데이터 로컬** → 보안은 사내 인프라가 결정
* 사내 클라우드 서버 + 자체 플러그인으로 *사내망 전용 SYNC* 구성 가능
* 단, 앱(.app)이 있어야 함. 웹 미지원

#### 3. 노션과의 직접 비교 (AI 협업 관점)

| 영역 | 노션 | 옵시디언 |
| --- | --- | --- |
| 파일 형식 | 유사 마크다운 (클라우드 DB) | **실제 `.md` (로컬 저장)** |
| AI 협업 가능성 | 1 (Notion AI 한정) | **100 이상** (Claude Code 자유 접근) |
| 강점 | 공동 협업, 어디서든 | 개인 생산성, AI 연동, 플러그인 |
| 미세 지식 재발굴 | ✗ (단편 검색 한계) | ✅ (그래프뷰, Dataview, 위키링크) |
| 노트 1만+ 렌더 | 느림 | 빠름 (로컬) |
| 클라우드 실시간 공유 | ✅ | △ (Sync 유료, 또는 git) |
| 데이터 주권 | 클라우드 | **본인 컴퓨터** |

#### 4. 다른 도구와의 관계 — 안 버려도 됨

옵시디언이 *모든 것을 대체*해야 하는 게 아님. 역할 분리가 핵심:

* **노션** → 팀 매뉴얼·프로세스 공유는 노션 유지 OK
* **PDF·논문** → Bookends(Mac) 또는 Zotero(Win)에 *원문* 보존, 옵시디언엔 *메타+노트*만
* **이미지 자산** → Eagle 등 자산 관리 툴
* **회의록 음성** → Plaud / Otter / Whisper로 전사 후 옵시디언으로 import
* **할 일 / 캘린더** → 별도 도구 + Obsidian Tasks 플러그인 연동

→ "옵시디언이 안 좋은 게 아니라, 모든 걸 한 도구로 하려는 게 안 좋은 것"

#### 5. 코호트 1주차 학생용 진입 권장 순서

1. **클론**: cmds-vault 클론 (Mac/Win, 한글 폴더명 회피) → [G1 클론 가이드](#guide-01)
2. **첫 노트**: `00. Inbox/`에 일자 노트 1개 작성 (마크다운 + frontmatter 7필드)
3. **위키링크**: 다른 노트 1개에 `[[]]`로 연결
4. **그래프뷰**: 그래프 한 번 보기 — *노드 2개 + 엣지 1개*의 작은 시작
5. **Daily Note**: Calendar 플러그인 활성화 후 매일 일자 노트 1개 작성

→ "그래프뷰가 풍성해지는 데 평균 3개월". 첫 1–2주는 *그냥 작성*에만 집중.

Concept 05 · 📚 601

### 다차원 분류 (Multi-dimension Classification)

**세션 매핑**: Session 1 1부 (4) — *폴더 vs 태그 vs 링크 vs 메타* · **한 문장**: 하나의 파일은 하나의 폴더에만 살 수 없다.

⭐ Key Takeaway

폴더는 *mutually exclusive* 분류에만 쓰고, 그 외의 모든 분류는 태그·메타데이터·위키링크·인덱스 노트로 다차원적으로 처리한다.

#### 1. 시작 비유: 원숭이·바나나·팬더

세 가지 사물을 *두 그룹*으로 분류하시오. 학생들에게 답을 시켜보면 보통 4–5가지 답이 나옴:

| 분류 기준 | 그룹 |
| --- | --- |
| 동물/식물 (서양적·분류론) | (원숭이·팬더) vs (바나나) |
| 관계론적 (동양적) | (원숭이·바나나) vs (팬더) — 원숭이가 바나나를 좋아함 |
| 글자 수 | (원숭이·바나나, 6글자) vs (팬더, 3글자) |
| 끝 글자 | (바나나·팬더, 끝글자 'A') vs (원숭이) |

→ **모두 정답**. 단지 *어느 차원으로 자르느냐*의 차이. 마찬가지로 *하나의 노트가 하나의 폴더에만 살 수 없다.*

#### 2. 폴더의 한계 — 왜 폴더 한 개로는 부족한가

##### 예시: 리더십 논문 1편

* 주제 분류: **리더십**? 그런데 **조직 문화**도 다룸
* 방법론: **서베이** 사용? 그런데 **머신러닝** 분석도 함
* 산출물: **저널 논문**? 그런데 **강의 자료**로도 재활용

→ 어느 폴더에 넣어도 *다른 분류에서 보면 잘못된 곳*

##### 폴더의 정당한 사용처

폴더는 *서로 겹치지 않는(mutually exclusive)* 분류에만:

* `00. Inbox/` (미정리) vs `30. Permanent Notes/` (정리 완료) — 시간/상태 기준
* `60. Collections/61. People/` vs `60. Collections/63. Meetings/` — 엔티티 종류 기준
* `40. Docs/41. Official Docs/` vs `40. Docs/46. My Docs/` — 출처 기준

#### 3. 4가지 분류 도구 — 언제 무엇을 쓸 것인가

| 도구 | 적합 | 부적합 | CMDS 활용 예 |
| --- | --- | --- | --- |
| **폴더** | mutually exclusive 상태 | 횡단 주제 | `00. Inbox/` / `30. Permanent Notes/` |
| **태그** (`#태그`) | 횡단 주제, 동시에 여러 개 | 정확한 위계 | `#pkm`, `#ai`, `#cohort` |
| **위키링크** (`[[]]`) | 노트 간 관계 | 단순 분류 | `[[김진영]]` 으로 모든 김진영 미팅 노트 연결 |
| **메타데이터** | 구조화 속성, 쿼리 가능 | 자유 텍스트 | `CMDS: "[[📚 601 Knowledge Management]]"` |

#### 4. "정리되어 있지 않다 ≠ 정리 안 됨"

학생이 흔히 갖는 오해: *모든 노트가 깔끔한 폴더에 들어가 있어야 정리된 상태*.

사실은:

* **스택 형태도 정리**: "이번 분기 읽을 논문 30편" 스택 = 정리된 상태
* **인덱스 노트(MOC)도 정리**: 큐레이션 노트 1개로 분산된 노트 모음
* **태그 클러스터도 정리**: `#book2026`으로 묶인 모든 노트
* **그래프 군집도 정리**: 위키링크로 자연스럽게 형성된 클러스터

→ 폴더에만 의존하면 *분류 불안*에 시달림. 다차원적으로 보면 *어디든 정리된 상태*.

#### 5. CMDS의 다차원 매핑 — 실제 사례

한 노트 (예: *2026-04-15 LG 회장단 코칭 회의*)는 다음 차원에 *동시에* 등장:

yaml

```
type: meeting                            # → 클래스
CMDS: "[[📚 909 Consulting & Advisory]]" # → 카테고리
index: "[[🏷 Meeting Notes]]"             # → 인덱스
attendees:
  - "[[구광모]]"
  - "[[권봉석]]"                         # → 인물 그래프
project: "[[LG-AX-임원교육-프로젝트]]"   # → 프로젝트
date: 2026-04-15                         # → 시간축
tags: [coaching, executive, lg, ax]      # → 횡단 주제
```

→ 폴더는 `60. Collections/63. Meetings/2026-04-15-LG-회장단-코칭.md` 단 한 곳. 하지만 **6개 차원에서 동시 surface**.

#### 6. 강의 진행 큐 (5–7분 핸드아웃)

| 분 | 내용 |
| --- | --- |
| 0–1 | 원숭이·바나나·팬더 비유 — 학생들에게 답 시키기 |
| 1–2 | "하나의 노트가 하나의 폴더에만 살 수 없다" |
| 2–4 | 4가지 분류 도구 비교 (폴더 / 태그 / 링크 / 메타) |
| 4–5 | CMDS 다차원 매핑 사례 (한 회의 노트가 6개 차원에 surface) |
| 5–6 | "혼잡 ≠ 안 정리됨" 메시지 |
| 6–7 | 다음 자산 (06 CMDS 시스템 구조) 으로 연결 |

Concept 06 · 📚 601

### CMDS 시스템 구조 — 9 카테고리 + 8 시스템 파일

**세션 매핑**: Session 1 2부 (1)(2) — CMDS 9 카테고리 + 8 시스템 파일 라이브 투어

⭐ Key Takeaway

9 카테고리는 학생이 *자기 분류 체계를 만들 때 참조하는 청사진*이고, 8 시스템 파일은 *AI에게 본인을 컨테이너로 설명하는 표준*이다.

#### 0. 강조: 학생은 CMDS를 *그대로 따라할 필요 없음*

* 9 카테고리는 *구요한의 체계*. 도서관 Decimal System을 모방
* 본 코호트는 *체계 만드는 방법*을 보여주는 게 목적, *이 체계를 강제하는 게* 목적이 아님
* 학생 권장 경로: ① cmds-vault 그대로 시작 → ② 3–6개월 사용하며 자기 도메인 적응 → ③ 자기 버전 100–900 만들기

#### 1. 9 카테고리 (100–900) 빠른 투어

| 번호 | 영역 | 핵심 주제 | 키 서브카테고리 |
| --- | --- | --- | --- |
| 📖 100 | **Themes** | 관심사 / 토픽 / 변수 / 용어 | 101 Interests / 102 Topics / 103 Variables / 104 Terminologies |
| 📖 200 | **Literature** | 외부 지식 통합 → 자기 이해 | 201 Concepts / 202 Frameworks / 210 Reviews / 220 Insights / 240 Books |
| 📖 300 | **Data** | 데이터 관리 / 설문 / 패널 / LMS | 301 Scale Dev / 302 Questionnaires / 310 Data Mgmt / 311 DB |
| 📖 400 | **Methodologies** | 연구방법 / 통계 / ML / 코드·프롬프트 | 401 Research Methods / 410 Stat / 420 ML / 491 Codes / 492 Prompts |
| 📖 500 | **Products** | 도구 (Obsidian / ChatGPT / Claude / n8n) | 501 Obsidian / 521 Claude / 530 Midjourney / 541 n8n |
| 📖 600 | **Specialties** | 전문 영역 (PKM / Second Brain / GenAI / 생산성) | 601 KM / 603 Second Brain / 620 GenAI / 680 Educations |
| 📖 700 | **Creatives** | 창작 (YouTube / SNS / 음악 / 디자인) | 701 YouTube / 710 SNS / 720 Music / 731 Digital Art |
| 📖 800 | **Outputs** | 산출물 (논문 / 강의 / 컨설팅) | 801 PhD / 802 Articles / 820 Research / 831 Consulting / 840 Lectures |
| 📖 900 | **Divisions** | 9 사업부 운영 | 901 KM / 902 Writing / 903 Teaching / 909 Consulting |

#### 2. CMDS Process — Connect → Merge → Develop → Share

CMDS는 *분류 체계*인 동시에 *지식 흐름의 4단계 파이프라인*:

workflow

```
🔗 Connect          🔀 Merge              🛠 Develop                📤 Share
(아이디어 발견)   →  (지식 통합)        →  (방법론·도구 적용)     →  (출판·교육·공유)
[100 Themes]        [200 Literature]      [300–600]                 [700 Creatives /
                                                                     800 Outputs]
```

**단계별 질문**:

* **Connect**: 무엇이 궁금한가? 어떤 용어를 알아야 하는가?
* **Merge**: 학자들은 뭐라 하나? 내 해석은?
* **Develop**: 어떤 데이터·방법·도구로 발전시킬까?
* **Share**: 누구에게 어떤 형식으로 공유할까?

→ CMDS Process는 마더십에서 8개 슬래시 커맨드로 자동화 (`/connect`, `/merge`, `/develop`, `/share` + `/inbox`, `/lint`, `/query`, `/status`)

#### 3. 8 시스템 파일 — Audience 별 그룹

##### 그룹 A: 🤖 LLM 코딩 에이전트 (always-loaded)

| 파일 | 대상 | 역할 |
| --- | --- | --- |
| **CLAUDE.md** | Claude Code | Claude Code 전용 기술 규칙·command 매핑 |
| **AGENTS.md** | Codex / Cursor / Windsurf | 일반 AI agent 기술 규칙 |

##### 그룹 B: 🧪 Vendor-specific

| 파일 | 대상 | 역할 |
| --- | --- | --- |
| **ANTIGRAVITY.md** | Google Gemini / Antigravity | Gemini 전용 행동 규칙·도구 매핑 |

##### 그룹 C: 📚 Context & Standards (모든 agent가 참조)

| 파일 | 역할 |
| --- | --- |
| **CMDS.md** | WHY & WHAT — 시스템 철학·사용자 컨텍스트·9 카테고리 |
| **🏛 CMDS Guide.md** | STANDARDS — Properties v2, 템플릿, naming |
| **🏛 CMDS Head Quarter.md** | WHERE — 91 카테고리 네비게이션 허브 |

##### 그룹 D: 🧠 Gobi 페르소나 시스템 (Gobi 앱 전용)

| 파일 | 역할 |
| --- | --- |
| **BRAIN.md** | 구요한 brain profile (사람을 기술하는 grounding source) |
| **BRAIN\_PROMPT.md** | Rules of Engagement (BRAIN.md 사용 메타 지침) |

#### 4. 공개 vs 비공개 — system.cmdspace.work

8개 중 **공개 가능한 5개** (그룹 A·C) 가 [system.cmdspace.work](https://system.cmdspace.work)에 배포:

* CLAUDE.md / AGENTS.md / CMDS.md / 🏛 CMDS Guide / 🏛 CMDS Head Quarter
* + `.claude/rules/` 7개 공유 규칙
* + `CMDS-System-Files.zip` 번들

비공개 3개:

* ANTIGRAVITY.md (Gemini 전용 — vendor-specific)
* BRAIN.md / BRAIN\_PROMPT.md (Gobi 페르소나 — product 전용)

→ 학생이 자기 버전을 만들 때는 **CLAUDE.md / AGENTS.md / CMDS.md / Guide / HQ** 5개로 시작 권장.

#### 5. 학생 적응 가이드 — 자기 시스템 파일 만들기

1. **그대로 시작**: cmds-vault 클론 → CLAUDE/AGENTS/CMDS/Guide/HQ 그대로. 처음엔 *변경 X*. 1–2주 사용하며 *어디가 본인과 안 맞는지* 관찰
2. **CMDS.md 부분 수정**: 100–900 카테고리 중 본인 도메인에 *없는 것 제거*, *없는 것 추가*
3. **BRAIN.md 작성** (Session 1 4부 실습으로 이어짐): Claude Code 온보딩 인터뷰로 *본인 페르소나* 캡처
4. **자기 버전 8 시스템 파일 정착**: 6개월 사용 후, 안정된 본인 시스템으로 정립

Concept 07 · 📚 620

### AI 협업 환경 — Chat UI · API · CLI

**세션 매핑**: Session 1 3부 도입 — *왜 Claude Code를 쓰는가* · **한 문장**: AI 사용 환경은 3 단계, 그중 PKM·볼트 작업의 정점은 CLI다.

⭐ Key Takeaway

Chat UI는 시작점, API는 자동화, CLI는 *볼트 전체를 컨텍스트로 다루는 유일한 환경*이다. AI 전문가들은 모두 CLI에 머문다.

#### 1. 3 단계 비교

| 단계 | 환경 | 진입 난이도 | 강점 | 약점 |
| --- | --- | --- | --- | --- |
| **1. Chat UI** | ChatGPT / Gemini / Claude 웹 | ★ 쉬움 | 빠른 시작, 누구나 | 파일 첨부 한계, 볼트 통합 X |
| **2. API** | OpenAI / Anthropic / Google API | ★★★ 개발자 | 자동화·서비스 통합 | 코딩 필요 |
| **3. CLI** | **Claude Code** / Codex / Gemini CLI | ★★ 중간 | **볼트 전체를 컨텍스트로** + 도구 사용 + 멀티스텝 추론 | 까만 화면 거부감 |

#### 2. 1단계 — Chat UI (모두가 시작한 곳)

* 가장 사용성 높음. 90%의 사람이 여기서 시작
* 한국에서 ChatGPT가 압도적, Gemini·Claude·Grok 추격
* 이미지 첨부, 파일 1–2개 첨부 가능
* 한계: *볼트 1만 노트*를 한 번에 컨텍스트로 줄 수 없음

#### 3. 2단계 — API

* 서비스 ↔ AI 간 *프로그램적 통신*
* 처방전처럼 *표준화된 요청·응답*
* 일관된 결과, 자동화 가능
* 코딩 필요 (Python·JavaScript 등)

#### 4. 3단계 — CLI ⭐ Claude Code

* 까만 화면에 흰 글씨 (MS-DOS 같은 터미널)
* 진입 곡선: 처음 무섭지만 *3시간이면 적응*
* **체급이 다름**:
  + *내 컴퓨터의 모든 파일*에 접근 가능
  + 볼트 전체를 컨텍스트로
  + 멀티스텝 추론 + 자기 계획 수립
  + 미리 만든 *스킬* (서브 에이전트) 자동 호출
  + 여러 에이전트 *병렬* 실행

##### 사용자 발언 인용

> "CLI를 안 쓰는 AI 전문가는 가짜다."
> "전 세계 AI를 극단적으로 쓰시는 분들은 다 이걸 쓰고 있다."

##### CLI에서만 가능한 작업

* "내 만 개 노트 다 읽고서, LG 관련 미팅을 시기별 연표로 정리해" — 1–2분
* "내 발행 글 publish=true 만 학습한 다음, 더베러 스타일로 글 한 편 써" — writer 스킬 자동 호출
* "이 PPT 읽고서 옵시디언 마크다운으로 변환해서 적절한 폴더에 저장해" — 파일 시스템 직접 조작
* "이 데이터 분석하고, 통계 돌리고, 결과 페이지 만들어" — Python·R 직접 실행

#### 5. CLI 거부감 해소 — 비개발자를 위한 경로

##### 옵션 A: Claudian 옵시디언 플러그인

* 옵시디언 UI 내에서 Claude Code 작동
* 윈도우 스위칭·터미널 진입 없이 사용
* 추천 대상: CLI 처음 진입, *옵시디언이 익숙해진* 학생

##### 옵션 B: Gobi Desktop

* GUI 기반 AI 비서
* 옵시디언 볼트 자동 인식
* 추천 대상: CLI 자체가 부담스러운 학생, 3주차 이후 본격 사용

##### 옵션 C: Claude Code 직접

* 정통 경로. 익숙해지면 가장 강력
* macOS·WSL2 윈도우에서 가장 잘 작동

#### 6. 5 모델 비교 — 어디에 무엇을 쓸 것인가

| 모델 | 강점 | 적합 작업 | 비용 (월) |
| --- | --- | --- | --- |
| **ChatGPT** (GPT-5.4 PRO) | 논리·추론·구조 설계 | 기획, 메모리 우수 | 27만원 (Pro) |
| **Gemini** (3.1 Pro / Deep Think) | 구글 서비스 연동, 글쓰기 변호사 자문급 | 구글 검색·문서, 딥리서치 | 36만원 (Ultra) |
| **Claude** (Opus 4.0 / Code) | 글쓰기·시각화·**CLI 최강** | Claude Code, HTML/React | 사용량 기반 |
| **Grok** (XAI) | 속도 + X 데이터 + 자연 언어 | 최신 트렌드·뉴스 | $300 |
| **Perplexity** | 팩트 체크, 검색 기반 | 사실 검증, 학술 검색 | 27만원 |

→ **사용자 구독 = 월 200만원** = 1인 인건비. 단, 100명 역할.

→ 학생 권장: 본 코호트 시작 시 **Claude Code** + **ChatGPT 또는 Gemini** 무료/저가 1개로 시작. 익숙해지면 전문성 영역에 맞춰 확장.

Concept 08 · 📚 601

### 멀티볼트 컨셉 — mothership + satellite

**세션 매핑**: Session 1 5부 — *2주차 LLM Wiki 위성 볼트 추가 예정 사전 안내* · **한 문장**: 한 볼트로 모든 걸 담을 수 없다.

⭐ Key Takeaway

메인 볼트는 *모든 작업의 기반(substrate)*, 위성 볼트는 *특정 목적의 격리 공간*. 분리의 5가지 힘(주저자·합의·수명·도구·검색)이 새 볼트 결정을 이끈다.

#### 1. 왜 한 볼트로 안 되는가

##### 사용자(구요한)의 7-볼트 생태계 (2026-04 기준)

| Type | Vault | 멤버 | Purpose |
| --- | --- | --- | --- |
| 🌍 Mothership | CMDSPACE\_Local\_MBP | 구요한 | 모든 작업의 substrate |
| 🛰 Compiled Satellite | CMDS\_LLM\_Wiki | 구요한 + LLM | 학습·연구·정리 (Karpathy 패턴) |
| 🤖 Personal Product | CMDS\_Gobi | 구요한 | 고비 데스크탑 개인 사용 |
| 🤝 Pair | CMDS\_JoonLab | 구요한 + 박준 | 교육·강의·컨설팅·코칭 |
| 🤝 Pair | CMDSPACE\_Admin | 구요한 + 이태극 | 운영 총괄 |
| 👥 Team (5인) | GOBI | 5인 팀 | 커맨드스페이스 × 고비 팀 |
| 📤 Distribution | cmds-vault | 구요한 → 외부 | CMDS 스타터킷 (학생 클론용) |

##### 분리의 5가지 힘 (5 Forces)

새 볼트를 *언제 만들어야 하는가*의 결정 기준:

1. **주저자 분리** — 사람 vs LLM, 개인 vs 협업 (Contamination Mitigation)
2. **합의 모델 분리** — Solo / Pair / Team / Public 의 git·sync 충돌 방식이 다름
3. **수명 분리** — Permanent vs Project-bound vs Time-boxed
4. **도구 분리** — vault 별 plugin / hook / `.claude/` 다를 수 있음
5. **검색 인덱스 분리** — qmd collection 단위로 분리 가능

#### 2. Karpathy LLM Wiki 패턴

##### 컨셉

* Andrej Karpathy의 *LLM Wiki 아이디어*: AI가 외부 자료를 ingest 하고 *지속 가능한 위키*를 컴파일
* 마더십과 분리하여 *LLM 주저자*의 위키만 담는 위성

##### 3-Layer 구조

structure

```
[Raw Sources]   →   [Wiki]          →   [Queries]
(immutable)         (LLM-maintained)    (synthesized)
원본 자료           정제된 wiki 페이지   대화/질의 결과
```

* **Raw Sources**: 외부 아티클·논문·전사본 (수정 불가)
* **Wiki**: LLM이 수집된 자료에서 합성한 *재사용 가능한* 위키 페이지
* **Queries**: 사용자가 LLM과 대화한 답변 — *위키 가치 있으면 wiki로 file back*

#### 3. 코호트 1기 권장 구조 — 단계적 도입

##### 1주차 (5/2)

* **메인 볼트만**: cmds-vault 클론 → 자기 컨텍스트로 채우기
* 멀티볼트 *컨셉만* 노출 (이 자산이 그 노출)

##### 2주차 (5/9) ⭐ 위성 볼트 추가

* **CMDS\_LLM\_Wiki 위성 볼트** 추가 생성
* 메인은 *PKM 작업본*, 위성은 *학습·연구 컴파일*
* 분리 이유: AI가 만든 노트와 본인이 만든 노트를 *섞지 않기 위해*

##### 3주차+ (선택)

* 팀 협업 볼트 (Pair / Team) — 본인 도메인이 협업 중심이면
* Personal Product 볼트 — Gobi Desktop 등 본격 사용 시

#### 4. Anti-pattern — 새 볼트 *만들지 말 것*

다음은 **새 볼트 만들지 말고 마더십 처리**:

| 상황 | 권장 처리 |
| --- | --- |
| 단순 카테고리 분리 | 마더십의 9 카테고리로 충분 |
| 임시 프로젝트 | `00. Inbox/` 또는 마더십의 project 폴더 |
| 혼자 쓰는 새 도메인 | 마더십의 새 subcategory 추가 |

→ "새 볼트는 *governance가 다를 때만*. 단순 분류는 폴더·메타로." — 사용자

#### 5. 학생용 멘탈 모델 — 단순화

학생이 처음 멀티볼트를 들으면 부담스러울 수 있음. *최소 모델*:

mental-model

```
[메인 볼트]                    [LLM Wiki 위성]
                               (2주차에 추가)
- 일상 PKM                  vs - 학습·연구·정리
- 회의·미팅·일기              - AI가 컴파일한 개념 위키
- 개인 산출물                  - Raw 자료 + Wiki 페이지
- 자기 손으로 작성             - LLM이 주저자

→ 헷갈리면? 일단 메인에 다 쌓고, 시간 지나서
   *LLM이 정리할 만한 것* 만 위성으로.
```

CMDS 9 카테고리

## 100 → 900 — 자기 분류 청사진.

도서관 Decimal System 모방. 학생은 *그대로 따라할 필요 없음* — 자기 도메인에 맞춰 단계적으로 적응.

100

Themes

관심사 / 토픽 / 변수 / 용어

200

Literature

개념 · 프레임워크 · 리뷰 · 책

300

Data

데이터 관리 · 설문 · 패널 · LMS

400

Methodologies

연구방법 · 통계 · ML · 코드 · 프롬프트

500

Products

Obsidian · ChatGPT · Claude · n8n

600

Specialties

PKM · Second Brain · GenAI · 생산성

700

Creatives

YouTube · SNS · 음악 · 디자인

800

Outputs

논문 · 강의 · 컨설팅 · 프로젝트

900

Divisions

9개 운영 부문 (KM · 교육 · 컨설팅 등)

Guides · 2

## 실습 가이드 — Session 1 4부 (25분).

강의 시간엔 *흐름 보여주기*에 집중. 각 가이드는 학생이 **강의 후 자가 진행**할 수 있게 작성됨. 막히면 카톡방 / office hour.

[G1 · 5분

### cmds-vault 클론 가이드

Mac / Win 분기
WSL2 권장
Claudian 옵션

git clone 명령부터 옵시디언 vault 열기까지. 한글 경로 회피, 권한 이슈, 시스템 파일 8개 검증, CLI 거부감 학생용 Claudian 플러그인 옵션.](#guide-01-detail)
[G2 · 15분 ⭐

### Claude Code 온보딩 인터뷰 가이드

인터뷰 5 배치 × 12 질문
BRAIN.md 자동 작성
100 Themes stub 5–10개

cmds-vault 클론 후 `claude` 진입 → "cmds onboarding" 한 마디로 발동. 각 배치당 1–2개만 답해도 컨텍스트 누적. BRAIN.md + 100 Themes stub 자동 생성.](#guide-02-detail)

G1 · cmds-vault 클론 가이드

## cmds-vault 클론 — 5분.

#### 0. 사전 체크리스트 (학생용)

* 옵시디언 설치 완료 ([obsidian.md](https://obsidian.md/))
* git 설치 완료 (Mac은 보통 기본, Win은 [Git for Windows](https://git-scm.com/download/win))
* 터미널 진입 가능 (Mac: 터미널 / Win: PowerShell 또는 WSL2)
* 사용자 디렉터리에 한글 없음 (Win 사용자 권장)

→ 위 중 하나라도 막히면 **태극 영상** (카톡방 공유) 우선 참고.

#### 1. 클론 명령 (Mac · Linux · WSL2 공통)

bashCopy

```
cd ~
mkdir -p Documents
cd Documents
git clone https://github.com/johnfkoo951/cmds-vault.git
```

→ 결과: `~/Documents/cmds-vault/` 폴더에 모든 파일 다운로드 완료.

#### 2. Windows (PowerShell — WSL2 미사용 시)

powershellCopy

```
cd $HOME
mkdir Documents -Force
cd Documents
git clone https://github.com/johnfkoo951/cmds-vault.git
```

⚠️ 사용자명에 한글이 있으면 *경로 이슈*. WSL2 권장.

#### 3. Windows + WSL2 (권장)

WSL2가 셋업돼 있으면 Mac과 동일하게 진행. Windows 파일 탐색기에서 `\\wsl$\Ubuntu\home\<사용자명>\Documents\cmds-vault`로 접근 가능.

#### 4. 옵시디언에서 볼트 열기

1. 옵시디언 실행
2. 첫 화면 (또는 좌측 하단 *Vault Switcher*) → **"Open folder as vault"**
3. 방금 클론한 `cmds-vault` 폴더 선택
4. **"Trust author and enable plugins"** 체크 → 신뢰
5. 첫 진입 시 `🏛 CMDS Head Quarter` 노트가 뜸

#### 5. 첫 투어 (강의 시간 5분 라이브) — 10개 numeric 폴더

| 폴더 | 역할 |
| --- | --- |
| `00. Inbox/` | 미정리 캡처 (일자 노트, 클리핑, AI 산출) |
| `10. CMDS Process/` | Connect → Merge → Develop → Share 파이프라인 |
| `20. Literature Notes/` | 외부 지식 정리 |
| `30. Permanent Notes/` | 영구 노트 (evergreen) |
| `40. Docs/` | 기술 문서 |
| `50. Assets/` | 재사용 자원 |
| `60. Collections/` | 사람·미팅·환경 |
| `70. Outputs/` | 최종 산출물 |
| `80. References/` | 참고 자료 |
| `90. Settings/` | 템플릿·스킬·에이전트 설정 |

#### 6. 시스템 파일 8개 확인

볼트 루트(`cmds-vault/` 직속)에 다음 파일 존재 확인:

* `CLAUDE.md` · `AGENTS.md` · `ANTIGRAVITY.md`
* `CMDS.md` · `🏛 CMDS Guide.md` · `🏛 CMDS Head Quarter.md`
* `BRAIN.md` · `BRAIN_PROMPT.md`

→ 8개 다 있으면 정상. 빠진 게 있으면 `git pull` 또는 다시 클론.

#### 7. 자주 발생하는 문제

##### (a) "git: command not found" (Mac)

bashCopy

```
xcode-select --install
```

→ 개발자 도구 설치 후 git 자동 활성화.

##### (b) 한글 경로 깨짐 (Windows)

* Git for Windows 설치 시 **UTF-8 옵션** 선택
* 또는 사용자 폴더 자체를 영어로 (`C:\Users\Yohan` 처럼)
* 그래도 안 되면 **WSL2**로 이동

##### (c) 권한 에러 (Mac/Linux)

bashCopy

```
sudo chown -R $(whoami) ~/Documents/cmds-vault
```

#### 8. CLI 거부감 학생용 — Claudian 플러그인

터미널 자체가 부담스러운 학생을 위한 *옵시디언 UI 내 Claude Code* 솔루션:

1. 옵시디언 → Settings → Community plugins → Browse
2. **Claudian** 검색 → 설치 → Enable
3. Claudian이 옵시디언 사이드바에 Claude Code 패널 제공
4. 터미널 진입 없이 *옵시디언 안에서* Claude 명령 실행 가능

→ 단, *완전한 CLI 경험*은 직접 터미널 사용이 더 강력. Claudian은 *진입 단계 보조*로만.

G2 · Claude Code 온보딩 인터뷰 가이드

## cmds-onboarding — 15분 인터뷰로 본인 컨텍스트 채우기.

**✅ 스킬 위치 확정**: `cmds-vault/90. Settings/91. Skills/cmds-onboarding/SKILL.md`
학생은 cmds-vault 클론 후 `claude` 진입 → "cmds onboarding" 또는 "온보딩" 한 마디로 발동.

#### 0. 이 실습의 목적 — 한 줄

⭐ 목적

cmds-vault의 placeholder들을 *내 컨텍스트*로 채워서, 12주 동안 함께할 *내 볼트*로 만든다.

#### 1. 사전 준비

* G1 클론 가이드 완료 (볼트가 옵시디언에서 열림)
* **Claude Code 설치 완료**:
  + Mac: `npm install -g @anthropic-ai/claude-code`
  + Win: WSL2 권장. 그 외 환경은 태극 영상 참조
  + 또는 Claudian 플러그인 (옵시디언 UI 내)
* Anthropic 계정 + API 또는 Claude.ai 구독

#### 2. Claude Code 첫 실행

bashCopy

```
cd ~/Documents/cmds-vault     # 볼트 폴더로 이동
claude                          # Claude Code 실행
```

→ 첫 실행 시 로그인 / API 키 설정 안내. 따라서 진행.

#### 3. 온보딩 인터뷰 발동

볼트 폴더에서 Claude Code 진입 후 다음 중 한 마디:

promptCopy

```
cmds onboarding
```

또는 `온보딩`, `내 컨텍스트로 채워줘`, `fill my vault`, `interview me`

→ Claude가 자동으로 **`cmds-onboarding` 스킬** 발동. 5 배치(A–E)에서 12개 질문을 *나누어* 던짐. **모든 질문에 답할 필요 없음** — 각 배치당 1–2개만 답해도 됨.

#### 4. 인터뷰 질문 5 배치

##### Batch A — 현재 도구·환경 (3 질문)

1. 어떤 도구로 지식을 관리하나요? (Notion / Evernote / Apple Notes / 종이 / 아직 없음)
2. 파일은 어디에 사나요? (클라우드 / 로컬 / 혼합)
3. AI는 얼마나 자주 쓰나요?

##### Batch B — 도메인·전문성 (3 질문)

4. 본인의 도메인을 1–2 문장으로?
5. 도메인 안에서 AI가 *약한* 영역은?
6. 도메인의 *핵심 키워드 2–3개*는?

##### Batch C — 잃기 싫은 정보 (2 질문)

7. 6개월 후 *절대 잃기 싫은 정보 1개*는?
8. 어떤 종류의 인풋을 가장 많이 잡고 싶나요? (아티클 / 미팅 / 책 / 대화 / 본인 아이디어 / 데이터)

##### Batch D — 12주 지향점 (2 질문)

9. 12주 동안 이 볼트로 *만들어내고 싶은 산출물*은?
10. PKM Mission 한 줄로?

##### Batch E — 톤·공유 (2 질문)

11. 누가 이 노트를 읽나요? (나만 / 동료 / 팀 / 공개)
12. 톤은? (격식 / 캐주얼 / 한국어 / 영어 / 혼합)

⚠️ **모든 질문에 답할 필요 없음**. 각 배치당 1–2개만 답해도 컨텍스트가 누적됨.

#### 5. 인터뷰 결과로 채워지는 것들 (Step 1–7)

| 단계 | 결과 |
| --- | --- |
| Step 0 | 사전 체크 (Claude Code · BRAIN.md · `[[Me]]` placeholder 상태) |
| Step 1 | 학생이 author wikilink 결정 (`[[홍길동]]` 같은 형식) |
| Step 2 | `[[Me]]` → `[[<선택 이름>]]` 일괄 치환 (vault 전체) |
| Step 3 | 페르소나 인터뷰 5 배치 (5–8분) |
| Step 4 | **BRAIN.md** 자동 작성 — 7가지 관심 영역 + How I Use This Vault + Pinned |
| Step 5 | **30. Permanent Notes/**에 5–10개 theme stub 자동 생성 — 각 stub에 `CMDS: [[📚 10X]]` 메타 부여 |
| Step 6 (선택) | **CMDS.md** Vault Operator 섹션 자동 작성 |
| Step 7 | 마무리 + 다음 단계 (`/status` / `/connect` 시도) |

→ 결과 검토 후 *수정 가능*. Claude가 만든 게 *최종*이 아님 — 본인이 *조정·보완*.

→ 스킬은 자동으로 **Resume Logic** 수행. "이어서 하자" / "온보딩 이어서" 라고 하면 어디까지 했는지 grep으로 자동 진단 후 재개.

#### 6. 라이브 시연 시간 분배 (15분)

| 분 | 강사·학생 |
| --- | --- |
| 0–2 | (강사) Claude Code 실행 + "cmds onboarding" 입력 |
| 2–3 | (강사) 첫 질문 등장 — 강사가 본인이라면 어떻게 답할지 시연 |
| 3–8 | (학생) 본인 Claude Code에서 동일 발동 → 1–2개 질문에 답변 |
| 8–11 | (학생) Claude가 BRAIN.md 일부 채우는 모습 관찰 |
| 11–13 | (강사) 결과물 점검 — 어떤 노트가 만들어졌는지 보여주기 |
| 13–15 | "디테일은 집에서 마저" 마무리 + 과제 안내 |

⚠️ **15분 안에 다 끝낼 필요 없음**. *어떻게 진행되는지 감 잡는 게* 1차 목적. 디테일은 과제.

#### 7. 과제 (Session 1 → Session 2 사이)

##### 필수 (모든 트랙)

* 온보딩 인터뷰 *나머지 질문에 답변*
* **BRAIN.md**가 본인 컨텍스트로 어느 정도 채워졌는지 확인 — 부족하면 직접 수정
* **100 Themes**에 본인 도메인 핵심 키워드 5–10개 stub 노트 등록
* *볼트가 본인 컨텍스트로 살아있는 상태* 유지 — Session 2 입력

##### Advanced (3명)

* CMDS.md의 9 카테고리 중 본인 도메인에 *없는 것 제거 / 추가* — 자기 버전 작성

##### 비동기 (다시보기 2명)

* BRAIN.md 1차 작성본을 카톡방에 공유 → 운영진 1:1 피드백

#### 8. 자주 발생하는 문제

##### (a) Claude Code가 온보딩 스킬을 못 찾음

* `90. Settings/91. Skills/cmds-onboarding/SKILL.md` 파일 존재 확인
* 없으면 `git pull origin main`

##### (b) Claude의 답이 *이상함*

* 가능: 컨텍스트 부족 → 1–2개 질문에 *조금 더 구체적으로* 답해보기
* 가능: API 한도 초과 → Claude 프로 결제 또는 잠시 대기

##### (c) 한국어 답변이 *AI스러움*

* 정상. 1차 결과는 *템플릿 채우기* 수준
* 2주차 *Compounding* 단계에서 본인 어조로 다듬어 갈 것

## 지금 바로 시작 — 4단계.

강의 직전·직후 어디서든. 위에서 아래로 따라가기만 하면 됩니다. 각 명령은 우상단 *Copy* 버튼으로 복사 가능.

1
cmds-vault 클론

Copy

```
git clone https://github.com/johnfkoo951/cmds-vault.git ~/Documents/cmds-vault
```

2
옵시디언에서 vault 열기

옵시디언 실행 → "Open folder as vault" → `~/Documents/cmds-vault` 선택 → "Trust author and enable plugins" 체크

3
Claude Code 진입

Copy

```
cd ~/Documents/cmds-vault && claude
```

4
온보딩 인터뷰 발동 (15분)

Copy

```
cmds onboarding
```

→ 5 배치 × 12 질문. **각 배치당 1–2개만 답해도 OK**. BRAIN.md + 100 Themes stub 자동 생성.

W1 과제 · Session 2 입력 준비

## 집에서 마저 하기 — Session 2의 입력.

강의 시간엔 *흐름 보기*까지. 디테일 채우기는 한 주 동안 천천히. Session 2 (5/9) 입력은 **지금 채운 BRAIN.md + 100 Themes stubs**.

필수 (모든 트랙)

### 1. CMDS 볼트 온보딩 완료

실습에서 시작한 온보딩 인터뷰를 *집에서 마저 진행*. 결과: BRAIN.md / 100 Themes의 placeholder가 자기 컨텍스트로 채워진 상태. 자기 도메인 핵심 키워드 5–10개를 stub 노트로 등록.

필수

### 2. Session 2 사전 준비

Claude Code 설치 시도 (Anthropic 가이드 + 태극 영상). 본인 볼트가 *온보딩 데이터로 채워진 상태* 유지 — Session 2의 입력.

Advanced (3명)

### 3. 케이스 발표 준비

Session 3 본인 PKM 케이스 발표 5분 분량 초안 + 자기 시스템 vs cmds-vault 비교 메모.

비동기 (다시보기)

### 4. BRAIN.md 카톡방 공유

녹화본 시청 후 BRAIN.md 1차 작성본을 카톡방에 공유 → 운영진 1:1 피드백.

참고 자료

## 파고들 사람을 위한 레퍼런스.

강의 후 더 깊이 파고들고 싶은 학생을 위해. cmds-vault 안의 시스템 파일 5종, 공개 배포 페이지, 사용자(구요한) 작성 발행 에세이.

[📚

system.cmdspace.work

CMDS 시스템 파일 5종 + 7개 rules + ZIP 번들 — 공개 canonical](https://system.cmdspace.work)
[🐙

github.com/johnfkoo951/cmds-vault

스타터 볼트 — 8 슬래시 커맨드 + 7 rules + cmds-onboarding · gobi-onboarding 스킬 포함](https://github.com/johnfkoo951/cmds-vault)
[🟪

obsidian.md

옵시디언 다운로드 — Mac · Win · Linux · iOS · Android](https://obsidian.md/)
[🤖

Anthropic Claude Code 공식 가이드

설치 + 첫 실행 + Authentication. `npm install -g @anthropic-ai/claude-code`](https://docs.anthropic.com/claude-code)
[🐪

Gobi Desktop

3주차부터 본격 사용. 옵시디언 볼트를 Brain Page로 발행. CLI 거부감 학생용 대안.](https://gobi.app)

다음 — Session 2 (5/9 토)

## "시키기"가 아니라 "쌓기 (Compounding)".

매번 같은 일을 다시 시키지 말고, 잘 된 프롬프트를 **프롬프트 → 스킬 → 워크플로우**로 복리처럼 누적합니다. W1 산출물(BRAIN.md + 100 Themes stubs)이 W2 입력. 책쓰기 가설은 코호트 후반에 다시 도입.

🔀

#### 1부 AI + PKM 이론 (45분)

챗봇 vs 에이전트 / CLI×PKM 적합성 / Compounding 3단계 / AI+PKM 파이프라인 (Capture · Process · Connect · Distill · Express)

🛠

#### 2부 Claude Code 도구 (45분)

설치 + 첫 실행 / cmds-vault AI 자산 투어 / 첫 Distill 프롬프트 / 프롬프트 쌓기 (Compounding 첫 한 줄)

📝

#### 3부 실습 (30분)

"내 stub → Permanent Note 단락" 1편 작성 + Compounding 프롬프트 1–3개 저장 → `90. Settings/92. Prompts/`

## 강의가 끝나도 자료는 그대로 있어요.

이 페이지는 코호트 종료 후에도 영구 유지됩니다. 12주 동안 막힐 때마다 돌아오세요. 시스템 파일은 system.cmdspace.work, 스킬은 cmds-vault 에서 항상 최신 버전으로.

[지금 시작](#quickstart)
[GitHub ↗](https://github.com/johnfkoo951/cmds-vault)
[system.cmdspace.work ↗](https://system.cmdspace.work)

![CMDSPACE](/assets/logos/cmds-logo-typo-black.png)
![CMDSPACE](/assets/logos/cmds-logo-typo-white.png)

Command your space.

© 2026 CMDSPACE · 구요한 + 김진영 · CMDS × GOBI Cohort 1기

[cmds-vault](https://github.com/johnfkoo951/cmds-vault)
[System Files](https://system.cmdspace.work)
[Gobi](https://gobi.app)
[Obsidian](https://obsidian.md)
