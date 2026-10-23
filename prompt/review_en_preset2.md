# 영문본·프리셋 2 재검수 — 결정 목록

대상: `system_prompt_v1_en_paste.txt`(= `system_prompt_v1_en.md`), `test_paste.md` ③ 프리셋 2. 한국어 원본 `system_prompt_v1.md`와 참조본 `preset_b4.md`는 반영 시 함께 동기화한다.

영문 행 번호는 `system_prompt_v1_en_paste.txt` 기준이다. 이 파일은 목록 정리만 한다. 아래 수정은 아직 어느 파일에도 반영하지 않았다.

## 상태 요약

| 항목 | 내용 | 결정 |
|---|---|---|
| A1 | 성인 장면 발성·소리: 문체 경계에만 예외, 표현 레지스터 경계·프리셋 1과 충돌 | 최우선 보류 (프리셋 1 작업) |
| A2 | 4-2 "보이거나 셀 수 있는 값"이 감각값을 막음 | 반영 |
| A3 | 3-1 "이미 써 온 호칭 이어 쓰기"가 과거 오류를 고정할 수 있음 | 현행 유지 |
| A4 | 3-2 "처음부터 높지 않고"에 입력 예외가 없음 | 반영 |
| B1 | 3-2 대사 속 신음의 빈도·강도 (금지 아님) | 재검토안 결정 대기 (②안 철회) |
| B2 | 프리셋 2 수식어 앵커가 대사까지 덮음 | 반영 (①안, 지문 한정) |
| B3 | 2-1 {{user}} 관계 문장이 "관계"만 덮음 | 반영 |
| B4 | 2-1 다른 인물의 공개 활동 인지 | 반영 |
| B5 | 설정 괄호에 캐릭터 설명 추가 | 미반영 (캐릭터 설명 칸 미사용) |
| C1 | 합의 없이 천편일률적으로 존댓말을 쓰는 문제 | 반영 (초안 문구 확정) |
| C2–C8 | 충돌 없음 확인 항목 | 유지 |

## 최우선 보류 — 프리셋 1을 건드리는 항목

프리셋 2 수정 직후 바로 작업한다. 목록은 그때까지 여기 유지한다.

### A1. 성인 장면의 발성·소리·강도 우선순위

- 충돌 지점
  - 프리셋 2 Prose style boundary: 성적 장면 예외 문장이 있음 ("In sexual scenes, characters' speech, vocalization and sound follow the operator directions (3-2, 4-2) rather than this sentence.").
  - 프리셋 2 Expression register boundary: 같은 효력의 문장("cannot quietly lower the expressive strength… repeated sound, emotional force… duration")에 예외 없음.
  - 프리셋 1: "Once the event is chosen, give it its full expression: duration, density, repetition, volume…", "no low-to-high curve is assigned in advance" — 3-2 "처음부터 높지 않고"와 정면 충돌.
  - 프리셋 1: "When a cry, plea, refusal, breath, impact or environmental sound really repeats, keep its recurrence, spacing, interruption, vowel length and density", "Keep intentional sound spelling" — 3-2 신음·말끝 늘이기 제한과 마찰.
  - 프리셋 2 성인 블록 "modifiers and sound follow 4-2": 4-2에는 소리 규칙이 없음. B1 반영 후 신음 규칙은 3-2에 있고, 지문 의성어 제한은 없어짐.
- 현재 처리: 헤더 우선순위로 시스템 프롬프트가 이기지만, 매 응답 판정을 추론하게 됨.
- 검토했던 안 (프리셋 2만 수정)
  - 성인 블록: `Characters' speech, vocalization, sound and how intensity rises follow the operator directions (3-2), and modifiers follow 4-2; in sexual scenes these take precedence over the prose style and expression register settings.`
  - Prose style boundary의 성적 장면 문장 삭제.
- 보류 이유: 충돌의 뿌리가 프리셋 1 문장이라 프리셋 1 작업과 함께 정한다.

## 반영 확정

### A2 + B2. 4-2 수식어 기준 — "관측되거나 셀 수 있는 값", 앵커는 지문 한정

B2 재검수(예시문 기준): 예시의 문제는 지문의 상투 수식어("묵직한")와 대사 속 신음이었다. 대사 속 수식어는 증상에 없었고, 대사 속 신음은 4-2가 아니라 3-2(B1)가 맡는다. 지문 한정 ①안 유지.

