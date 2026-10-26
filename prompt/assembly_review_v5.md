# 조립본 검수: 테스트용 프리셋 1 → 시스템 프롬프트 v5 → 테스트용 프리셋 2

- 대상
  - 프리셋: `preset_test_v5.md` ①·③ (v5 번호, 수정안 1~4 반영)
  - 시스템 프롬프트: `system_prompt_v5_ko.md` / `_en.md`
    - 1-1·5-4 통일 반영
    - 제목 `[Operator Directions — …]` (fixes 0번 A안) 반영
- 기준 (가이드 §10.1)
  - 충돌: 같은 결정을 같은 범위에서 두 층이 다르게 정한 것
  - 중복: 같은 대상, 조건, 강도를 두 층이 모두 정한 것
- 처리 원칙 (사용자 지시)
  - 중복은 프리셋에서 지운다. 단 묘사에 지장이 없을 때만 지운다.
  - 유력 대상은 존비어다.
- 상태: 검수 결과와 수정안이다. 아직 반영하지 않았다.
- 표기: P1-n은 프리셋 ① n번째 줄, P2-n은 프리셋 ③ n번째 줄이다(코드블록 안 기준).

---

## 1. 중복

### 1-1. 존비어 (유력 대상)

| 프리셋 ① [Language and Voice] | v5 7-2 | 판정 |
|---|---|---|
| P1-94 "For Korean dialogue, bind DIRECTIONAL SPEECH REGISTER STATE for each speaker-to-listener direction …" | "호칭과 존비어도 따로, 말하는 방향마다 정한다" | 중복 |
| P1-94 "Start with accepted speech and explicit relationships, then culture, milieu, age/generation/school year, status, familiarity and individual formality." | 「이렇게 정한다」 첫 줄(이미 정해진 쌍은 이어 씀) + 「정해지지 않은 쌍의 계산」(나이, 들어온 시기, 직급, 친밀도, 자리) | 중복 |
| P1-94 "In a contemporary Korean secondary school, same-year peers ordinarily use peer casual speech …" | 초면과 아직 가깝지 않은 사이는 존댓말이 기본 | **충돌** (학교 배경일 때). v5가 정함 |
| P1-94 "Narration, inner language, involuntary voice and the reverse direction remain separate." | "말하는 방향마다 정한다", "혼잣말과 속마음에서도 같은 호칭을 쓴다" | 반대 방향은 중복. 속말은 다르게 읽힐 수 있음. v5가 정함 |
| P1-95 "Inherit each direction across completed utterances. Emotion, attraction, embarrassment, fear, intimacy and escalation do not themselves change speech level. A deliberate switch is a speaker-owned event with a cause …" | "이미 정해진 사이의 호칭과 존비어는 두 사람이 합의하거나 두 사람 사이를 바꾸는 일이 본문에 있을 때만 바뀐다", "이번 장면에서 친해 보인다는 것만으로 서로 말을 놓지 않는다" | 중복 |
| P1-95 "Source-established banjondae is a pattern …", "A shortened address or unreached ending does not establish a new level.", "Preserve rhetorical variety and incomplete speech without accidentally completing another register.", "Before submission … correct uncaused switching, address/ending mismatch, stray yo, unstable imitation …" | 없음 | **v5에 없는 기능** (반존대 패턴, 말끝 흔들림, 요 섞임 점검) |
| P1-94·95 앵커 "address and speech level … set by the operator directions (7-2)", "each direction inherits the state 7-2 sets; … the uncaused switch to correct …" | — | 테스트 때 존비어를 해결한 앵커 (예시 1) |
| P2-208 [Before writing] "Keep the address and speech level each pair already uses … as 7-2 sets; do not call someone 선배 who joined after the speaker …" | 7-2 "나중에 들어온 사람을 선배라고 부르지 않는다" | 중복이지만 **출력 직전 앵커**(효과 확인된 자리) |

- 묘사 영향: 없음. 대사의 존비어와 호칭만 정하는 문장이고, 지문·묘사 문장은 들어 있지 않다.
- 수정안
  - P1-94·95 두 줄을 지우고, 아래 한 줄로 바꾼다.
  - 남기는 것: 7-2 앵커 두 개, 그리고 v5에 없는 기능(반존대, 말끝, 요 섞임 점검).
  - 지우는 것: 중복된 판정 절차와 학교 동갑 기본값(충돌).
  - P2-208 출력 직전 앵커는 그대로 둔다.

  > - In this work, address and speech level between characters in Korean dialogue are set by the operator directions (7-2), for each speaker-to-listener direction; each direction inherits the state 7-2 sets, and an utterance that departs from it, even the first in this response, is the uncaused switch to correct, not a new state to carry forward. Source-established banjondae is a pattern, not random alternation, and a shortened address or unreached ending does not establish a new level. Before submission, read completed utterances directionally and chronologically and correct uncaused switching, address/ending mismatch and stray yo without exposing the audit.

