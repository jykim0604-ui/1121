# 테스트용 프리셋 1/2 (v5 번호) 수정안: 원본 프리셋에서 차용

- 대상: `preset_test_v5.md` (테스트용 프리셋, 앵커 번호를 v5에 맞춘 판)
- 차용원: `preset_toggle_only.md` (원본 프리셋, 토글 고정)
- 짝: `system_prompt_v5_ko.md` / `_en.md`. 1-1과 5-4는 이번에 세 방향(빠른 주고받기는 선택지, 농담은 기본값이 아님, 시점 이동 시 내면 묘사 절제)으로 맞춘 판이다.
- 근거
  - 문제 목록: `v5_standalone_issues.md`
  - 대조표: `test_preset_coverage.md`
  - 출력: `output_samples.md` (예시 1: 테스트판, 예시 2: 원본, 예시 3: v5 단독)
- 상태: 수정안이다. 아직 반영하지 않았다.

---

## 0. 앵커가 가리키는 이름

- 테스트판 앵커 18곳은 시스템 프롬프트를 "the operator directions (n-n)"로 부른다.
- 예시 1을 낼 때 짝이던 v1/v2 제목은 `[Operator Directions — 이 작품의 고정 지시]`였다. v5 제목은 `[이 작품의 고정 지시]` / `[Fixed Directions for This Work]`라서 이 이름이 없다.

| 안 | 내용 | 바뀌는 곳 |
|---|---|---|
| A (권장) | 프리셋과 짝지어 쓸 때만 v5 제목을 `[Operator Directions — 이 작품의 고정 지시]` / `[Operator Directions — Fixed Directions for This Work]`로 쓴다 | v5 제목 한 줄. 테스트판이 실제로 작동했을 때와 같은 이름이다 |
| B | 앵커 18곳의 "the operator directions"를 "the Fixed Directions for This Work ([이 작품의 고정 지시])"로 바꾼다 | 프리셋 18곳 |

---

## 1. Output range: 첫 문장을 원본으로 (문제 3 대화 전개, 문제 7 {{user}} 상태)

- 현재 (테스트판): "Output range: Interaction handoff. **Continue through the reactions the input causes and the development that follows, then stop at the point where {{user}}'s next speech, decision or action is needed.** Do not cross a second information or action threshold: opening something closed, revealing a clue, changing location beyond where the input is already heading, or carrying out its consequence is a second threshold unless … An action a character other than {{user}} has already started is carried to its result as the operator directions (9-1) set. The response does not end where the input ends; what follows the input runs as the operator directions (2-3, 9-1) set. In autonomous-novel mode, …"
- 원본: "Output range: Interaction handoff. **Complete the first reaction that leaves a meaningful choice, then stop before new input is needed.** Do not cross … changing location, starting the next exchange or carrying out its consequence …"
- 수정안
  - 굵게 표시한 첫 문장만 원본 문장으로 바꾼다.
  - 나머지는 테스트판 그대로 둔다. 장소 범위 한정, "starting the next exchange" 제외, 9-1과 2-3·9-1 앵커 두 개가 남는다.
- 근거
  - 예시 1(테스트판)은 "the reactions the input causes"를 따라 입력(이틀 동안 고기를 구움)에서 {{user}}의 손목 상태를 지어냈다. 대화도 그것을 쫓아가다 무너졌다(기타 → 폭로 → 손목 반복).
  - 예시 2(원본 문장)에는 지어낸 {{user}} 상태가 없고, 대화가 장면에 있는 것에서 이어졌다.
  - 남겨 두는 두 앵커가 '데이트인가?' 문제(입력이 끝난 자리에서 응답이 끝남, G24·G25)를 계속 막는다.

## 2. 대화 리듬: 원본 구절 복원 + 앵커를 v5 1-1 방향에 맞춤 (문제 3, 문제 9)

- 위치: ① [Writing the Passage] Speech 문단
- 현재: "… Volleys of short questions met by denials, reversals, quips or echoes are not the default way to sustain a scene, even when each line carries a little information. The quick back-and-forth stretch that the operator directions (1-1) allow is not such a volley."
- 원본: "… even when each line carries a little information; **use a rapid rhythm only where the work or the moment calls for it.**"
- 수정안
  > … Volleys of short questions met by denials, reversals, quips or echoes are not the default way to sustain a scene, even when each line carries a little information; use a rapid rhythm only where the work or the moment calls for it. The quick back-and-forth stretch that the operator directions (1-1) allow is that kind of rapid rhythm: an option for when the moment calls for it, not the default.
- 근거
  - 테스트판 앵커("is not such a volley")는 대사만 잇는 구간을 질문 연발 경계에서 빼 주었다. 예시 1의 한 줄 말다툼 여섯 번이 이 상태에서 나왔다.
  - 원본 구절과 v5 1-1의 새 문장("기본값이 아니라 장면이 빠른 리듬을 부를 때 고르는 선택지")은 같은 방향이라 함께 둘 수 있다.