6-2와 같은 말로 맞추고, 온도·촉감·소리 같은 감각값을 살린다. 원래 예시의 "묵직하게"(인상)는 여전히 걸러진다. 앵커는 4-2 본문의 범위("Style applies to narration")와 맞춰 지문으로 한정한다. 대사 속 평가어("묘하네" 류)는 5-2 입말 항목이 다룬다.

- 한국어 4-2 (`system_prompt_v1.md` 149행, `preset_b4.md` 322행)
  - 현행: `명사 앞 수식과 동사 앞 부사는 보이거나 셀 수 있는 값만 남긴다.`
  - 수정: `명사 앞 수식과 동사 앞 부사는 관측되거나 셀 수 있는 값만 남긴다.`
- 영문 4-2 (`system_prompt_v1_en.md`/paste 137행)
  - 현행: `Before nouns and verbs, keep only modifiers whose value can be seen or counted.`
  - 수정: `Before nouns and verbs, keep only modifiers whose value can be observed or counted.`
- 프리셋 2 [Before writing] 앵커
  - 현행: `- Before nouns and verbs keep only modifiers whose value can be seen or counted, and do not make warmth, sound, air or a gaze the subject that acts, as 4-2 sets.`
  - 수정: `- In narration, keep only modifiers before nouns and verbs whose value can be observed or counted, and do not make warmth, sound, air or a gaze the subject that acts, as 4-2 sets.`

### A4. 3-2 강도 — 입력이 정한 강도는 입력을 따른다

- 자율 장면 해제는 지금처럼 단계 제한에만 둔다. 같은 줄의 의성어 문장은 B1 결정에 따른다.
- 한국어 3-2 (`system_prompt_v1.md` 105행, `preset_b4.md` 278행)
  - 현행: `{{user}}의 입력이 여러 단계를 담고 있으면 입력을 따르고, NPC끼리의 자율 장면에는 이 단계 제한을 두지 않는다.`
  - 수정: `{{user}}의 입력이 강도나 여러 단계를 정하면 입력을 따르고, NPC끼리의 자율 장면에는 이 단계 제한을 두지 않는다.`
- 영문 3-2 (93행)
  - 현행: `If {{user}}'s input contains several stages, follow the input, and scenes of NPCs acting on their own among themselves are not under this stage limit.`
  - 수정: `If {{user}}'s input sets the intensity or several stages, follow the input, and scenes of NPCs acting on their own among themselves are not under this stage limit.`

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

### C1. 합의 없이 천편일률적으로 존댓말을 쓰는 문제 — 방향 수정

- 관찰 (사용자): 합의 없이 전부 존댓말로 굳는 양상이 훨씬 심각하다. 그러지 않아야 할 인물들까지 모두 이렇게 나온다.
- 이전 판단 정정: 첫 검수에서 "추정한 친분으로 반말을 여는 쪽이 더 위험하다"며 유지를 권했으나, 실제로는 반대 방향 실패가 주된 문제다.
- 원인 (문장 구조)
  - 3-1에서 반말로 가는 길은 모두 관문을 거친다: 합의 줄(69행)은 앞선 이야기나 설정이 반말 사이로 "보여 줄" 때만 합의를 인정하고, 75행 초면 존댓말, 76행 반말은 허락·합의 필요, 77행 반대 축 상호 존댓말, 78행 "나이만으로 반말이 시작되지 않는다·동갑은 초면 존댓말".
  - 반대로 존댓말은 근거 없이도 성립한다. 근거가 모자라면 모든 판정이 존댓말로 떨어진다.
  - 65행(첫 등장 관계)은 "이미 아는 사이인지, 얼마나 가까운지"를 정하게 하지만, 그렇게 정한 관계는 69행의 합의 근거에 들지 않는다. 그래서 작중에서 몇 년을 알고 지낸 사이로 정해져도 존비어 계산에서는 초면처럼 처리된다.
  - 1-2는 "흔한 기본값을 고르지 않는다"고 하지만, 3-1 안에서는 존댓말이 사실상 기본값이다.
- 수정 방향
  - 이전 안: 65행대로 정한 관계를 합의 근거에 넣는다. → 친분이 "보여야" 반말이 열리는 구조는 그대로라 근거 부족 시 존댓말로 떨어지는 문제가 남는다.
  - 수정 방향: 이미 알고 지내 온 쌍은 합의를 "찾는" 대신, 지금 실제로 쓰고 있을 존비어 자체를 관계 사실로 정한다. 그 값에 필요한 합의는 이미 있는 것으로 본다. 근거 부족을 이유로 존댓말을 기본값으로 고르지 않는다.
  - 유지하는 안전장치: 이번 장면에서 친해 보인다는 것만으로는 합의가 아니다(기존 문장), 77행 반대 축, 70행 공적 상황 판정, 75행 초면 규칙은 실제로 처음 만난 쌍에만 적용.
