# 🇰🇷 ChanneulPark_italki

> **Korean Culture Mentor System**
> 박찬늘 — italki 한국어 멘토링 프로젝트

---

## What This Is

외국인이 한국을 이해하고 연결되게 만드는 멘토링 시스템.
교수법, 커리큘럼, 브랜드, 전략, 학생 자료를 하나의 구조로 관리한다.

### Core Identity

> **I don't teach Korean. I help you understand Koreans.**

### 교수법 핵심

- **4대 원칙**: SHOW IT · WAIT · BRIDGE · SPLIT
- **Q&A-First Method**: 질문을 먼저 → 답변 → 응용 → 문화 해석 → 자발적 조합
- **배포 시스템**: Google Classroom(허브) + Quizlet(훈련) + Google Docs(기록)

---

## 📁 디렉토리 구조

| 디렉토리 | 역할 | 언제 보는가 |
|----------|------|-------------|
| [`strategy/`](./strategy/) | 사업 전략, 브랜드, 클래스 라인업 | 포지셔닝, 가격, 런치 방향을 바꿀 때 |
| [`methodology/`](./methodology/) | 교수법, 고객 발견 인터뷰 | 수업 방식이나 피드백 반영 원칙을 바꿀 때 |
| [`lessons/`](./lessons/) | Week 1-4 수업안 | 실제 수업 준비, 수업 후 개선할 때 |
| [`students/`](./students/) | 학생별 맞춤 커리큘럼/매뉴얼 | 특정 학생 자료를 만들거나 수정할 때 |
| [`quizlet/`](./quizlet/) | 낱말 카드 세트 | 예습/복습 카드 생성, Quizlet 업로드할 때 |
| [`assets/`](./assets/) | PDF, 슬라이드 등 산출물 | 학생에게 보여주는 시각 자료를 관리할 때 |
| [`archive/`](./archive/) | 대화 로그, 과거 작업 기록 | 맥락 복원이나 의사결정 히스토리가 필요할 때 |

---

## 📁 파일 인덱스

### 핵심 문서 (Core)

| 파일 | 역할 | 설명 |
|------|------|------|
| [`methodology/teaching_methodology.md`](./methodology/teaching_methodology.md) | 📖 교수법 마스터 가이드 | 4대 원칙, 6개 섹션, Q&A-First Method, 배포 시스템 3중 구조. **모든 수업 설계의 근간.** |
| [`strategy/italki_brand_guideline.md`](./strategy/italki_brand_guideline.md) | 🎯 브랜드 DNA | 정체성, 포지셔닝, 차별화, 시그니처 요소, 경쟁 분석 |
| [`strategy/italki_strategy.md`](./strategy/italki_strategy.md) | 📊 전략 로드맵 | Think→Plan→Build 통합. 시장, 가격, KPI(월 500만원), 콘텐츠/자동화 비전 |
| [`strategy/italki_janchy_think_plan.md`](./strategy/italki_janchy_think_plan.md) | 🧠 초기 Think/Plan | 초기 문제 정의, 시장 판단, 확장 방향, Office Hours 반영 기록 |
| [`strategy/italki_classes.md`](./strategy/italki_classes.md) | 🧾 클래스 라인업 | Trial, Making Friends, 확장 클래스 설정과 가격 로드맵 |

### 수업 매뉴얼 (Week v2)

| 파일 | 주제 | 핵심 표현 |
|------|------|----------|
| [`lessons/week1_taxi_moving_v2.md`](./lessons/week1_taxi_moving_v2.md) | 🚕 택시 생존 | 기사님, OO(으)로 가주세요 / 세워주세요 / 잘 모르겠어요~ |
| [`lessons/week2_fan_interaction_v2.md`](./lessons/week2_fan_interaction_v2.md) | 💞 팬 소통 | 헐! 대박! / 아니에요~ 부끄러워요 / 같이 찍어요! |
| [`lessons/week3_cafe_shopping_v2.md`](./lessons/week3_cafe_shopping_v2.md) | ☕ 카페/쇼핑 | 아아 하나 포장이요 / 괜찮아요~ / 이거 얼마예요? |
| [`lessons/week4_vlog_streaming_v2.md`](./lessons/week4_vlog_streaming_v2.md) | 📱 콘텐츠 크리에이터 | 안녕 예쁜이들~ / 좋아요 구독 눌러줘~ / 인터넷 슬랭 |

