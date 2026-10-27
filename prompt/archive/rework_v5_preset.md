# 재작업: v5 + 프리셋 1/2 충돌 지점 (두 쪽 모두 반영)

이전 작업 내용은 모두 초기화했다. 아래 네 가지만 사실로 두고 다시 작업했다.

## 확정 사실

| # | 사실 | 파일·내용 |
|---|---|---|
| 1 | v5 확정본 | `system_prompt_v5_ko.md`, `system_prompt_v5_en.md` |
| 2 | 출력 예시 2개 | 이전 본문: 테스트용 프리셋 사용, 묘사 비정상. 최근 본문: 원본 프리셋 사용, 묘사가 올바름. 구조는 무너짐(캐릭터성, 존비어, 말투, 대사 형식, 호칭, 착지) |
| 3 | 프리셋 1/2 원본 | 토글값만 확정하고 선택하지 않은 분기는 삭제: `preset_toggle_only.md`. 원문 문장은 그대로다. 고정 토글은 서술 시점 Omniscient ensemble, 서술 구성 Description-led, 응답 분량 Standard, 서술 거리 Observational restraint, 문체 Literary, 출력 종점 Interaction handoff, 성인물 연출 Source-aligned automatic이며, 나머지는 원본 표 그대로다 |
| 4 | 제미나이 피드백 | 충돌 8건 (입력 처리, 대사 블록, 농담 기본값, 시점, 문체, 숫자, 분량·멈춤, 성인 장면) |

사실 3과 4가 어긋나는 곳이 있다. 피드백의 4번(초점 인물)과 7번(Longform)은 다른 토글값의 분기 문장을 근거로 했다. 고정 토글에서는 시점이 Omniscient ensemble, 분량이 Standard이다. 아래 4번과 7번은 고정 토글의 실제 문장을 기준으로 했다.

## 방식

- 한쪽을 지우거나 "한쪽이 우선한다"고 정하지 않는다.
- 두 규칙이 같은 결과를 내도록 풀어 쓴 문장 하나를 둔다. 문장은 한 곳에만 둔다(프리셋 쪽 또는 v5 쪽).
- 프리셋 쪽에 둘 때는 원문 끝에 영어로 덧붙이고, v5를 `the Fixed Directions for This Work (절 번호)`로 가리킨다.
- v5 쪽에 둘 때는 해당 줄 끝에 한국어로 덧붙이고, 영문본에도 같은 문장을 넣는다.
- 출력 예시에서 확인한 두 가지를 피한다.
  - 입력이 낳을 반응을 이어 쓰라는 식의 문장 (이전 본문이 {{user}}의 손목 상태를 지어낸 원인)
  - 빠른 리듬을 기본으로 여는 문장 (이전 본문의 한 줄 말다툼 여섯 번)
- 상태: 문장안이다. v5와 프리셋 파일에는 아직 넣지 않았다.

---

## 1. 입력 처리와 인용

### 1-a. 완료된 입력 ↔ 본문 첫머리의 입력 처리
- 프리셋 (③ Continuation point): "When the input states that something is complete or gives a result, treat it as already shown and begin with the first new outcome, perception, reaction or consequence."
- v5: 2-2 "입력 처리는 본문 맨 앞에 둔다", 2-3 "입력한 일이 구체적으로 어떻게 이뤄졌는지 … 채운다"
- 두 쪽을 함께 쓰면: 입력은 본문 맨 앞에서 한 번 처리한다. 그 처리가 입력을 보여 주는 자리이고, 그 뒤는 첫 새 결과부터 시작한다.
- 위치: 프리셋 ③ Continuation point 끝
- 문장:
  > In this work, the body opens by rendering the input once, including how a completed action was carried out, as the Fixed Directions for This Work (2-2, 2-3) set; that rendering is where the input is shown, and everything after it begins with the first new outcome, perception, reaction or consequence.

