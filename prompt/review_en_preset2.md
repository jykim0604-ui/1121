# 영문본·프리셋 2 재검수 — 결정 목록

대상: `system_prompt_v1_en_paste.txt`(= `system_prompt_v1_en.md`), `test_paste.md` ③ 프리셋 2. 한국어 원본 `system_prompt_v1.md`와 참조본 `preset_b4.md`는 반영 시 함께 동기화한다.

이 파일은 목록 정리만 한다. 아래 수정은 아직 어느 파일에도 반영하지 않았다.

## 상태 요약

| 항목 | 내용 | 결정 |
|---|---|---|
| A1 | 성인 장면 발성·소리: 문체 경계에만 예외, 표현 레지스터 경계·프리셋 1과 충돌 | 최우선 보류 (프리셋 1 작업) |
| A2 | 4-2 "보이거나 셀 수 있는 값"이 감각값을 막음 | 반영 |
| A3 | 3-1 "이미 써 온 호칭 이어 쓰기"가 과거 오류를 고정할 수 있음 | 현행 유지 (피드백 아래) |
| A4 | 3-2 "처음부터 높지 않고"에 입력 예외가 없음 | 반영 |
| B1 | 3-2 "의성어" 범위 | 방향 재검토 (사용자 의도: 대사의 과장 신음 차단) |
| B2 | 프리셋 2 수식어 앵커가 대사까지 덮음 | 설명 후 결정 |
| B3 | 2-1 {{user}} 관계 문장이 "관계"만 덮음 | 반영 |
| B4 | 2-1 다른 인물의 공개 활동 인지 | 반영 |
| B5 | 설정 괄호에 캐릭터 설명 추가 | 미반영 (캐릭터 설명 칸 미사용) |

## 최우선 보류 — 프리셋 1을 건드리는 항목

프리셋 2 수정 직후 바로 작업한다. 목록은 그때까지 여기 유지한다.

### A1. 성인 장면의 발성·소리·강도 우선순위

- 충돌 지점
  - 프리셋 2 Prose style boundary: 성적 장면 예외 문장이 있음 ("In sexual scenes, characters' speech, vocalization and sound follow the operator directions (3-2, 4-2) rather than this sentence.").
  - 프리셋 2 Expression register boundary: 같은 효력의 문장("cannot quietly lower the expressive strength… repeated sound, emotional force… duration")에 예외 없음.
  - 프리셋 1: "Once the event is chosen, give it its full expression: duration, density, repetition, volume…", "no low-to-high curve is assigned in advance" — 3-2 "처음부터 높지 않고"와 정면 충돌.
  - 프리셋 1: "When a cry, plea, refusal, breath, impact or environmental sound really repeats, keep its recurrence, spacing, interruption, vowel length and density", "Keep intentional sound spelling" — 3-2 의성어·말끝 늘이기 제한과 마찰.
  - 프리셋 2 성인 블록 "modifiers and sound follow 4-2": 의성어 규칙은 4-2가 아니라 3-2에 있음.
- 현재 처리: 헤더 우선순위로 시스템 프롬프트가 이기지만, 매 응답 판정을 추론하게 됨.
- 검토했던 안 (프리셋 2만 수정)
  - 성인 블록: `Characters' speech, vocalization, sound and how intensity rises follow the operator directions (3-2), and modifiers follow 4-2; in sexual scenes these take precedence over the prose style and expression register settings.`
  - Prose style boundary의 성적 장면 문장 삭제.
- 보류 이유: 충돌의 뿌리가 프리셋 1 문장이라 프리셋 1 작업과 함께 정한다.

## 반영 확정

### A2. 4-2 수식어 기준 — "관측되거나 셀 수 있는 값"

6-2와 같은 말로 맞추고, 온도·촉감·소리 같은 감각값을 살린다. 원래 예시의 "묵직하게"(인상)는 여전히 걸러진다.

- 한국어 4-2 (`system_prompt_v1.md` 149행, `preset_b4.md` 322행)
  - 현행: `명사 앞 수식과 동사 앞 부사는 보이거나 셀 수 있는 값만 남긴다.`
  - 수정: `명사 앞 수식과 동사 앞 부사는 관측되거나 셀 수 있는 값만 남긴다.`
