# 📚 Quizlet 낱말 카드 세트

> **Korean Mentoring — Flashcard System**
> 자동화 파이프라인 호환 · Q&A-First 교수법 반영

---

## Quick Start (Quizlet 가져오기)

1. 아래 세트 파일 중 하나를 연다
2. `## Quizlet Import` 섹션의 내용을 **전체 복사**
3. [Quizlet](https://quizlet.com) → "만들기" → "가져오기" → 붙여넣기
4. 설정: 용어-정의 구분 = **Tab** / 카드 구분 = **줄바꿈**

---

## 파일 인덱스

### 📐 Template

| 파일 | 설명 |
|------|------|
| [`_template.md`](./_template.md) | 마스터 템플릿 — 모든 세트의 YAML 구조, 카드 유형별 Front/Back 규칙, ID 체계 정의. LLM 자동 생성 시 이 파일을 참조. |

### 🧱 Foundation (기초 — 모든 학생 공통)

| 파일 | 카드 수 | 내용 |
|------|--------|------|
| [`foundation_particles.md`](./foundation_particles.md) | 14장 | 필수 조사: 은/는, 이/가, 을/를, 에, 에서, (으)로, 도, 와/과, 하고, 의, 까지, 부터, 만 |
| [`foundation_verbs.md`](./foundation_verbs.md) | 20장 | 필수 동사: 가다, 오다, 하다, 먹다, 마시다, 보다, 알다, 모르다 등 — Week 1~4에서 실제 사용 |
| [`foundation_adjectives.md`](./foundation_adjectives.md) | 15장 | 필수 형용사: 좋다, 예쁘다, 맛있다, 비싸다, 괜찮다, 부끄럽다 등 |
| [`foundation_numbers.md`](./foundation_numbers.md) | 15장 | 고유숫자(하나~다섯), 한자숫자(일~십), 단위(개/잔/명/원/번), 변형(한/두/세/네) |

**소계: 64장**

### 📅 Weekly (주차별 복습)

| 파일 | 카드 수 | 주제 | 연결 수업 |
|------|--------|------|----------|
| [`week1_review.md`](./week1_review.md) | 18장 | 🚕 택시 생존: 목적지, 하차, 방어 문장, 리액션 | [`../lessons/week1_taxi_moving_v2.md`](../lessons/week1_taxi_moving_v2.md) |
| [`week2_review.md`](./week2_review.md) | 20장 | 💞 팬 소통: 리액션, 겸손 응답, 사진 찍기 | [`../lessons/week2_fan_interaction_v2.md`](../lessons/week2_fan_interaction_v2.md) |
| [`week3_review.md`](./week3_review.md) | 20장 | ☕ 카페/쇼핑: 주문, 알바생 3대 질문, 가격 | [`../lessons/week3_cafe_shopping_v2.md`](../lessons/week3_cafe_shopping_v2.md) |
| [`week4_review.md`](./week4_review.md) | 22장 | 📱 콘텐츠: 오프닝/클로징, 인터넷 슬랭, 팬덤 | [`../lessons/week4_vlog_streaming_v2.md`](../lessons/week4_vlog_streaming_v2.md) |

**소계: 80장**

### 🛠️ Practical (실용회화 필수)

| 파일 | 카드 수 | 내용 |
|------|--------|------|
| [`practical_reactions.md`](./practical_reactions.md) | 12장 | 만능 리액션: 아 네~, 괜찮아요~, 진짜요?, 대박!, 잘 모르겠어요~ 등 |
| [`practical_patterns.md`](./practical_patterns.md) | 15장 | 필수 문법 패턴: -주세요, -(으)로, -요, -아요/어요, -(이)요, -야/이야 등 |
| [`practical_basics.md`](./practical_basics.md) | 15장 | 의문사(뭐/어디/언제/왜), 시간(오늘/내일), 장소(여기/거기), 지시사(이거/그거) |

**소계: 42장**

### **총계: 186장 / 11세트**

---

## 카드 유형

| 타입 | 색상 | Front (앞면) | Back (뒷면) | 용도 |
|------|------|-------------|------------|------|
| `vocab` | 🟢 | 한국어 | English \| pronunciation | 단어 암기 |
| `grammar` | 🔵 | 한국어 패턴 | Pattern rule + example \| pronunciation | 문법 이해 |
| `expression` | 🟢 | `[Situation]` 상황 설명 (EN) | 한국어 답변 \| pronunciation | Q&A-First 훈련 |
| `reaction` | 🟡 | `[When]` 상황 (EN) | 한국어 \| pronunciation \| English | 리액션 훈련 |

> **Q&A-First**: 표현/리액션 카드는 "상황을 보고 한국어를 떠올리는" 방식으로 교수법과 일치.

---

## ID 체계

```
{category}{number}-{sequence}
```

| Prefix | Category | 예시 |
|--------|----------|------|
| `f1-` ~ `f4-` | Foundation (조사/동사/형용사/숫자) | `f1-01`, `f2-15` |
| `w1-` ~ `w4-` | Weekly (Week 1~4) | `w1-09`, `w3-14` |
| `p1-` ~ `p3-` | Practical (리액션/패턴/기초) | `p1-06`, `p2-03` |

---

## 듀얼 포맷 구조

모든 세트 파일에는 두 가지 형식이 포함됨:

```
┌────────────────────────────────────────┐
│  ## 메타데이터 (YAML)                    │
│  → 자동화 파이프라인 / LLM 파싱용         │
│  → 카드별 id, type, color, korean,      │
│    pronunciation, english, context      │
├────────────────────────────────────────┤
│  ## Quizlet Import (TSV)               │
│  → 복사 → Quizlet에 바로 붙여넣기        │
│  → {front} TAB {back}                  │
└────────────────────────────────────────┘
```

---

## 자동화 파이프라인 (LLM 참조)

새 세트를 자동 생성할 때:

1. `_template.md`의 YAML 구조와 Front/Back 규칙을 읽는다
2. 해당 Week의 v2 커리큘럼 파일 (`../lessons/week{N}_*_v2.md`)에서 치트시트와 표현을 추출한다
3. 카드 유형(vocab/grammar/expression/reaction)에 따라 front/back을 생성한다
4. YAML 메타데이터 + Quizlet Import TSV를 함께 출력한다

**참조 파일**:
- 교수법: `../methodology/teaching_methodology.md` (4대 원칙, Q&A-First Method, 배포 시스템)
- 커리큘럼: `../lessons/week{1-4}_*_v2.md` (주차별 수업 매뉴얼)
- 브랜드: `../strategy/italki_brand_guideline.md` (색상 체계, 시그니처 요소)
