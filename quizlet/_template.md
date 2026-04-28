# Quizlet 세트 마스터 템플릿

> **목적**: 모든 Quizlet 세트의 구조 정의. 자동화 파이프라인(8B LLM)이 이 템플릿을 읽고 새 세트를 생성한다.
> **최종 업데이트**: 2026-04-27

---

## 템플릿 사용법

### 1. 새 세트 만들기
- 이 파일의 구조를 복사
- `set_info`와 `cards` 섹션 채우기
- 대응하는 `import/{set_name}.tsv` 파일은 cards에서 자동 생성 가능

### 2. Quizlet에 가져오기
- 대응하는 `import/{set_name}.tsv` 파일을 연다
- 파일 내용을 전체 복사
- Quizlet "만들기" > "가져오기"에 붙여넣기
- 설정: 용어와 정의 구분 = `탭(Tab)` / 카드 구분 = `줄바꿈`

### 3. 자동화 파이프라인
- LLM은 `cards` YAML을 파싱하여 새 카드 생성
- `front`/`back` 필드는 카드 `type`에 따라 규칙적으로 생성
- 생성 후 `import/{set_name}.tsv` 순수 붙여넣기 파일도 함께 출력
- 질문 응답 훈련이 필요한 세트는 `qna_cards`에서 `import/qna/{set_name}_qna.tsv`도 함께 출력

---

## 카드 유형별 Front/Back 규칙

### 🟢 vocab (단어)
```text
Front: {korean} ({pronunciation})
Back:  {english}. Example: {korean_example} = {english_example}.
```

### 🔵 grammar (문법 패턴)
```text
Front: {korean} ({pronunciation})
Back:  {simple_use}. Example: {korean_example} = {english_example}.
```

### 🟢 expression (표현 — Q&A-First)
```text
Front: {korean} ({pronunciation})
Back:  {english}. Situation: {context_english}.
```

### 🟡 reaction (리액션)
```text
Front: {korean} ({pronunciation})
Back:  {english}. Use when: {context_english}.
```

### 🧩 qa_drill (질문/답변 훈련)
```text
Front: [Q] {korean_question} ({question_sound}) / [A] {korean_answer} ({answer_sound})
Back:  [Q] {english_question} / [A] {english_answer}
```

---

## YAML 구조

```yaml
# === QUIZLET SET METADATA ===
set_info:
  name: ""                    # 세트 이름 (한/영)
  category: ""                # foundation | weekly | practical
  week: null                  # 주차 번호 (weekly만 해당, 없으면 null)
  level: beginner             # beginner | intermediate
  description: ""             # 세트 설명
  card_count: 0               # 총 카드 수
  created: ""                 # 생성일 (YYYY-MM-DD)
  updated: ""                 # 수정일 (YYYY-MM-DD)
  tags: []                    # 태그 (검색용)

cards:
  - id: ""                    # 고유 ID — 규칙: {category첫글자}{week}-{번호}
                              #   예: w1-01 (weekly week1 첫번째)
                              #       f1-01 (foundation 조사 첫번째)
                              #       p1-01 (practical 리액션 첫번째)
    type: ""                  # vocab | grammar | expression | reaction
    color: ""                 # 🔵 | 🟢 | 🟡
    korean: ""                # 한국어 텍스트
    pronunciation: ""         # 로마자 발음 (dash-separated syllables)
    english: ""               # 영어 번역
    context: ""               # 사용 상황 (영어, 짧게)
    note: ""                  # 교사용 메모 (선택, Quizlet 뒷면에 길게 넣지 않음)
    simple_use: ""            # grammar 전용: 학생용 짧은 사용 설명
    korean_example: ""        # Quizlet 뒷면 예문
    english_example: ""       # Quizlet 뒷면 예문 번역

qna_cards:
  - id: ""                    # 예: w3-q01, f2-q04
    type: "qa_drill"
    korean_question: ""       # 학생이 듣거나 받을 한국어 질문
    question_sound: ""        # 질문 발음
    korean_answer: ""         # 학생이 말할 한국어 답변
    answer_sound: ""          # 답변 발음
    english_question: ""      # 질문 영어 뜻
    english_answer: ""        # 답변 영어 뜻
    source: ""                # role play, micro-drill, review 등
# === END METADATA ===
```

---

## ID 규칙

| Category | Prefix | 예시 |
|----------|--------|------|
| Foundation 조사 | f1- | f1-01, f1-02 |
| Foundation 동사 | f2- | f2-01, f2-02 |
| Foundation 형용사 | f3- | f3-01, f3-02 |
| Foundation 숫자 | f4- | f4-01, f4-02 |
| Weekly Week 1 | w1- | w1-01, w1-02 |
| Weekly Week 2 | w2- | w2-01, w2-02 |
| Weekly Week 3 | w3- | w3-01, w3-02 |
| Weekly Week 4 | w4- | w4-01, w4-02 |
| Practical 리액션 | p1- | p1-01, p1-02 |
| Practical 패턴 | p2- | p2-01, p2-02 |
| Practical 기초 | p3- | p3-01, p3-02 |
| Q/A Drill companion | {prefix}-q | w3-q01, p1-q06 |

---

## Quizlet Import 형식

```text
{front}<TAB>{back}
{front}<TAB>{back}
...
```

> ⚠️ `{front}`과 `{back}` 사이는 반드시 **TAB 문자**로 구분.
> 줄바꿈 = 카드 구분.
> 실제 학생 전달용 파일은 `import/{set_name}.tsv`에 저장한다.
> Q/A Drill 파일은 `import/qna/{set_name}_qna.tsv`에 저장한다.