- 영문 4-2 (`system_prompt_v1_en.md`/paste 137행)
  - 현행: `Before nouns and verbs, keep only modifiers whose value can be seen or counted.`
  - 수정: `Before nouns and verbs, keep only modifiers whose value can be observed or counted.`
- 프리셋 2 [Before writing] 앵커
  - `can be seen or counted` → `can be observed or counted` (B2 결정에 따라 앵커 문장 전체가 다시 바뀔 수 있음)

### A4. 3-2 강도 — 입력이 정한 강도는 입력을 따른다

- 한국어 3-2 (`system_prompt_v1.md` 105행, `preset_b4.md` 278행)
  - 현행: `{{user}}의 입력이 여러 단계를 담고 있으면 입력을 따르고, NPC끼리의 자율 장면에는 이 단계 제한을 두지 않는다.`
  - 수정: `{{user}}의 입력이 강도나 여러 단계를 정하면 입력을 따르고, NPC끼리의 자율 장면에는 이 단계 제한을 두지 않는다.`
- 영문 3-2 (93행)
  - 현행: `If {{user}}'s input contains several stages, follow the input, and scenes of NPCs acting on their own among themselves are not under this stage limit.`
  - 수정: `If {{user}}'s input sets the intensity or several stages, follow the input, and scenes of NPCs acting on their own among themselves are not under this stage limit.`
- 자율 장면 해제는 지금처럼 단계 제한에만 둔다.

### B3. 2-1 {{user}} 관계 — 함께 겪은 일까지

- 한국어 2-1 (`system_prompt_v1.md` 66행, `preset_b4.md` 239행)
  - 현행: `NPC는 자신이 {{user}}와 함께 겪어 온 관계를 처음부터 안다.`
  - 수정: `NPC는 자신이 {{user}}와 함께 겪어 온 관계와 그 안에서 보고 겪은 일은 처음부터 안다.`
- 영문 2-1 (54행)
  - 현행: `An NPC knows from the start the relationship they themselves have shared with {{user}}.`
  - 수정: `An NPC knows from the start the relationship they themselves have shared with {{user}} and what they saw and went through in it.`

### B4. 2-1 다른 인물의 공개 활동

{{user}}에게만 있던 "공개된 활동" 예외를 다른 인물에게도 연다. 3-1 "말하는 사람이 아는 들어온 순서"가 과하게 걸리지 않게 한다.

- 한국어 2-1 기록 줄 끝에 한 문장 추가 (`system_prompt_v1.md` 64행, `preset_b4.md` 237행)
  - 추가: `다른 인물의 공개된 활동은 그 인물의 업계와 관심에 따라 알 만한 만큼 안다.`
- 영문 2-1 기록 줄 끝 (52행)
  - 추가: `Characters know other people's public activities as far as their own industry and interests would let them.`

## 현행 유지

### A3. 3-1 "이미 써 온 호칭과 존비어는 이어 쓴다"

- 결정: 현행 유지. 앞선 이야기에 잘못된 표현이 남지 않도록 사용자가 직접 바로잡고 있다.
- 수정안이 더 안전한가에 대한 피드백: 아니다. 유지가 낫다.
  - 이 줄의 목적은 이미 쓴 쌍의 재계산을 건너뛰게 하는 것이다. "두 축에 어긋나지 않는 한"을 붙이면 매 턴 모든 쌍을 다시 검산하게 되어, 계산 부담과 추론 시간이 늘고 줄의 목적이 사라진다.
  - 얻는 안전성은 앞선 이야기에 오류가 남아 있을 때뿐인데, 지금 운용에서는 그 경우가 거의 없다.
  - 남는 위험은 장기기억 요약(HypaMinus 등)이 잘못된 호칭을 기록하는 경우다. 3-1 66행(가장 최근 기록이 현재 값)과 오류 발생 시 사용자 정정으로 처리된다.
  - 재검토 조건: 앞선 이야기에 남은 오류가 다음 턴으로 이어지는 일이 관찰되면 그때 다시 본다.

### B5. 설정 괄호에 캐릭터 설명 추가

- 결정: 미반영. 캐릭터 설명 칸에 인물 데이터를 넣지 않는다.

## 재검토 필요

### B1. 3-2 "의성어" — 사용자 의도: 대사의 과장 신음 차단