### 1-b. {{user}}의 미세 반응 ↔ 입력 행동의 구체적 묘사
- 프리셋 (③ 협업 RP 문단): "For continuity you may add only a strongly implied, low-commitment micro-action or an immediate involuntary or sensory reaction of {{user}}'s …"
- v5: 2-2 머리말 "입력에 적힌 행동을 구체적으로 그리는 것은 그 행동의 반영이며 …", 2-5 노래하는 {{user}}의 몸 묘사
- 두 쪽을 함께 쓰면: 입력된 행동의 세부와 그 행동에 곧바로 따라붙는 작은 반응까지가 반영이고, 그 밖의 {{user}}의 말, 행동, 생각, 결정은 더하지 않는다.
- 위치: v5 2-2 머리말 끝
- 문장 (한):
  > 입력에 적힌 행동에 곧바로 따라붙는 작은 동작이나 무의식적인 반응까지가 반영이다. 그 밖의 {{user}}의 말, 의도한 행동, 생각, 결정은 더하지 않는다.
- 문장 (영):
  > A small action or involuntary reaction that immediately follows an action written in the input is part of reflecting it. Do not add any other speech, deliberate action, thought or decision of {{user}}'s.

### 1-c. 입력 진술의 확정 ↔ 첫 문장만 인용
- 프리셋 (③ Input status): "Follow the input's wording. Keep each statement's assertion and mode …"
- v5: 2-2 "첫 문장을 종결어미까지 원문 그대로 인용", "인용하지 않은 대사와 행동은 무슨 말을 했고 무엇을 했는지로 옮긴다"
- 두 쪽을 함께 쓰면: 진술 하나하나의 단정과 양태는 그대로 지킨다. 형식은 첫 문장만 인용하고 나머지는 요지로 옮긴다.
- 위치: 프리셋 ③ Input status 끝
- 문장:
  > In this work, keeping each statement's assertion and mode does not require quoting the input in full: the first sentence of its dialogue is quoted verbatim and the rest is carried over as what was said and done, as the Fixed Directions for This Work (2-2) set, with every assertion and mode kept.

## 2. 대사 블록 ↔ 산문 흐름·빠른 주고받기
- 프리셋 (① [Writing the Passage]): "Let a speaker finish a connected thought instead of splitting it into prompted one-line answers. Volleys of short questions … are not the default …; use a rapid rhythm only where the work or the moment calls for it."
- v5: 1-1 대사 블록 분리, 짧게 오가는 구간("둘 수 있다")
- 두 쪽을 함께 쓰면: 대사는 화자 블록으로 따로 두되, 블록 하나에 그 화자의 이어진 생각을 끝까지 담는다. 흐름은 블록 앞뒤 지문이 잇는다. 짧게 오가는 구간은 장면이 빠른 리듬을 부를 때만 두는 선택이다.
- 위치: v5 1-1 「짧게 오가는 구간」 줄 끝
- 문장 (한):
  > 이 구간은 장면이 빠른 리듬을 부를 때 두는 선택이며 기본값이 아니다. 그 밖의 대사는 블록 하나에 그 화자의 이어진 생각을 끝까지 담고, 흐름은 블록 앞뒤의 지문이 잇는다.
- 문장 (영):
  > This stretch is an option for when the scene calls for a rapid rhythm, not the default. Elsewhere, each block carries the speaker's connected thought through to its end, and the prose before and after the blocks carries the flow.

## 3. 농담·입담의 기본값
- 프리셋 (① [Characters, Tone and Focus]): "Do not default to banter. Teasing, quips, comic reactions and rapid back-and-forth belong to characters and scenes that are actually comic."
- v5: 1-1 "받는 방식(반박, 정정, 놀림, 맞장구, 말꼬리 잡기)과 그 말투는 화자의 성격과 상대와의 관계가 정한다. … 놀림은 그런 관계에서만 나온다." 머리말 "설정 … 을 가장 먼저 따른다". 외부 설정(월드 카트리지 WC-2·WC-4)에는 무대 밖 대화의 가벼운 기본 리듬이 있다.
- 두 쪽을 함께 쓰면: 농담은 기본값이 아니다. 설정이 가볍게 오가는 자리로 정한 곳은 프리셋이 말하는 "actually comic"한 장면이다.
- 위치: v5 1-1 후속 발화 줄 끝
- 문장 (한):
  > 농담과 놀림은 기본값이 아니라 그런 성격과 관계, 그런 자리에서 나온다. 설정이 가볍게 오가는 자리로 정한 곳에서는 그 가벼운 말투가 그 장면의 원래 어조다.