- 확정 문구 — 한국어 3-1 합의 줄 (`system_prompt_v1.md` 69행, `preset_b4.md` 254행). 3-1은 영문본에도 한국어 원문으로 들어가므로 같은 문구.
  - 현행: `합의와 허락: 이 항목에서 반말과 사적 호칭에 필요한 합의와 허락은, 합의하거나 허락하는 장면이 본문에 서술됐을 때만 성립하는 것이 아니다. 앞선 이야기나 설정(로어북·페르소나)이 그 쌍을 이미 반말이나 사적 호칭으로 지내 온 사이로 보여 주면 합의와 허락이 있는 것으로 본다. 반말이나 사적 호칭을 이미 써 온 기록, 그렇게 지낼 만한 친분이 앞선 이야기에 서술된 경우가 여기에 든다. 이번 장면에서 친해 보인다는 것만으로는 합의나 허락이 아니다.`
  - 수정: `합의와 허락: 이 항목에서 반말과 사적 호칭에 필요한 합의와 허락은, 합의하거나 허락하는 장면이 본문에 서술됐을 때만 성립하는 것이 아니다. 작중 세계에서 이미 알고 지내 온 쌍(앞선 이야기, 설정(로어북·페르소나), 앞 항목대로 정한 관계)은 계산 요소와 함께 지낸 기간으로 지금 실제로 쓰고 있을 호칭과 존비어를 1-2대로 가장 있을 법하게 정하고, 그 값에 필요한 합의와 허락은 이미 있는 것으로 본다. 근거가 모자란다는 이유로 존댓말을 기본값으로 고르지 않는다. 이번 장면에서 친해 보인다는 것만으로는 합의나 허락이 아니다.`
- 확인할 점
  - 반말이 과하게 열리는 반대 실패가 생기는지 테스트로 본다. 관찰 대상: 공적 자리의 반말, 연하가 먼저 반말하는 경우, 반대 축 쌍.
  - 65행 끝 문장("호칭과 존비어는 그 관계를 바탕으로 아래 기준으로 계산한다")은 손대지 않는다. 반영 후 재검수에서 겹침이 문제가 되면 그때 본다.
  - 프리셋 2 [Before writing]에 존비어 앵커를 둘지는 테스트 결과를 보고 정한다.

## 재검토안 — 결정 대기

### B1. 대사 속 신음의 빈도·강도

- 사용자 의도: 큰따옴표 대사 안에 "아앙" 같은 신음이 부적절하게 남발되는 것을 막는다. 금지가 아니라 빈도와 강약의 문제다.
- 근거 증상 (G11 기록, 운영자 예시): 대사마다 감탄 신음, 첫 대사부터 최고 강도, 말끝 모음 늘이기, 정형 대사 반복.
- ②안 철회 이유: `신음 같은 발성은 실제로 쓰이는 한국어 소리로만 쓴다`는 소리의 종류만 정한다. "아앙"은 실제로 쓰이는 소리라 이 문장을 통과하고, 빈도와 강도에는 아무 작용이 없다.
- 현행에서 빈도·강도를 다루는 문장
  - 3-2 103행 `섞이는 말과 빈도는 인물마다 다르고` — 차이만 말하고 빈도의 기준이 없다. 대사마다 붙여도 위반이 아니다.
  - 3-2 104행 `발성의 강도는 처음부터 높지 않고…말끝을 늘이거나 감탄부호를 반복하는 것은…실제로 그럴 때만` — 강도는 다루지만, 길게 끄는 신음 자체는 "말끝 늘이기"로 읽히지 않을 수 있다.
  - 3-2 105행 `의성어는…드물게` — 신음에 걸리는지 모호하다(5-2가 신음을 대사로 분류).
  - 압축 전 원문은 신음 단계(弱·中·强 음절 수)로 강도를 묶었으나, 숫자 기준은 쓰지 않기로 했다(G11).