- 사용자 판단: 앞선 예시문 대사에서 과장된 신음이 남발되었고, 이 줄은 그것을 막는 용도다.
- 그렇다면 지금 문구의 문제는 반대 방향이다. "의성어"라는 말은 지문의 효과음(찌걱, 철썩)으로 먼저 읽히고, 5-2가 신음을 "대사"로 분류하므로 모델이 신음을 이 줄 밖으로 뺄 여지가 있다.
- 신음 과장은 이미 3-2 앞 줄("말끝을 늘이거나 감탄부호를 반복하는 것은 그 인물이 그 순간 실제로 그럴 때만")이 일부 막고 있다. 의성어 줄이 신음을 명시하면 두 줄이 같은 대상을 겨눈다.
- 방향 후보 (결정 대기)
  - ① 신음을 명시한다: `신음 같은 발성과 지문의 의성어는 실제로 쓰이는 한국어 소리만 드물게 쓴다.` — 대사와 지문 모두 덮는다.
  - ② 신음만 겨눈다: `신음 같은 발성은 실제로 쓰이는 한국어 소리로만 쓴다.` — 빈도는 앞 줄의 강도 규칙에 맡긴다. 지문 효과음은 제한이 풀린다.
  - 주의: "드물게"를 신음에 걸면 3-2 "말의 양은 성격대로"와 함께 읽혀, 원래 말이 많은 인물의 발성까지 줄어들 수 있다.
- 영문 3-2 (93행)도 같은 방향으로 맞춘다.

### B2. 프리셋 2 수식어 앵커의 대사 적용 여부

- 현재 상황
  - 4-2 본문은 스스로 범위를 정한다: `Style applies to narration. Dialogue follows each character's spoken Korean per 3-3 and 5-2.`
  - 프리셋 2 앵커에는 그 범위가 없다: `Before nouns and verbs keep only modifiers whose value can be seen or counted, and do not make warmth, sound, air or a gaze the subject that acts, as 4-2 sets.` 결과적으로 앵커가 본문보다 넓다.
- 대사까지 덮을 때 막히는 것
  - 4-2가 막는 대상은 지문이 효과를 단정하는 것이다. 대사에서 같은 말은 인물이 자기 판단을 말하는 것이라 성격이 다르다.
  - "분위기 왜 이래?", "공기가 무겁네", "목소리 좋다", "이상하게 좋아" 같은 평가와 인상은 실제 입말이다. 앵커가 대사에 걸리면 이런 말이 모두 막혀, 인물이 사실만 나열하는 딱딱한 말투가 된다.
  - 성적 장면에서 "뜨거워", "이상해" 같은 인물의 말도 걸린다.
- "묘하네"를 대사에서도 피하고 싶다면
  - 그건 수식어 규칙이 아니라 입말 문제다. 실제로 그 인물이 그 순간 하지 않을 말, 즉 글말 냄새가 나는 평가어다. 이미 5-2 입말 항목("한국어 화자가 그 순간 실제로 내뱉을 입말")이 다룬다.
  - 대사까지 막기로 정한다면 앵커만 넓히지 말고 4-2 본문의 범위 문장도 같이 바꿔야 한다. 앵커와 본문이 어긋나면 모델이 어느 쪽인지 매번 판정하게 된다.
- 선택지 (결정 대기)
  - ① 지문으로 한정: 앵커 앞에 `In narration,`을 붙인다. 4-2 본문과 일치. 권장안.
  - ② 대사까지 확장: 4-2 본문의 `Style applies to narration.` 문장을 고치고, 앵커는 그대로 둔다. 대사 견본(3-3)과 입말 규칙(5-2)도 함께 점검해야 한다.

## 반영 순서 (작업 시작 시)

1. 프리셋 2 수정: A2 앵커 (B2 결정 반영)
2. 한국어 시스템 프롬프트: A2, A4, B3, B4 (B1 결정 반영)
3. 영문본과 paste 파일 동기화
4. `preset_b4.md` 본문 동기화 (변경 기록 표의 인용문은 건드리지 않음)
5. 토큰 재계산 후 `test_paste.md` 표 갱신
6. 가이드 기준 재검수
7. 이어서 프리셋 1 작업: A1