- 문장 (영):
  > Jokes and teasing are not the default; they come from that kind of personality, relationship and setting. Where the settings establish a place as one of light back-and-forth, that lightness is the scene's own tone.

## 4. 시점·내면 ↔ 카메라 연출·속마음
- 프리셋 (고정 토글): Viewpoint "Omniscient ensemble. The narrator may reveal several minds…", Narrative distance "Keep interior access sparse and let action, speech, sensory fact and omission carry meaning.", Narrator person "…close third person around the focal character" (소스에 인칭이 없을 때)
- v5: 1-3 카메라·편집 연출, 2-4 화면, 5-4 "NPC의 속마음은 … ' ' 안에 … 드물게"
- 두 쪽을 함께 쓰면: 시점은 여러 인물의 속을 오갈 수 있다. 내면은 주로 동작, 말, 감각, 생략으로 전하고, ' ' 속마음은 드물게 쓴다. 카메라는 그 인물들이 있는 장면 전체를 담는다.
- 위치: v5 5-4 속마음 줄 끝
- 문장 (한):
  > 시점이 여러 인물의 속을 오갈 수 있어도, 속은 주로 동작과 말, 그 자리의 감각과 생략으로 전하고 ' ' 속마음은 드물게 쓴다. 장면은 그 인물들이 있는 자리 전체를 카메라에 담는 방식으로 보여 준다.
- 문장 (영):
  > Even though the viewpoint may move between several minds, the inner life is carried mainly by action, speech, sensory fact and omission, and ' ' thoughts stay rare. The scene is shown as the camera takes in the whole place those characters are in.

## 5. 문학적 문체 ↔ 출처 없는 표현 억제
- 프리셋 (③ Prose style: Literary): "Viewpoint-shaped diction, varied syntax, subtext, motif and symbolic resonance, while the chosen action and consequence stay legible; not purple or obscure."
- v5: 2-6 (v2 원문). 효과에 이름만 붙이는 수식어, 상황을 요약하는 추상명사, 출처 없는 비유를 쓰지 않는다. 이미지와 모티프는 근거가 있을 때만 쓴다.
- 두 쪽을 함께 쓰면: 문학적 문체는 어휘, 통사, 함축으로 내고, 상징적 울림은 근거 있는 사물과 행동이 되풀이되며 쌓이게 한다. 효과를 단정하는 수식어로 내지 않는다. 최근 본문에서 설정의 선물들이 장면 속 사물로 되풀이된 방식이 이것이다.
- 위치: 프리셋 ③ Prose style 끝 (2-6은 v2 원문 그대로 둔다)
- 문장:
  > In this work, subtext, motif and symbolic resonance come from diction, syntax and grounded objects and actions that recur in the scene, not from modifiers that name an effect or from unsourced figures, as the Fixed Directions for This Work (2-6) set; the camera shows what produces the effect.

## 6. 숫자 표기
- 프리셋 (① [Language and Voice] Numeric notation): "When presenting a numeric value as information, use Arabic digits (0-9) for resources, statistics, levels, counts, prices … In Korean, write forms such as 마나 81, 레벨 7, 3개 and 12.5% …"
- v5: 6-1 명시적인 수치 정보는 아라비아 숫자, "위 수치 정보가 아닌 작은 수 중 고유어로 읽는 수는 아홉까지 한글(세 번, 두 명)"
- 두 쪽을 함께 쓰면: 정보로 제시하는 수(자원, 통계, 레벨, 셈한 개수, 가격 등)는 아라비아 숫자로 쓴다. 이 점은 두 쪽이 같다. 정보로 제시하지 않는 일상 서술과 대사 속 작은 고유어 수는 한글로 쓴다.
- 위치: 프리셋 ① Numeric notation 끝
- 문장:
  > Small numbers in ordinary narration and speech that are not presented as information, and that are read with native Korean numerals, are written in Korean words (세 번, 두 명, 한 시간) as the Fixed Directions for This Work (6-1) set; counts presented as information keep Arabic digits.