> 모든 v2 파일은 4대 교수법 원칙(SHOW IT/WAIT/BRIDGE/SPLIT)이 수업 흐름에 직접 삽입되어 있다.
> 색상 체계: 🔵 문법 / 🟢 어휘 / 🟡 문화 포인트

### 학생 관리

| 파일 | 설명 |
|------|------|
| [`students/student01/curriculum.md`](./students/student01/curriculum.md) | Student #01 맞춤 커리큘럼 (한국어) |
| [`students/student01/curriculum_en.md`](./students/student01/curriculum_en.md) | Student #01 맞춤 커리큘럼 (영어) |
| [`students/student01/lesson_manual.md`](./students/student01/lesson_manual.md) | Student #01 수업 운영 매뉴얼 (영어) |
| [`students/student01/lesson_manual_ko.md`](./students/student01/lesson_manual_ko.md) | Student #01 수업 운영 매뉴얼 (한국어) |

### Quizlet 낱말 카드

| 디렉토리 | 내용 |
|----------|------|
| [`quizlet/`](./quizlet/) | 11세트 / 186장. Foundation(64) + Weekly(80) + Practical(42). 자세한 인덱스는 [`quizlet/README.md`](./quizlet/README.md) 참조. |

### 참고 자료

| 파일 | 설명 |
|------|------|
| [`methodology/italki_first_interview_guide.md`](./methodology/italki_first_interview_guide.md) | 첫 수업(인터뷰) 진행 가이드 |
| [`assets/slides/week1_taxi_moving.pdf`](./assets/slides/week1_taxi_moving.pdf) | Week 1 택시 수업 PDF 슬라이드 |
| [`archive/conversations/2026-04-27-optimizing-korean-lesson-design.md`](./archive/conversations/2026-04-27-optimizing-korean-lesson-design.md) | Gemini와 진행한 긴 개선 대화 로그 |

---

## 🤖 AI Agent 참조 가이드

### 수업 자료를 수정할 때
1. **먼저 읽을 것**: `methodology/teaching_methodology.md` (교수법 원칙 + 배포 시스템)
2. **원칙 확인**: 4대 원칙(SHOW IT/WAIT/BRIDGE/SPLIT)이 수업 흐름에 반영되었는지
3. **표기 규칙**: OO(으)로 (범용), 🔵문법/🟢어휘/🟡문화

### Quizlet 세트를 생성할 때
1. **먼저 읽을 것**: `quizlet/_template.md` (YAML 구조 + Front/Back 규칙)
2. **소스**: 해당 `lessons/week{N}_*_v2.md`의 치트시트에서 카드 데이터 추출
3. **출력**: YAML 메타데이터 + Quizlet Import TSV 둘 다 생성

### 브랜드/전략 문서를 수정할 때
1. **정합성 체크**: `methodology/teaching_methodology.md` ↔ `strategy/italki_brand_guideline.md` ↔ `strategy/italki_strategy.md` 3개 문서 동기화 필수
2. **핵심 키워드**: Q&A-First Method, Combination Practice, Classroom+Quizlet+Docs

### 새 학생 커리큘럼을 만들 때
1. `students/student01/curriculum.md`를 참고 템플릿으로 사용
2. `lessons/`의 Week v2 파일에서 시나리오를 학생 배경에 맞게 커스텀
3. Quizlet 세트는 `_template.md` 규칙에 따라 자동 생성

---

## Version History

| 날짜 | 변경 |
|------|------|
| 2026-04-27 | Quizlet 11세트(186장) 생성, 배포 시스템 3중 구조 정립, Q&A-First Method 공식화, 전략/브랜드 동기화 |
| 2026-04-19 | Office Hours Review 반영, 4대 교수법 원칙 수립, Week 1~4 v2 커리큘럼 재설계 |
| 2026-04-12 | 초기 프로젝트 생성, Student #01 커리큘럼, 브랜드/전략 초안 |
