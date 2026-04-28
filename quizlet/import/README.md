# Quizlet Import Files

이 폴더의 `.tsv` 파일은 Quizlet 가져오기 창에 바로 붙여넣는 순수 텍스트입니다.
각 줄은 `앞면 + 탭 + 뒷면` 구조입니다.
Reference 파일의 앞면은 `한국어 (발음)`, 뒷면은 `뜻 + 예문/사용 상황` 형식입니다.
Q/A Drill 파일의 앞면은 `[Q] 질문 / [A] 답변`, 뒷면은 영어 질문/답변 형식입니다.

Reference 카드는 학생 혼자 빠르게 복습하는 용도입니다. Q/A Drill 카드는 질문을 듣고 바로 답하는 실전 조합 훈련용입니다.

## 사용법

1. 필요한 `.tsv` 파일을 연다.
2. 파일 전체를 복사한다.
3. Quizlet "만들기" > "가져오기"에 붙여넣기.
4. 설정을 아래처럼 둔다.

```text
단어 / 뜻 구분자: 탭
카드 구분: 다음 줄
```

## Reference Import 파일

| 파일 | 카드 수 | 내용 |
|------|--------|------|
| [`foundation_particles.tsv`](./foundation_particles.tsv) | 14장 | 필수 조사 |
| [`foundation_verbs.tsv`](./foundation_verbs.tsv) | 20장 | 필수 동사 |
| [`foundation_adjectives.tsv`](./foundation_adjectives.tsv) | 15장 | 필수 형용사 |
| [`foundation_numbers.tsv`](./foundation_numbers.tsv) | 15장 | 숫자와 단위 |
| [`week1_review.tsv`](./week1_review.tsv) | 18장 | Week 1 택시 생존 복습 |
| [`week2_review.tsv`](./week2_review.tsv) | 20장 | Week 2 팬 소통 복습 |
| [`week3_review.tsv`](./week3_review.tsv) | 20장 | Week 3 카페/쇼핑 복습 |
| [`week4_review.tsv`](./week4_review.tsv) | 22장 | Week 4 콘텐츠 크리에이터 복습 |
| [`practical_reactions.tsv`](./practical_reactions.tsv) | 12장 | 만능 리액션 |
| [`practical_patterns.tsv`](./practical_patterns.tsv) | 15장 | 필수 문법 패턴 |
| [`practical_basics.tsv`](./practical_basics.tsv) | 15장 | 의문사, 시간, 장소 |

**Reference 총계: 186장**

## Q/A Drill Import 파일

| 파일 | 카드 수 | 내용 |
|------|--------|------|
| [`qna/foundation_particles_qna.tsv`](./qna/foundation_particles_qna.tsv) | 14장 | 조사 Q/A micro-drill |
| [`qna/foundation_verbs_qna.tsv`](./qna/foundation_verbs_qna.tsv) | 20장 | 동사 Q/A micro-drill |
| [`qna/foundation_adjectives_qna.tsv`](./qna/foundation_adjectives_qna.tsv) | 15장 | 형용사 Q/A micro-drill |
| [`qna/foundation_numbers_qna.tsv`](./qna/foundation_numbers_qna.tsv) | 15장 | 숫자/단위 Q/A micro-drill |
| [`qna/week1_review_qna.tsv`](./qna/week1_review_qna.tsv) | 18장 | Week 1 택시 질문 응답 |
| [`qna/week2_review_qna.tsv`](./qna/week2_review_qna.tsv) | 20장 | Week 2 팬 소통 질문 응답 |
| [`qna/week3_review_qna.tsv`](./qna/week3_review_qna.tsv) | 20장 | Week 3 카페/쇼핑 질문 응답 |
| [`qna/week4_review_qna.tsv`](./qna/week4_review_qna.tsv) | 22장 | Week 4 콘텐츠/통합 질문 응답 |
| [`qna/practical_reactions_qna.tsv`](./qna/practical_reactions_qna.tsv) | 12장 | 만능 리액션 질문 응답 |
| [`qna/practical_patterns_qna.tsv`](./qna/practical_patterns_qna.tsv) | 15장 | 패턴 Q/A micro-drill |
| [`qna/practical_basics_qna.tsv`](./qna/practical_basics_qna.tsv) | 15장 | 의문사/시간/장소 Q/A |

**Q/A Drill 총계: 186장**
