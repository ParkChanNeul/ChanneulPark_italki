# 📚 Quizlet 낱말 카드 세트

> **Korean Mentoring — Flashcard System**
> 자동화 파이프라인 호환 · Q&A-First 교수법 반영

---

## Quick Start (Quizlet 가져오기)

1. `import/` 폴더의 `.tsv` 파일을 연다
2. 파일 내용을 **전체 복사**
3. [Quizlet](https://quizlet.com) "만들기" > "가져오기"에 붙여넣기
4. 설정: 용어-정의 구분 = **Tab** / 카드 구분 = **줄바꿈**

> `.md` 파일은 수업/관리용 문서입니다. Quizlet에는 [`import/`](./import/)의 순수 `.tsv` 파일을 붙여넣으세요.
> Reference 카드는 짧은 복습용이고, Q/A Drill 카드는 질문을 듣고 바로 답하는 조합 훈련용입니다.

### Reference Import 파일

| 파일 | 카드 수 | 내용 |
|------|--------|------|
| [`import/foundation_particles.tsv`](./import/foundation_particles.tsv) | 14장 | 필수 조사 |
| [`import/foundation_verbs.tsv`](./import/foundation_verbs.tsv) | 20장 | 필수 동사 |
| [`import/foundation_adjectives.tsv`](./import/foundation_adjectives.tsv) | 15장 | 필수 형용사 |
| [`import/foundation_numbers.tsv`](./import/foundation_numbers.tsv) | 15장 | 숫자와 단위 |
| [`import/week1_review.tsv`](./import/week1_review.tsv) | 18장 | Week 1 택시 생존 복습 |
| [`import/week2_review.tsv`](./import/week2_review.tsv) | 20장 | Week 2 팬 소통 복습 |
| [`import/week3_review.tsv`](./import/week3_review.tsv) | 20장 | Week 3 카페/쇼핑 복습 |
| [`import/week4_review.tsv`](./import/week4_review.tsv) | 22장 | Week 4 콘텐츠 크리에이터 복습 |
| [`import/practical_reactions.tsv`](./import/practical_reactions.tsv) | 12장 | 만능 리액션 |
| [`import/practical_patterns.tsv`](./import/practical_patterns.tsv) | 15장 | 필수 문법 패턴 |
| [`import/practical_basics.tsv`](./import/practical_basics.tsv) | 15장 | 의문사, 시간, 장소 |

**Reference 총계: 186장**

### Q/A Drill Import 파일

| 파일 | 카드 수 | 내용 |
|------|--------|------|
| [`import/qna/foundation_particles_qna.tsv`](./import/qna/foundation_particles_qna.tsv) | 14장 | 조사 Q/A micro-drill |
| [`import/qna/foundation_verbs_qna.tsv`](./import/qna/foundation_verbs_qna.tsv) | 20장 | 동사 Q/A micro-drill |
| [`import/qna/foundation_adjectives_qna.tsv`](./import/qna/foundation_adjectives_qna.tsv) | 15장 | 형용사 Q/A micro-drill |
| [`import/qna/foundation_numbers_qna.tsv`](./import/qna/foundation_numbers_qna.tsv) | 15장 | 숫자/단위 Q/A micro-drill |
| [`import/qna/week1_review_qna.tsv`](./import/qna/week1_review_qna.tsv) | 18장 | Week 1 택시 질문 응답 |
| [`import/qna/week2_review_qna.tsv`](./import/qna/week2_review_qna.tsv) | 20장 | Week 2 팬 소통 질문 응답 |
| [`import/qna/week3_review_qna.tsv`](./import/qna/week3_review_qna.tsv) | 20장 | Week 3 카페/쇼핑 질문 응답 |
| [`import/qna/week4_review_qna.tsv`](./import/qna/week4_review_qna.tsv) | 22장 | Week 4 콘텐츠/통합 질문 응답 |
| [`import/qna/practical_reactions_qna.tsv`](./import/qna/practical_reactions_qna.tsv) | 12장 | 만능 리액션 질문 응답 |
| [`import/qna/practical_patterns_qna.tsv`](./import/qna/practical_patterns_qna.tsv) | 15장 | 패턴 Q/A micro-drill |
| [`import/qna/practical_basics_qna.tsv`](./import/qna/practical_basics_qna.tsv) | 15장 | 의문사/시간/장소 Q/A |

**Q/A Drill 총계: 186장**

---

## 파일 인덱스

### 📐 Template

| 파일 | 설명 |
|------|------|
| [`_template.md`](./_template.md) | 마스터 템플릿 — 모든 세트의 YAML 구조, 카드 유형별 Front/Back 규칙, ID 체계 정의. LLM 자동 생성 시 이 파일을 참조. |
| [`qna/README.md`](./qna/README.md) | Q/A Drill 관리 인덱스 — 질문/답변 훈련용 companion set 관리. |

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

### 🧩 Q/A Drill (질문/답변 훈련)

| 위치 | 카드 수 | 내용 |
|------|--------|------|
| [`qna/`](./qna/) | 186장 / 11세트 | 질문을 듣고 바로 답하는 실전 조합 훈련 companion set |

### **총계: Reference 186장 / Q/A Drill 186장 / 22세트**

---

## 카드 유형

| 타입 | 색상 | Front (앞면) | Back (뒷면) | 용도 |
|------|------|-------------|------------|------|
| `vocab` | 🟢 | 한국어 + 발음 | Meaning + example | 단어 암기 |
| `grammar` | 🔵 | 한국어 패턴 + 발음 | Use + example | 짧은 패턴 복습 |
| `expression` | 🟢 | 한국어 표현 + 발음 | Meaning + situation | 실전 표현 복습 |
| `reaction` | 🟡 | 한국어 리액션 + 발음 | Meaning + use case | 리액션 훈련 |
| `qa_drill` | 🧩 | `[Q] 한국어 질문 / [A] 한국어 답변` | `[Q] English / [A] English` | 질문 응답 조합 훈련 |

> 수업에서는 Q&A-First로 상황을 먼저 다루고, Quizlet에서는 Reference로 표현을 확인한 뒤 Q/A Drill로 질문 응답을 반복한다.

---

## ID 체계

```text
{category}{number}-{sequence}
```

| Prefix | Category | 예시 |
|--------|----------|------|
| `f1-` ~ `f4-` | Foundation (조사/동사/형용사/숫자) | `f1-01`, `f2-15` |
| `w1-` ~ `w4-` | Weekly (Week 1~4) | `w1-09`, `w3-14` |
| `p1-` ~ `p3-` | Practical (리액션/패턴/기초) | `p1-06`, `p2-03` |
| `{prefix}-q` | Q/A Drill companion | `w3-q01`, `p1-q06` |

---

## 듀얼 포맷 구조

모든 세트는 두 가지 파일로 관리됨:

```text
┌────────────────────────────────────────┐
│  ## 메타데이터 (YAML)                    │
│  자동화 파이프라인 / LLM 파싱용           │
│  카드별 id, type, color, korean,        │
│    pronunciation, english, context      │
├────────────────────────────────────────┤
│  import/*.tsv                          │
│  Reference 학생 전달/Quizlet 붙여넣기용  │
│  {front} TAB {back}                    │
├────────────────────────────────────────┤
│  import/qna/*.tsv                      │
│  Q/A Drill 학생 전달/Quizlet 붙여넣기용  │
│  [Q] 질문 / [A] 답변 TAB English Q/A    │
└────────────────────────────────────────┘
```

---

## 자동화 파이프라인 (LLM 참조)

새 세트를 자동 생성할 때:

1. `_template.md`의 YAML 구조와 Front/Back 규칙을 읽는다
2. 해당 Week의 v2 커리큘럼 파일 (`../lessons/week{N}_*_v2.md`)에서 치트시트와 표현을 추출한다
3. 카드 유형(vocab/grammar/expression/reaction)에 따라 front/back을 생성한다
4. Q/A가 필요한 세트는 `qa_drill` 카드도 생성한다
5. YAML 메타데이터 + `import/{set_name}.tsv` + `import/qna/{set_name}_qna.tsv`를 함께 출력한다

**참조 파일**:
- 교수법: `../methodology/teaching_methodology.md` (4대 원칙, Q&A-First Method, 배포 시스템)
- Google Docs 템플릿: `../templates/google_docs_lesson_note.md` (자세한 문법/문화 설명)
- 커리큘럼: `../lessons/week{1-4}_*_v2.md` (주차별 수업 매뉴얼)
- 브랜드: `../strategy/italki_brand_guideline.md` (색상 체계, 시그니처 요소)
