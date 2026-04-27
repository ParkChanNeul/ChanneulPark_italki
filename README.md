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

## 📁 파일 인덱스

### 핵심 문서 (Core)

| 파일 | 역할 | 설명 |
|------|------|------|
| [`teaching_methodology.md`](./teaching_methodology.md) | 📖 교수법 마스터 가이드 | 4대 원칙, 6개 섹션, Q&A-First Method, 배포 시스템 3중 구조. **모든 수업 설계의 근간.** |
| [`italki_brand_guideline.md`](./italki_brand_guideline.md) | 🎯 브랜드 DNA | 정체성, 포지셔닝, 차별화, 시그니처 요소, 경쟁 분석 |
| [`italki_strategy.md`](./italki_strategy.md) | 📊 전략 로드맵 | Think→Plan→Build 통합. 시장, 가격, KPI(월 500만원), 콘텐츠/자동화 비전 |

### 수업 매뉴얼 (Week v2)

| 파일 | 주제 | 핵심 표현 |
|------|------|----------|
| [`week1_taxi_moving_v2.md`](./week1_taxi_moving_v2.md) | 🚕 택시 생존 | 기사님, OO(으)로 가주세요 / 세워주세요 / 잘 모르겠어요~ |
| [`week2_fan_interaction_v2.md`](./week2_fan_interaction_v2.md) | 💞 팬 소통 | 헐! 대박! / 아니에요~ 부끄러워요 / 같이 찍어요! |
| [`week3_cafe_shopping_v2.md`](./week3_cafe_shopping_v2.md) | ☕ 카페/쇼핑 | 아아 하나 포장이요 / 괜찮아요~ / 이거 얼마예요? |
| [`week4_vlog_streaming_v2.md`](./week4_vlog_streaming_v2.md) | 📱 콘텐츠 크리에이터 | 안녕 예쁜이들~ / 좋아요 구독 눌러줘~ / 인터넷 슬랭 |

> 모든 v2 파일은 4대 교수법 원칙(SHOW IT/WAIT/BRIDGE/SPLIT)이 수업 흐름에 직접 삽입되어 있다.
> 색상 체계: 🔵 문법 / 🟢 어휘 / 🟡 문화 포인트

### 학생 관리

| 파일 | 설명 |
|------|------|
| [`student01_curriculum.md`](./student01_curriculum.md) | Student #01 맞춤 커리큘럼 (한국어) |
| [`student01_curriculum_en.md`](./student01_curriculum_en.md) | Student #01 맞춤 커리큘럼 (영어) |
| [`student01_lesson_manual.md`](./student01_lesson_manual.md) | Student #01 수업 운영 매뉴얼 (영어) |
| [`student01_lesson_manual_ko.md`](./student01_lesson_manual_ko.md) | Student #01 수업 운영 매뉴얼 (한국어) |

### Quizlet 낱말 카드

| 디렉토리 | 내용 |
|----------|------|
| [`quizlet/`](./quizlet/) | 11세트 / 186장. Foundation(64) + Weekly(80) + Practical(42). 자세한 인덱스는 [`quizlet/README.md`](./quizlet/README.md) 참조. |

### 참고 자료

| 파일 | 설명 |
|------|------|
| [`italki_classes.md`](./italki_classes.md) | italki 수업 유형 및 클래스 설정 |
| [`italki_first_interview_guide.md`](./italki_first_interview_guide.md) | 첫 수업(인터뷰) 진행 가이드 |
| [`italki_janchy_think_plan.md`](./italki_janchy_think_plan.md) | 초기 기획 문서 (Think/Plan) |

---

## 🤖 AI Agent 참조 가이드

### 수업 자료를 수정할 때
1. **먼저 읽을 것**: `teaching_methodology.md` (교수법 원칙 + 배포 시스템)
2. **원칙 확인**: 4대 원칙(SHOW IT/WAIT/BRIDGE/SPLIT)이 수업 흐름에 반영되었는지
3. **표기 규칙**: OO(으)로 (범용), 🔵문법/🟢어휘/🟡문화

### Quizlet 세트를 생성할 때
1. **먼저 읽을 것**: `quizlet/_template.md` (YAML 구조 + Front/Back 규칙)
2. **소스**: 해당 `week{N}_*_v2.md`의 치트시트에서 카드 데이터 추출
3. **출력**: YAML 메타데이터 + Quizlet Import TSV 둘 다 생성

### 브랜드/전략 문서를 수정할 때
1. **정합성 체크**: `teaching_methodology.md` ↔ `italki_brand_guideline.md` ↔ `italki_strategy.md` 3개 문서 동기화 필수
2. **핵심 키워드**: Q&A-First Method, Combination Practice, Classroom+Quizlet+Docs

### 새 학생 커리큘럼을 만들 때
1. `student01_curriculum.md`를 참고 템플릿으로 사용
2. Week v2 파일에서 시나리오를 학생 배경에 맞게 커스텀
3. Quizlet 세트는 `_template.md` 규칙에 따라 자동 생성

---

## Version History

| 날짜 | 변경 |
|------|------|
| 2026-04-27 | Quizlet 11세트(186장) 생성, 배포 시스템 3중 구조 정립, Q&A-First Method 공식화, 전략/브랜드 동기화 |
| 2026-04-19 | Office Hours Review 반영, 4대 교수법 원칙 수립, Week 1~4 v2 커리큘럼 재설계 |
| 2026-04-12 | 초기 프로젝트 생성, Student #01 커리큘럼, 브랜드/전략 초안 |