### 1-2. 그 밖의 중복

| # | 프리셋 | v5 | 묘사 영향 | 수정안 |
|---|---|---|---|---|
| D1 | P1-45 "Do not default to banter. Teasing, quips and comic reactions belong to characters and scenes that are actually comic." / P2-205 "add no banter, cheer or affection …" | 1-1 "농담과 놀림은 기본값이 아니다. 그런 성격과 관계, 설정이 그런 자리로 정한 장소에서만 나온다." | 없음 (어조 판정) | P1-45 삭제. P2-205는 banter 외에 cheer·affection도 다루므로 유지 |
| D2 | P1-60·61 [Ending the Response] "…a question or options for the operator, characters staring at {{user}} in silence …" / P2-207 "stop inside the scene without a question, options or a waiting stare aimed at {{user}} unless the scene itself ends there" | 9-1 "{{user}}가 응답할 차례라는 것을 본문에 드러내지 않는다. 대답을 기다리는 시선이나 공기도 …", 2-3 "응답은 장면 안에서 끝낸다. 다음 행동, 이야기 제안 … 은 {{user}}의 몫" | 없음 | 프리셋 두 층이 같은 말을 두 번 하고, v5가 세 번째로 한다. P1-61은 착지 판정이므로 v5에 맡기고 삭제. P2-207은 출력 직전 자리라 유지. 질문 끝맺음 허용("When the scene genuinely stops on another character's question … that is fine")은 사용자 판단(장면상 자연스러우면 허용)과 같은 방향이라 P2-207의 "unless the scene itself ends there"가 그대로 맡음 |
| D3 | P1-28 "Do not leap past the current movement: no jump of days, months or years … unless the operator asks for it." | 4-2 "시간 도약 확정은 {{user}}의 권한", 8-1 "시간 도약을 명시하지 않은 턴에는 큰 시간이 흐르지 않는다" | 없음 | 겹치는 것은 이 문장 하나다. 같은 줄의 "Cover only the time the current movement needs"는 v5에 없는 기능이라, **줄 전체는 유지**한다 |
| D4 | P1-29 "Stay inside the current event … The operator may want to spend many turns inside one event." / P2-204 "Stay inside the current event …" | 2-1 "{{user}}가 다음으로 넘길 때까지 같은 장면을 이어 간다", 4-2 "장면의 최종 종료 … {{user}}의 권한" | 없음 | 프리셋 안에서도 두 번 나온다. P2-204는 출력 직전 요약이라 유지. P1-29는 "conversation … meal, journey"처럼 사건 단위로 v5보다 넓어서 유지 |
| D5 | P1-68 "Characters know only what they have perceived or learned. Names and labels from the card are not common knowledge." | 4-3 인지 경계 전체 | 없음 | 같은 줄 앞부분("Each fact belongs to its own person …")은 v5에 없는 기능이라 줄 전체는 유지. 지우지 않음 |
| D6 | P2-20 1:1 앵커 "In a scene with only {{user}} and one NPC, {{user}}'s responses follow the operator directions (1-1, 9-1)." | 1-1 "{{user}}와 NPC 한 명뿐이면 … 그 NPC가 혼자 이어 간다" | 없음 | 앵커라 유지 |

- 묘사 쪽 문장은 v5와 겹치는 것이 있어도 지우지 않는다.
  - 대상: [Writing the Passage] 전체, full expression, 소리 문장, Composition, Prose style, Narrative distance, "The world does not revolve around {{user}}"
  - 이유: 예시 2에서 묘사를 맡은 문장들이다.

---

## 2. 충돌

