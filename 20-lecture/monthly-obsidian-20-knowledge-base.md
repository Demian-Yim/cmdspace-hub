---
title: monthly-obsidian-20-옵시디언을-지식베이스로
source: https://labs.cmdspace.work/monthly-obsidian-20/
author: 구요한 (CMDSPACE)
fetched: 2026-08-28
note: markitdown HTML→MD 자동 변환 스냅샷. 정확한 원문은 source URL 참조.
---

[![CMDSPACE](cmds-logo-round.png)CMDSPACE 월간 옵시디언](https://cmdspace.work)

[여섯 계약](#contracts)
[솔루션](#solutions)
[검색 설계](#design)
[자료실](#resources)
테마
[신청하기](https://class.cmdspace.kr/channels/L2NoYW5uZWxzLzE3Njkx/C00007/classes/153252/information)

Monthly Obsidian #20 · 2026-08-26 (수) 19:30–21:30

# 옵시디언을 지식 베이스로 쓰는 법

AI Agent를 위한 설계 — Agentic Memory와 옵시디언, 무엇이 다르고 어떻게 쓰면 좋을까

20회차에서 다룬 내용의 후속 자료 페이지입니다. Agentic Memory의 해부, Mem0·Honcho·Cognee 등 솔루션 비교, 옵시디언 볼트가 이 지형에서 서는 자리, 그리고 Markdown + YAML로 지식을 쌓고 다시 찾는 검색 설계까지 — 강의에서 소개한 프레임, 공식 링크, 논문, 그리고 제 해석을 한 페이지에 정리했습니다.

[월간 옵시디언 신청 페이지](https://class.cmdspace.kr/channels/L2NoYW5uZWxzLzE3Njkx/C00007/classes/153252/information)
[CMDS 스타터킷 받기](https://github.com/johnfkoo951/cmds-vault)

## 01 · 오늘의 결론세 문장이면 충분합니다

"에이전트 메모리는 저장소가 아니라 운영 계약이다.
그리고 그 계약의 정본은 이미 당신의 볼트에 있다."

* **층이 다르다.** Agent Memory와 옵시디언은 경쟁 관계가 아닙니다. Memory 제품들은 요약·추출·프로필을 다루는 *파생층*이고, 여러분의 볼트는 사람이 읽고 고치고 git으로 이력이 남는 *정본층*입니다. 정본이 파생층을 이깁니다.
* **계약으로 심사한다.** 어떤 메모리 제품이든 아래 여섯 가지 질문(Write · Reconcile · Retrieve · Correct · Forget · Audit)에 답할 수 있어야 합니다. 하나라도 못 답하면 기억 시스템이 아니라 "검색 가능한 부산물 저장소"입니다.
* **업계가 옵시디언 방식으로 수렴 중이다.** 2026년, git 기반 컨텍스트 저장소(Letta), 파일 기반 에이전트 메모리(Anthropic), markdown+YAML 지식 스펙(Google OKF)까지 — 사람이 읽고 diff할 수 있는 마크다운으로 모이고 있습니다. 옵시디언 사용자는 이미 도착해 있습니다.

## 02 · 개념 정리RAG · 위키 · 메모리는 다른 질문에 답한다

셋은 경쟁 기술이 아닙니다. 잘 지은 시스템은 셋을 층으로 쌓지, 하나로 나머지를 대체하지 않습니다.

|  | 비유 | 처리 시점 | 하는 일 | 쓰기와 검증 |
| --- | --- | --- | --- | --- |
| **RAG** | 사서 — 질문마다 서가에서 책을 찾아 옴 | 질의 시점 (매번) | 근거를 검색해 조립, 답은 세션과 함께 소멸 | 읽기 전용 |
| **Compiled Wiki** | 편집자 — 읽은 것을 백과사전 항목으로 정리 | 인제스트 시점 (한 번) | 컴파일해 유지, 좋은 답은 위키로 환류 (축적·compounding) | 사람 게이트 + git |
| **Agentic Memory** | 비서의 수첩 — 겪은 일에서 배운 것을 적어 둠 | 상호작용 시점 | 대화·실행 경험에서 자동 추출, 다음 세션에 회수 | **자동 쓰기 — 검증 최약** |

함정 주의: 위키를 읽는 것도 retrieval입니다. 진짜 결정할 것은 "무엇을 매번 최신 원문에서 찾고, 무엇을 검토된 파생 지식으로 유지할 것인가"입니다.

## 03 · 심사 도구여섯 단계의 계약 체크리스트

메모리 제품을 살 때도, 자기 시스템을 진단할 때도 같은 여섯 질문을 던지세요.

1. **Write** 어떤 관찰과 결과를, 누가 영구 기억으로 승격할 수 있는가?
2. **Reconcile** 새 정보가 기존 기억과 충돌할 때 — 덮어쓰기, 병합, 시간 버전 중 무엇을 적용하는가?
3. **Retrieve** 사람·작업·시간 범위를 거른 뒤에 관련 근거를 회수하는가?
4. **Correct** 잘못된 사실과 추론을 원문까지 추적해 수정할 수 있는가?
5. **Forget / Delete** 지우면 진짜 지워지는가 — 요약, 임베딩, 그래프, 캐시까지 전파되는가?
6. **Audit / Recover** 출처·행위자·모델·버전·변경 이력을 재구성하고, 내보내고, 복구할 수 있는가?

"하나라도 답할 수 없으면 그것은 기억 시스템이 아니라,
검색 가능한 부산물 저장소다."

정직성 노트: 이 여섯 질문을 제 시스템(CMDS)에 들이대도 Forget/Delete 하나는 빈칸입니다. 이 체크리스트는 제품 심사용이기 전에 자기 시스템 진단용입니다.

### 옵시디언 사용자에게 — 2·2·2

"정본이 있으니 마음 놓아도 되나?" — **반만 맞습니다.** 마음 놓아도 되는 것은 제품 선택(벤치마크 경쟁을 쫓아다닐 필요도, 정본을 옮길 이유도 없습니다), 마음 놓으면 안 되는 것은 운영 규율입니다. 여섯 계약을 볼트에 대면 정확히 둘·둘·둘로 갈라집니다.

| 구분 | 계약 | 챙길 것 |
| --- | --- | --- |
| ✅ 공짜 2 | **Correct · Audit** | 파일 편집 + git 이력이 곧 구현체 — 파일 기반의 구조적 이점. git(또는 버전 백업)만 켜두면 됩니다. |
| ⚠️ 당신 몫 2 | **Write · Retrieve** | Write: 에이전트가 볼트에 자동으로 쓰면 정본이 오염됩니다 — 에이전트 산출물 레인(인박스) 분리, 정본 승격은 사람 게이트, AI 작성 노트에 model 표기. Retrieve: 정본이 있어도 못 찾으면 없는 것 — description 프로퍼티와 검색 3모드 설계. |
| 📝 숙제 2 | **Reconcile · Forget** | Reconcile: 볼트에도 모순·낡은 노트가 조용히 공존합니다 — 주기적 lint(모순·stale·orphan 점검). Forget: 노트를 지워도 인덱스·임베딩에 잔존합니다 — 주기적 재인덱스, 파생물은 "언제든 날리고 재생성" 원칙. |

정본은 소유가 아니라 관리에서 나옵니다. Mem0 사용자가 벤더에게 묻는 질문을, 옵시디언 사용자는 자기 운영 습관에게 묻습니다 — 질문이 사라지는 게 아니라 수신인이 바뀝니다.

## 04 · 배치 프레임정본/파생 4계층 — "그래서 사야 하나요?"의 답

| 계층 | 소유하는 것 | 원칙 |
| --- | --- | --- |
| **정본층** | 원문 Markdown, 이벤트 원장, 승인된 프로필 | 사람이 읽고 수정하며 Git으로 provenance — **여기가 옵시디언 볼트** |
| **회수층** | BM25 / vector / graph 인덱스 | 정본에서 언제든 재생성 가능 (날려도 됨) |
| **추론층** | 요약, 자동 추출된 사실, persona representation | 가설로 취급 — 자동으로 정본에 쓰지 않음 |
| **실행층** | checkpoint, session state | 런타임 복구용 — 진실 원천으로 승격 금지 |

Mem0·Honcho는 추론층, Cognee는 회수+추론층 제품입니다. 정본이 아닙니다. **정본이 파생층을 이깁니다.**

| 상황 | 우선 접근 |
| --- | --- |
| 원문 문구, 최신 규정, 정확한 출처 위치 | Retrieval (RAG) |
| 여러 소스의 같은 설명을 반복하게 됨 | Wiki 컴파일 |
| "지난번에 뭐라 했더라", 이 사용자의 선호 | Memory |
| 에이전트 실행에서 얻은 교훈 | Memory → 반복 확인되면 Wiki 승격 |
| 다른 시스템·조직으로 내보내기 | OKF 표면 |
| 코퍼스가 작음 | 파일 검색부터 (전부 과잉일 수 있음) |

한 문장 배치: 위키를 정본으로, RAG를 그 위의 검색으로, Memory를 승격 후보 생산자로, OKF를 밖으로 나갈 때의 표면 규격으로.

## 05 · 랜드스케이프솔루션별 정리 — 공식 링크와 제 판정

순위표가 아닙니다. job이 다르면 평가도 분리합니다 — Honcho와 Cognee는 같은 문제의 경쟁자가 아닙니다. 판정은 2026-08 시점 제 시스템 기준의 개인 결정이며, 여러분의 상황에서는 달라질 수 있습니다.

Memory API

Mem0 / OpenMemory

대화에서 사실을 자동 추출하는 범용 memory API. GitHub 58K+ stars, AWS Agent SDK 메모리 프로바이더. "이 사용자에 대해 뭘 아는가"에 답한다. 주의: 해시 기반 중복 제거라 상충 기억이 나란히 축적될 수 있고, 재랭킹은 1차 벡터 recall을 넘지 못한다.

[GitHub](https://github.com/mem0ai/mem0)[공식](https://mem0.ai)[논문](https://arxiv.org/abs/2504.19413)

판정: 정본 대체로는 거절 · 파생층 실험은 가능

Theory-of-Mind

Honcho (Plastic Labs)

peer별 표상 + Dialectic 질의로 "이 사람은 누구이며 무엇을 선호하고 믿는가"를 모델링. 3.0에서 Deriver/Dialectic/Dreamer 3-에이전트 구조. 서버는 AGPL-3.0 (조사 대상 중 유일한 copyleft).

[GitHub](https://github.com/plastic-labs)[Honcho 3.0 발표](https://plasticlabs.ai/blog/posts/Honcho-3)

판정: 보류 — 지금 내 문제가 아니라 미래 문제를 푼다

Graph + Vector

Cognee

문서에서 개체·관계를 추출해 그래프+임베딩 파이프라인을 만든다. 1.0에서 Rust 코어와 Cloud. "어떤 문서·개체·관계가 이 질의와 연결되나"에 답한다. 주의: forget이 raw 업로드까지 지우지 않는다.

[GitHub](https://github.com/topoteretes/cognee)[릴리스](https://github.com/topoteretes/cognee/releases)

판정: 조건부 그림자 실험 — 내 검색이 반복해서 놓칠 때만

Agent Runtime

Letta (MemGPT)

메모리 미들웨어가 아니라 stateful agent 런타임. 2026-02 git 기반 Context Repositories — "파일 기반 수렴"의 대표 신호. 원류는 MemGPT 논문(제한된 컨텍스트를 OS식 메모리 계층으로 관리).

[공식 블로그](https://www.letta.com/blog/)[MemGPT 논문](https://arxiv.org/abs/2310.08560)

참고: working/episodic 계층 분리 아이디어 차용

Temporal Graph

Zep / Graphiti

Zep Community Edition은 유지보수 중단, 오픈소스 역량을 Graphiti(temporal knowledge graph — 사실마다 유효기간 + 신뢰도)에 집중. "언제까지 참이었나"를 그래프에 넣는 접근.

[Graphiti 문서](https://help.getzep.com/graphiti/getting-started/welcome)[전략 발표](https://blog.getzep.com/announcing-a-new-direction-for-zeps-open-source-strategy/)

참고: temporal validity 개념이 배울 점

Managed Graph

Supermemory

관리형 memory graph + 커넥터. 2026-05 "Dynamic Dreaming" 출시 — 백그라운드 기억 재조직 흐름의 한 축.

[공식](https://supermemory.ai)[TechCrunch](https://techcrunch.com/2025/10/06/a-19-year-old-nabs-backing-from-google-execs-for-his-ai-memory-startup-supermemory/)

참고: Dreaming 수렴의 한 사례

Built-in

플랫폼 내장 메모리 — ChatGPT · Claude

ChatGPT "Dreaming"(2026-06): 수동 저장을 백그라운드 합성으로 대체, temporal awareness. Claude: 2026-03 memory 전면 무료 + 타 챗봇 가져오기, Managed Agents는 메모리를 파일시스템의 파일로 저장. Claude Code는 처음부터 CLAUDE.md — "메모리 = 편집 가능한 마크다운".

[Dreaming 보도](https://www.techtimes.com/articles/317840/20260605/chatgpt-memory-dreaming-update-openai-rewrites-personalization-engine-limits-audit-trail.htm)[Claude 메모리 보도](https://sdtimes.com/anthropic/anthropic-adds-memory-to-claude-managed-agents/)

체크: 저장 내용을 읽고·고치고·내보낼 수 있는지 확인

Cloud & Spec

클라우드 3사 + Google OKF

AWS AgentCore Memory, Google Memory Bank, Azure Foundry Memory — 3사 전부 진입, 카테고리가 인프라화. 그리고 Google OKF(Open Knowledge Format, 2026-06): 조직 지식을 YAML frontmatter 달린 Markdown 디렉터리로 패키징하는 벤더 중립 스펙. 필수 필드는 type 단 하나.

[OKF 발표](https://cloud.google.com/blog/products/data-analytics/how-the-open-knowledge-format-can-improve-data-sharing/)[OKF GitHub](https://github.com/GoogleCloudPlatform/knowledge-catalog)[Memory Bank 문서](https://docs.cloud.google.com/gemini-enterprise-agent-platform/scale/memory-bank)

해석: OKF the FORMAT ≠ Knowledge Catalog the PRODUCT — 수렴은 FORMAT 층에서만 참

### 숫자를 믿지 마라 — 벤치마크 읽는 법

* Mem0 자체 논문 안에서도 풀 컨텍스트가 Mem0보다 정확했습니다. Mem0의 실제 가치는 정확도가 아니라 **토큰·지연 절감의 효율 트레이드오프**입니다.
* 한 제품은 사실상 전체 검색이 되는 설정(top\_k=50)으로 벤치마크 100%를 주장했다가 독립 감사에서 60.3%로 반박됐습니다.
* 원칙: **측정 protocol 세대가 다른 숫자는 합산 금지.** 벤더 숫자를 보면 조건부터 물어보세요.

## 06 · 2026년의 수렴업계가 옵시디언 방식으로 오고 있다

2026-01

Honcho 3.0 — Dreaming Agent (백그라운드 기억 합성)

2026-02

Letta — git 기반 Context Repositories

2026-03

Claude — memory 전면 무료 개방 + 타 챗봇 memory 가져오기

2026-04

Anthropic Managed Agents — 메모리를 파일시스템의 파일로 저장 (베타)

2026-05

Supermemory — Dynamic Dreaming

2026-06

ChatGPT Dreaming (수동 저장 → 백그라운드 합성) · Google OKF v0.1 공개

"사람이 읽을 수 있고 git으로 diff할 수 있는 마크다운 —
업계가 수렴하는 그 지점은, 옵시디언 사용자들이 이미 하던 방식입니다."

## 07 · 검색 설계Markdown + YAML로 쌓고, 다시 찾기

### 쌓기 — frontmatter가 곧 검색 설계

* CMDS 7 필수 프로퍼티: `type · aliases · description · author · date created · date modified · tags`
* 그중 **description이 핵심**입니다. 사람용 요약이 아니라 *"AI가 다음 세션에서 이 노트의 관련성을 판단하게 하는 machine-readable hint"* — 영어로, 도구 설명 쓰듯이. (무엇이 들어있고, 언제 참조해야 하는지)
* 시스템 파일(CLAUDE.md류)이 곧 에이전트에게 건네는 설계도: 우선순위(precedence), 정적/동적 분리, 컨텍스트 압축 후에도 살아남는 Essential 블록. 실물 예시는 [system.cmdspace.work](https://system.cmdspace.work)에 전부 공개되어 있습니다.

### 다시 찾기 — 검색 3모드

| 모드 | 무엇 | 언제 |
| --- | --- | --- |
| **lex** (BM25) | 정확한 키워드·구문 매칭 | 용어·파일명·정확한 문구를 알 때 — 빠르고 결정적 |
| **vec** (vector) | 의미 기반 유사도 | 표현은 몰라도 뜻은 알 때, 관련 개념 묶음 발굴 |
| **hyde** | 가설 답변을 먼저 쓰고 그것과 유사한 문서 검색 | 복잡·미묘한 질문, 어휘가 겹치지 않는 질문 |

* **Is Grep All You Need** (Sen 2026): 장기 기억 벤치마크에서 grep(어휘 검색)이 벡터 검색을 일반적으로 상회 — 그리고 **어떤 하네스를 쓰는지가 검색 방법만큼 성능을 좌우**. "마크다운 볼트 + 어휘 검색"이라는 단순한 조합의 첫 정량 근거.
* **MemoHarness** (Huang 2026): 메모리를 프롬프트도 모델도 아닌 **하네스 계층**에 두라. "사고가 나면 CLAUDE.md 규칙으로 증류한다"는 루프의 학술 대응물.
* 단, 재랭킹은 후보를 추가하지 못합니다 — **1차 검색의 recall이 전체 상한**입니다. 어떤 도구를 쓰든 같은 교훈.

## 08 · 보너스이 방향의 끝 — "옵시디언으로 자비스를 만들 수 있나요?"

멀티볼트 옵시디언을 지식 베이스로 하는 개인 Jarvis OS를 6개 모델(ChatGPT ×2 · Gemini ×2 · Grok red-team · Claude)에게 독립 설계시키고 통합한 리서치의 요약입니다.

* **결론: CONDITIONAL GO.** 단, "하이엔드"를 에이전트·DB·대시보드의 수가 아니라 **계약의 강도**(검색 평가 · 단일 쓰기 소유권 · 승인 · 검증 · 복구 · 감사)로 정의할 때만.
* 6개 모델의 강한 합의 1번: **"Markdown/Obsidian이 canonical knowledge이고, 벡터·그래프·agent memory는 파생 상태다."** — 오늘 강의의 4계층 프레임과 같은 결론에 독립적으로 도달.
* 한 문장 정의: "Jarvis OS는 Obsidian을 대체하는 AI 앱이 아니라, 여러 볼트의 Markdown을 정본으로 보존하면서 질문→검색→판단→행동→검증→기록을 안전하게 조정하는 로컬 우선 제어면이다."
* 운영 원칙: 읽기는 병렬, **쓰기는 단일 writer로 직렬**. 에이전트를 많이 붙일수록가 아니라, 쓰기 규율이 좋을수록 지식 베이스가 좋아집니다.
* 첫 단계는 자동화가 아니라 **read-only 검색 평가** — 실제 질문 100개로 내 검색의 recall부터 측정.

## 09 · 자료실논문과 1차 자료

* [LongMemEval (Wu et al., ICLR 2025)](https://arxiv.org/abs/2410.10813)장기 기억 500문항 벤치마크 — 상용·long-context 모두 약 30%p 하락
* [CoALA (Sumers et al.)](https://arxiv.org/abs/2309.02427)Working/Episodic/Semantic/Procedural 4유형 프레임의 원전
* [MemGPT (Packer et al.)](https://arxiv.org/abs/2310.08560)제한된 컨텍스트를 OS식 메모리 계층으로 — Letta의 원류
* [Mem0 논문](https://arxiv.org/abs/2504.19413)자체 논문 안에서 풀 컨텍스트가 더 정확 — 효율 트레이드오프로 읽을 것
* [MINJA — Memory Injection Attack (NeurIPS 2025)](https://arxiv.org/abs/2503.03704)질의만으로 공유 메모리에 독을 심는 공격 성립 — Write 계약의 근거
* [Is Grep All You Need (Sen 2026)](https://arxiv.org/abs/2605.15184)grep이 벡터 검색을 일반적으로 상회 + 하네스가 성능을 좌우
* [MemoHarness (Huang 2026)](https://arxiv.org/abs/2607.14159)메모리는 프롬프트도 모델도 아닌 하네스 계층에
* [Google OKF 발표 (2026-06)](https://cloud.google.com/blog/products/data-analytics/how-the-open-knowledge-format-can-improve-data-sharing/)markdown+YAML 지식 스펙 — §10이 Karpathy LLM Wiki를 인용
* [Karpathy — LLM Wiki 아이디어](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)Raw Sources / Wiki / Schema 3층 패턴의 원전

## 10 · 이어가기오늘 바로 시작할 수 있는 것들

Starter Kit

CMDS 옵시디언 스타터킷

17회차에서 공개한 CMDS 볼트 스타터킷. 7 필수 프로퍼티와 폴더 구조가 세팅된 상태로 시작합니다.

[GitHub](https://github.com/johnfkoo951/cmds-vault)

LLM Wiki Kit

CMDS LLM Wiki 스타터킷

Karpathy LLM Wiki 패턴(Raw Sources → Wiki → Queries)을 옵시디언 위성 볼트로 구현한 템플릿.

[GitHub](https://github.com/johnfkoo951/cmds-llm-wiki)

System Files

CMDS 시스템 파일 공개본

CLAUDE.md·AGENTS.md 등 "AI에게 건네는 설계도" 6종 + 규칙 파일 전문. 오늘 4부에서 다룬 실물입니다.

[system.cmdspace.work](https://system.cmdspace.work)

Assess

AKM Index — 내 시스템 자가진단

에이전틱 지식관리 성숙도를 5기둥 25문항으로 측정하는 공개 루브릭. 여섯 계약을 스스로에게 묻는 다음 단계.

[akm.cmdspace.work](https://akm.cmdspace.work)

Newsletter

더배러 (The Better)

지식관리 × 생성형 AI를 다루는 구요한의 뉴스레터. 오늘 같은 주제가 글로 이어집니다.

[구독하기](https://maily.so/josh)

Community

월간 옵시디언

매달 마지막 주, 옵시디언과 AI 지식관리를 다루는 라이브 세션. 지난 회차는 커뮤니티 [소식] 카테고리에서 다시 볼 수 있습니다.

[신청 페이지](https://class.cmdspace.kr/channels/L2NoYW5uZWxzLzE3Njkx/C00007/classes/153252/information)

## 11 · 아카이브지난 회차들

전체 다시보기는 월간 옵시디언 커뮤니티의 [소식] 카테고리에서.

012025-01 · 옵시디언의 AI 활용

022025-02 · 업무 활용과 공동 지식관리

032025-03 · 옵시디언과 자동화 Part 1

042025-04 · 옵시디언과 자동화 Part 2

052025-05 · 옵시디언 VS 노션

062025-06 · iOS 단축어와 n8n으로 빠른 노트

072025-07 · 동기화(Sync)의 모든 것

082025-08 · Bases Plugin과 Eagle

092025-09 · AI Agent 활용하기 1 (Claude Code 설치부터)

102025-10 · AI Agent 활용하기 2 (나만의 워크플로우)

112025-11 · 연구를 위한 지식관리 비법

122025-12 · 지식관리를 위한 AI Agent 시스템 구축

132026-01 · AI 툴 총집합 + AI 워크플로우

142026-02 · Obsidian X AI Agent 최신 동향

152026-03 · 핵심 플러그인 재정리

162026-04 · 지식의 재활용 — 수집·정리·검색·활용

172026-05 · CMDS 스타터킷 공개 + 전체 Q&A

182026-06 · 멀티볼트 운용의 기술

192026-07 · 언어의 장벽을 넘어서는 옵시디언 X AI

202026-08 · 옵시디언을 지식 베이스로 쓰는 법 (이 페이지)

## 다음 월간 옵시디언에서 만나요

매달 한 번, 옵시디언과 AI 지식관리의 최전선을 두 시간에 정리합니다. 라이브 + 다시보기 제공.

[월간 옵시디언 신청하기](https://class.cmdspace.kr/channels/L2NoYW5uZWxzLzE3Njkx/C00007/classes/153252/information)

"당신의 지식 시스템은 당신이 기억을 잃어도 당신을 재건할 수 있는가?
당신의 AI에게는 어떤 설계도가 주어져 있는가?"— 월간 옵시디언 20회차 클로징

© 2026 CMDSPACE · 구요한 — [cmdspace.work](https://cmdspace.work)

월간 옵시디언 20회차 후속 자료 · 2026-08-26