- 재검토안: 신음은 104행(강도 줄)에 모으고, 105행 의성어는 지문으로 한정한다.
  - 빈도: 원인에 묶는다. 소리가 나올 자극이 있을 때만 섞이고, 대사마다 붙지 않는다. 프리셋 1의 "really repeats"(실제 원인 있는 반복만 유지)와 같은 논리라 충돌이 줄어든다.
  - 강도: 기존 "말끝 늘이기·감탄부호 반복"에 "소리를 길게 끌기"를 더해 신음 자체의 늘임을 덮는다.
  - 지문 의성어: G12에서 복원한 만화식·외래식 의성어 차단 기능은 유지하되 "지문의"로 범위를 밝혀 신음과 겹치지 않게 한다.
- 문구안
  - 한국어 3-2 104행 (`preset_b4.md` 277행)
    - 현행: `발성의 강도는 처음부터 높지 않고, 장면의 진행과 그 인물에 따라 달라진다. 끝까지 크게 오르지 않는 인물도 있다. 말끝을 늘이거나 감탄부호를 반복하는 것은 그 인물이 그 순간 실제로 그럴 때만 쓴다.`
    - 수정: `신음은 그 순간의 자극에 실제로 소리가 나올 때만 대사에 섞이고, 대사마다 붙지 않는다. 발성의 강도는 처음부터 높지 않고, 장면의 진행과 그 인물에 따라 달라진다. 끝까지 크게 오르지 않는 인물도 있다. 소리를 길게 끌거나 말끝을 늘이거나 감탄부호를 반복하는 것은 그 인물이 그 순간 실제로 그럴 때만 쓴다.`
  - 한국어 3-2 105행 (A4와 같은 줄)
    - 현행: `의성어는 실제로 쓰이는 한국어 의성어만 드물게 쓴다.`
    - 수정: `지문의 의성어는 실제로 쓰이는 한국어 의성어만 드물게 쓴다.`
  - 영문 3-2 92행
    - 수정: `Moans mix into a line only when the stimulus of that moment actually draws a sound, not into every line. The intensity of vocalization does not start high; it varies with the scene's progress and the character. Some characters never rise very far. Drag out a sound, stretch word endings or repeat exclamation marks only when that character would actually do so at that moment.`
  - 영문 3-2 93행
    - 현행: `Use only Korean onomatopoeia that people actually use, and rarely.`
    - 수정: `In narration, use only Korean onomatopoeia that people actually use, and rarely.`
- 선택 사항: 프리셋 2 [Before writing] 앵커
  - `- In sexual scenes, a moan enters a line only when the moment actually draws one, as 3-2 sets.`
  - 권장: 처음에는 넣지 않고 테스트한다. 선배 오류처럼 재발이 이어지면 그때 추가한다. 성인 블록이 이미 3-2를 가리키고 있다.
- 테스트 관찰: 신음이 대사마다 붙는지, 첫 대사부터 길게 끄는지, 반대로 신음이 지나치게 사라지는지.

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

### C2–C8. 충돌 없음 확인

- C2. 전지적 시점과 2-1 정보 격리: 프리셋 문장("Characters still cannot use facts they have not learned")과 2-1 귀속 줄이 막는다. Observational restraint의 "sparse"도 "may reveal"과 함께 성립한다.
- C3. 4-3 티키타카 구간과 프리셋 1 volley 경계: 4-3에 명시적 예외가 있다.
- C4. 5-1 "요지만"과 프리셋 Input status: 단언과 미완료라는 양태는 유지되므로 충돌하지 않는다. 4-4는 5-1 제한에서 따로 빠져 있다.
- C5. 헤드라인 위치: 6의 출력 순서와 "this order" 예외 문장이 헤드라인까지 덮으므로 프리셋 1의 제목 금지와 충돌하지 않는다.
- C6. 헤더 G7(설정 우선)과 3-1 [CRITICAL], 프리셋 출처 순서: 세 곳의 방향이 같다.
- C7. 물결표 삭제: 범위는 5-2 숫자 규칙("2주에서 3주")이 처리한다.
- C8. Description-led의 "atmosphere"와 4-2 추상명사 금지: 약한 마찰은 있으나 4-2의 "근거 있는 이미지만"과 헤더 우선순위로 정리된다. 수정하지 않는다.

## 반영 순서 (작업 시작 시)

1. B1 문구 확정
2. 프리셋 2 수정: A2+B2 앵커
3. 한국어 시스템 프롬프트: A2, A4, B1, B3, B4, C1
4. 영문본과 paste 파일 동기화 (3-1은 한국어 원문 그대로)
5. `preset_b4.md` 본문 동기화 (변경 기록 표의 인용문은 건드리지 않음)
6. 토큰 재계산 후 `test_paste.md` 표 갱신
7. 가이드 기준 재검수
8. 이어서 프리셋 1 작업: A1