| # | 프리셋 | v5 | 충돌 내용 | 수정안 |
|---|---|---|---|---|
| C1 | P2-20 Collaborative RP "you may add only a strongly implied, low-commitment micro-action or an immediate involuntary or sensory reaction of {{user}}'s" | 2-2 머리말 "{{user}}의 행동과 대사는 입력창 문자열에서만 나온다 … 입력에 없는 새 행동이나 대사, 결정을 더하는 것은 아니다" | 입력에 없는 {{user}}의 작은 동작과 반응을 써도 되는지가 서로 다르다. 예시 1(손목)과 예시 3(피곤함, 다크서클)에서 {{user}}의 상태가 지어졌다 | 프리셋 문장 끝에 앵커 한 문장: "In this work, what {{user}} does comes from the input as the operator directions (2-2) set; a micro-action or reaction may only accompany an action the input already states, and no state of {{user}}'s body or mood is invented for other characters to react to." |
| C2 | P1-96 "In Korean … use a dash for a real cutoff" | 6-1 "문장 연결과 말 끊김은 쉼표, 마침표, 말줄임표, 줄바꿈으로 처리한다" | 말이 끊길 때의 표기(대시 / 말줄임표 등) | 표기는 v5가 맡으므로 프리셋의 "use a dash for a real cutoff," 구절만 지운다. 같은 줄의 띄어쓰기, 늦춘 음절 규칙은 v5에 없으니 유지. 묘사 영향 없음 |
| C3 | P1-94 학교 동갑 반말 기본값 | 7-2 초면 존댓말 기본 | 1-1에 포함 (존비어 줄 정리로 해소) | — |

## 3. 주의 (같은 결정이 아니거나 앵커로 이미 정리됨, 테스트에서 확인)

| # | 프리셋 | v5 | 내용 |
|---|---|---|---|
| W1 | P1-60 "End … on an action, a line, an image or a consequence" | 9-1 "순수 관찰이나 분위기 서술로 본문을 끝내지 않는다", 1-3 버튼 | "an image"가 관찰 끝맺음으로 읽힐 여지. 1-3이 "인물의 동작으로", 인서트는 인물 동작 안에 두라고 정함 |
| W2 | P2-162 Scene pacing "cannot … add a beat" | 9-1 "진전시킬 것이 없으면 … 새 행동으로 다음 박자를 연다" | 9-1의 박자 정의(다음 움직임 시작까지)로 정리됨 |
| W3 | P2-87 Output range "revealing a clue … is a second threshold" / P2-142·146 "does not require a durable change in every response" | 9-1 정체 방지 "응답마다 위치, 정보, 관계, 상황 가운데 무언가를 진전시킨다" | 프리셋은 지속적 변화와 단서 공개를 막고, v5는 작은 진전을 요구한다. 9-1 "진전시킨 것이 나중에 쓰여야 하는 것은 아니다", "조용한 장면은 조용한 채로"와 같은 방향이라 같은 결정은 아님 |
| W4 | P1-31 "do not steer the story toward canon. A canon event happens only if play actually reaches it" | 2-1 "작중 날짜 이후의 실제 역사는 … 그 날짜가 되면 … 실제대로 일어난다. {{user}}의 선택이 … 원인을 바꾸면 흐름이 갈라진다" | 날짜에 도달하면 play가 도달한 것이라 같은 방향. 갈라짐 규칙도 같음 |
| W5 | P2-209 "Output only the passage." / P1-103 "without a title, heading or other wrapper unless the requested format … require one" | 8 상태창은 매 응답 필수, 일반 규칙의 예외 | P1-103의 "unless the requested format"과 v5 8의 예외 명시로 정리됨. 테스트에서 상태창 정상 출력 확인 |
| W6 | P2-200 Tags (#Comedy) | 1-1 농담 기본값 아님 | 태그 문구 "More specific writing directions and settings win over a conflicting broad tag"로 v5가 우선 |

---

## 요약

| 구분 | 항목 | 처리 |
|---|---|---|
| 중복 → 프리셋에서 정리 | 존비어 P1-94·95 | 두 줄 → 앵커 + v5에 없는 기능만 남긴 한 줄 |
| 중복 → 프리셋에서 삭제 | D1 P1-45 농담 줄, D2 P1-61 착지 넘기기 금지 줄 | 삭제 |
| 중복이지만 유지 | D3·D4·D5 (같은 줄에 v5에 없는 기능이 있음), D6·P2-205·P2-207·P2-208 (앵커, 출력 직전 자리) | 유지 |
| 충돌 | C1 {{user}} 미세 동작, C2 말 끊김 대시 | C1 앵커 한 문장 추가, C2 구절 삭제 |
| 주의 | W1~W6 | 테스트에서 확인 |
| 묘사 문장 | [Writing the Passage], full expression, 소리, Composition, Prose style, Narrative distance 등 | 손대지 않음 |