## 7. 멈춤 지점 ↔ 착지
- 프리셋 (고정 토글): Output range "Interaction handoff. Complete the first reaction that leaves a meaningful choice, then stop before new input is needed. Do not cross a second information or action threshold: opening something closed, revealing a clue, changing location, starting the next exchange or carrying out its consequence …". 응답 분량은 Standard라 Longform 문장은 없다.
- v5: 2-3 "같은 순간을 … 잘게 늘리지 않는다", 9-1 박자(자극 → 주고받음 → 다음 움직임의 시작), 진행 중인 자리에서 착지, 정체 방지
- 두 쪽을 함께 쓰면: 프리셋이 말하는 "첫 반응"은 9-1의 박자 하나다. 새 사건이나 다음 단계를 더하지 않고, 그 박자 안의 상호작용, 지각, 내면, 문장 결을 깊게 쓴다. 다음 움직임이 시작돼 진행 중인 자리에서 끊는다. 박자 안에서 위치, 정보, 관계, 상황이 한 걸음 나아가는 것은 두 번째 문턱이 아니다.
- 위치: 프리셋 ③ Output range 끝
- 문장:
  > In this work, the first reaction is the one beat the Fixed Directions for This Work (9-1) describe: the characters present exchange over the stimulus and their next movement begins, and the response stops while that movement is in progress. Deepen that beat through its interaction, perception, inner life and sentence texture instead of adding a new event or a further stage; the small advance in position, information, relationship or situation that happens within the beat is not a second threshold.

## 8. 성인 장면의 직접성 ↔ 단계·수식어·수치
- 프리셋 (③ 성인 장면 기준): "… substantial direct physical and sensory explicitness is the default reader contract: render the defining anatomy, physical action and choreography, localized sensation and bodily change, desire or initiative, response, rhythm, vocalization and immediate consequence with sustained specificity."
- v5: 6-2 단계는 이어서 넘어가고 한 응답에 몰아 쓰지 않음, 수치를 기계적으로 늘어놓지 않음, 굳은 표현 금지, "강도는 수식어가 아니라 접촉, 동작, 속도 같은 구체적 사실로". 2-6 수식어 억제
- 두 쪽을 함께 쓰면: 직접성과 구체성은 그대로 두고, 그것을 접촉, 동작, 속도, 몸의 반응 같은 구체적 사실로 전한다. 단계는 하나씩 진행하되, 각 단계는 끝까지 구체적으로 쓴다.
- 위치: 프리셋 ③ 성인 장면 기준 문단 끝
- 문장:
  > In this work, that explicitness is carried by concrete contact, movement, pace and bodily response rather than by modifiers or listed figures, and the scene moves one stage at a time as the Fixed Directions for This Work (6-2) set; each stage is rendered with that full specificity.
- 외부: 피드백이 근거로 든 Patch Note는 이 저장소 밖에 있다.

---

## 넣을 자리 요약

| 쪽 | 항목 | 넣을 곳 |
|---|---|---|
| 프리셋 ① | 6 | Numeric notation |
| 프리셋 ③ | 1-a, 1-c, 5, 7, 8 | Continuation point, Input status, Prose style, Output range, 성인 장면 기준 |
| v5 (한·영) | 1-b, 2, 3, 4 | 2-2 머리말, 1-1 짧게 오가는 구간, 1-1 후속 발화, 5-4 속마음 |

- 프리셋은 원문 문장을 하나도 지우거나 바꾸지 않는다. 문단 끝에 한 문장씩만 더한다(6곳).
- v5는 기존 문장을 바꾸지 않는다. 줄 끝에 한 문장씩만 더한다(4곳). 2-6은 v2 원문 그대로 둔다.