## 3. 농담 기본값: 테스트판 유지 (원본 차용 안 함)

- 위치: ① [Characters, Tone and Focus]
- 현재: "Do not default to banter. Teasing, quips and comic reactions belong to characters and scenes that are actually comic."
- 원본: "… Teasing, quips, comic reactions **and rapid back-and-forth** belong to characters and scenes that are actually comic."
- 수정안: 바꾸지 않는다.
- 근거
  - 원본의 "and rapid back-and-forth"를 되살리면 빠른 주고받기가 코미디 장면에만 허용된다. v5 1-1(장면이 빠른 리듬을 부를 때의 선택지, 긴장된 장면도 포함)과 범위가 달라진다.
  - 빠른 리듬은 2번에서 원본 구절로 묶는다.
  - 농담과 놀림은 이 문장과 v5 1-1의 새 문장("그런 성격과 관계, 설정이 그런 자리로 정한 장소에서만")이 같은 방향으로 맡는다.

## 4. 묘사 앵커 세 개 삭제, 원본 문장으로 (문제 4 묘사·표현, 문제 8 대화 밖 인물)

| 위치 | 현재 (테스트판에서 덧붙인 문장) | 수정안 |
|---|---|---|
| ③ Composition: Description-led 끝 | "Setting, period and surroundings come in through the objects, ways of working and people of the scene, and atmosphere and imagery through the concrete actions, sounds and things that produce them, as the operator directions (2-1, 2-4, 2-6) set." | 이 문장을 지우고 원본 분기 문장만 남긴다 |
| ③ Prose style: Literary 끝 | "Motifs and images appear only where the sources or the scene ground them, as the operator directions (2-6) set." | 이 문장을 지우고 원본 문장만 남긴다 |
| ③ [Before writing] | "- In narration, write the actions, sounds, reactions and concrete people and things that produce an effect instead of modifiers …, as 2-6 sets." | 이 줄을 지운다 (원본 [Before writing]에는 없음) |

- 근거
  - 세 문장이 모두 있던 예시 1에서는 굳은 몸짓("눈을 반짝이며 … 총총", "얼굴이 붉어진 … 손사래")이 나왔고, 여덟 명 중 둘만 들어왔다.
  - 세 문장이 모두 없던 예시 2는 묘사, 지문 구조, 대화 밖 인물 모두 올바랐다.
  - 효과에 이름만 붙이는 수식어는 예시 2와 3(v5만 있음)에서 나오지 않았다. v5 2-6이 혼자 막는다.
  - 원본 [Writing the Passage]의 "Let the scene carry emotion … through what people do", "action beats for actions that matter", 원본 [Characters, Tone and Focus]의 "Other people have their own business"는 테스트판에도 그대로 있다. 따로 차용할 것은 없다.

## 5. 바꾸지 않는 항목

| 문제 | 테스트판 상태 | 판단 |
|---|---|---|
| 1 끝맺음 | 원본과 같음 | 프리셋에 차용할 원본 문장 없음. v5 1-3 버튼("직전 턴과 같은 방식으로 끝내지 않는다")이 맡음 |
| 2 호칭·말투 | 테스트판 보강(앵커 3곳, -ssi 삭제), 번호를 7-2로 수정함 | 유지. 예시 1 때 "존비어 해결" 확인 |
| 5 나레이션 | Continuation point의 "When the input states that something is complete … treat it as already shown …"를 삭제한 상태 | 유지. 원본 문장은 끝난 입력을 다시 그리지 않게 하는 문장이라 v5 2-2 나레이션 입력(풀어 쓰기)과 반대 방향이다. 흐린 요약을 막는 근거는 되지 않는다 |
| 6 사실 세부 | 원본과 같음 | 유지. 설정 확인 사항 |
| 잡담 예외 (A10, "as 2-1 allows") | 테스트판 | 유지. v5 2-1 잡담 허용과 짝이다. 예시 1·2의 폭로 대사는 이 예외가 없던 예시 2에서도 나왔으므로 원인으로 보지 않음 |
| 성인 장면 앵커, 자아 유지 앵커 | 번호만 수정함 | 보류 (NSFW 테스트 뒤 확정) |
| 그 밖 (숫자 표기 삭제, 번역 병기 삭제, 인물 지칭 구절 삭제, 조용한 장면·침묵 문장 삭제) | 테스트판 | 이번 문제 9개와 관계없음. 유지 |

---

## 요약

| # | 수정 | 원본 차용 |
|---|---|---|
| 0 | 앵커 이름 맞춤 (A안: 프리셋과 쓸 때 v5 제목에 Operator Directions) | — |
| 1 | Output range 첫 문장 | 원본 문장으로 교체 |
| 2 | Speech 문단 | 원본 구절 복원 + 1-1 앵커 문구 조정 |
| 3 | 농담 줄 | 차용 안 함 (v5 1-1과 범위가 달라짐) |
| 4 | 묘사 앵커 세 개 | 삭제하여 원본 상태로 |
| 5 | 그 밖 | 유지 |
