# 프리셋 1/2: 원본과 마지막 테스트판 대조 (묘사 밀도·묘사 지침)

- 원본: `preset_b0.md` 본문
  - 프리셋 1 = `[Mask Creative Writing Charter]`~`[Output]`
  - 프리셋 2 = `[Response controls]`, `[Before writing]`
  - 토글값은 B0 표를 따랐다(서술 시점 설정 준수, 응답 분량 장문, 서술 구성 균형).
- 테스트판: `test_paste.md`의 ① 프리셋 1, ③ 프리셋 2. `preset_b4.md`와 같은 본문이며, 마지막으로 테스트한 판이다.
- 방법: 두 본문을 줄 단위와 문장 단위로 대조했다. 외부 주입 블록을 빼면 바뀐 곳은 23곳이다.
- 범위
  - 묘사 밀도: 얼마나 촘촘하고 길게, 직접적으로 쓰는가.
  - 묘사 지침: 무엇을 어떤 방식으로 묘사하는가.
  - 위 둘에 걸리는 곳은 아래 1·2절에 모두 적었다. 나머지는 3절에 제목만 적었다.
- 외부 주입 서명 블록 두 개(`[External Injection Signatures]`, `[Argon Injection Boundary]`)는 원본에서도 옮기지 않았으므로 대조하지 않았다.

---

## 1. 묘사 밀도: 빠지거나 약해진 것

| # | 위치 (프리셋) | 원본 | 테스트판 | 빠진 것 | 바뀐 이유 (기록) |
|---|---|---|---|---|---|
| D1 | 2 Response length | **Longform.** "Deepen the selected material through distinct interaction, perception, choice, consequence, setting, inner life and sentence texture. Do not break a plainly legible action into routine micro-steps or restate one beat through several channels, and do not add another causal unit, padding, recap or repetition to be long." | **Standard.** "Develop the range with enough distinct action, reaction, context and texture to feel complete, without a fixed quota or explanatory duplication." | ① 상호작용, 지각, 선택, 결과, 배경, 내면, 문장 결을 "깊게" 쓰라는 지시. ② 잘게 쪼개기, 같은 박자 되풀이, 채우기를 막는 문장. Standard는 "완결감이 들 만큼"까지만 요구한다. | G19: 분량 지시가 추론 루프를 만든다고 보고 교체. 원문에도 숫자는 없다. |
| D2 | 2 성인 장면 기준 | "render the defining anatomy, physical action and choreography, localized sensation and bodily change, desire or initiative, **response, rhythm, vocalization** and immediate consequence **with sustained specificity**." | "… desire or initiative and immediate consequence. Characters' speech, vocalization, the pacing of the act and **how density and intensity are carried** follow the operator directions (3-2), and modifiers follow 4-2." | 반응, 리듬, 발성을 묘사 대상으로 둔 것과, "끝까지 구체적으로(sustained specificity)"라는 밀도 기준. 테스트판은 밀도를 시스템 프롬프트 3-2(v5의 6-2·6-3)로 넘겼다. 그런데 그 절은 페이싱, 강도, 발성만 정하고 **밀도 수준은 정하지 않는다.** 결과적으로 성인 장면의 밀도 기준이 사라졌다. | 성인 장면 발성·페이싱 충돌 정리(앵커) |
| D3 | 2 Prose style boundary | "…disciplined form, not less direct detail, **sound density**, emotional force, duration or payoff." | "…not less direct detail, emotional force, duration or payoff." | "절제된 문체라도 소리 밀도를 줄이지 않는다" | 발성을 3-2로 넘기면서 삭제 |
| D4 | 2 Expression register boundary | "…cultural form of established emotion **and adult vocal surface**." / "…not to erasing supported directness, **repeated sound**, emotional force…" | 두 구절 삭제 | 표현 관습이 성인 장면의 발성 표면을 다룬다는 범위, "되풀이되는 소리를 지우지 않는다" | 위와 같음 |
| D5 | 1 [People, Minds and Bodies] full expression | "A caused peak keeps its duration and recovery…, **and no low-to-high curve is assigned in advance.**" | 뒷구절 삭제. 성인 장면 발성·페이싱은 3-2를 따른다고 덧붙임 | 미리 정한 상승 곡선을 금지하는 문장 | 시스템 프롬프트의 기승전결 페이싱과 부딪혀서 삭제(의도적) |
| D6 | 1 [People, Minds and Bodies] sound | 되풀이되는 소리의 반복, 간격, 끊김, 모음 길이, 밀도를 유지하라는 문장 | 문장은 그대로 두고 "성인 장면 발성의 반복과 모음 길이는 3-2를 따른다"를 덧붙임 | 성인 장면에서는 이 문장의 밀도 지시가 3-2로 넘어감. 3-2에는 "소리를 늘이거나 되풀이하는 정도도 이 강도를 따른다"만 있다 | 위와 같음 |

**밀도 문장 중 그대로 남은 것** (두 판에 같은 문장)
- [People, Minds and Bodies] "Once the event is chosen, give it its full expression: duration, density, repetition, volume, directness, imagery, syntax and page space … Literary finish or restraint shapes form; it does not shrink what the scene supports."
- [People, Minds and Bodies] 소리를 출처, 재질, 접촉, 거리, 듣는 위치로 고르라는 문장
- Narrative distance "Observational restraint": "let action, speech, sensory fact and omission carry meaning."
- Prose style boundary 앞부분: 문체는 표현 강도를 낮추지 못한다.

## 2. 묘사 지침: 빠지거나 바뀐 것

| # | 위치 | 원본 | 테스트판 | 내용 | 바뀐 이유 (기록) |
|---|---|---|---|---|---|
| G1 | 2 Composition | **Balanced.** "Let the scene choose the weight of dialogue, action, sensation, atmosphere and inner language. Balance is not an equal share…; keep the one that makes the moment live…" | **Description-led.** 배경, 관찰, 감각, 분위기, 이미지, 내면을 발전시킴 + G22 앵커 "분위기와 이미지는 그것을 만드는 구체적 행동, 소리, 사물로" | 묘사 비중은 오히려 늘었다. 빠진 것은 "장면이 채널 비중을 고른다"는 균형 원칙 | 사용자 토글 변경 (커밋 `1600830`), G22 앵커 |
| G2 | 2 Viewpoint | **Follow the sources.** "Keep the established focal character. If none exists, focus on {{char}}… Author-level directions do not become character knowledge." | **Omniscient ensemble.** 여러 인물의 마음과 동시 진행을 의도적 전환으로 보여 줄 수 있음 | 초점 인물을 고정하는 규칙, "작가 층의 지시는 인물 지식이 아니다" | 사용자 토글 변경 (커밋 `03058d4`) |
| G3 | 1 [Characters, Tone and Focus] | "…a character's own dry or dark humor is still theirs. **Silence, stillness and restraint are content.**" | 마지막 문장 삭제 | **침묵, 정지, 절제도 묘사할 내용이라는 문장.** 시스템 프롬프트 v5에는 이것을 맡는 문장이 없다(9-1 "조용한 장면은 조용한 채로 둔다"는 진전 규칙이라 다름). | 기록 없음 (함께 지운 "A quiet scene may stay quiet."는 시스템 프롬프트 착지로 옮겨짐) |
| G4 | 1 [Sources and Continuity] | "Names and labels from the card are not common knowledge, **and in a limited viewpoint an unknown person stays described, not named, until learned.**" | 뒷구절 삭제 | 모르는 인물은 이름 대신 묘사로 쓴다 | A12 (지칭은 시스템 프롬프트 표기 절로). 전지적 시점으로 바꾼 뒤에는 적용 대상이 거의 없다 |
| G5 | 2 Continuation point | "When the input states that something is complete or gives a result, treat it as already shown and begin with the first new outcome, perception, reaction or consequence." | 삭제 | 끝난 일로 입력된 것은 다시 그리지 않는다 | v5 2-3 "입력한 일이 어떻게 이뤄졌는지 창의적으로 채운다"(초밥 예시)와 정반대라 삭제(의도적) |
| G6 | 2 Prose style | "Literary. …motif and symbolic resonance…; not purple or obscure." | 같은 문장 + "Motifs and images appear only where the sources or the scene ground them, as the operator directions (4-2) set." | 묘사 제한 추가 (빠진 것 아님) | G22 앵커 |
| G7 | 2 [Before writing] | (없음) | 수식어 대신 행동·소리·반응, 보이는 값만, 체온·시선을 주어로 세우지 않기 (4-2) | 묘사 제한 추가 (빠진 것 아님) | 출력 직전 앵커 |

## 3. 묘사와 무관한 차이 (제목만)

- 빠른 주고받기 제한 완화, 코미디 한정 삭제 (A7)
- 지어낸 이력 금지에 잡담 예외 추가 (A10)
- 존비어 상태를 운영자 지시(3-1)에 묶음, -ssi 문장 삭제 (A8 등)
- 숫자 표기 단락 삭제 (S2, 시스템 프롬프트로 옮김)
- 번역 병기 금지 문장 삭제 (F1)
- 출력 종점(Output range) 재작성, 4-5 앵커 추가
- 성인 장면 자아 유지 앵커 (A13)
- {{user}} 1:1 장면 앵커 (4-5)

---

## 4. 같이 확인할 점

**① 테스트판 앵커의 절 번호가 v5와 맞지 않는다.**
- 테스트판 프리셋은 시스템 프롬프트 v1/v2 번호를 가리킨다.
- v5와 함께 쓰면 아래처럼 엉뚱한 절을 가리키게 된다.

| 앵커 | v1/v2에서 가리킨 절 | v5의 해당 절 | v5에서 같은 번호가 가리키는 절 |
|---|---|---|---|
| 3-2 | 성적 장면 | 6-2·6-3 | 3 설정 처리 (3-2는 없음) |
| 4-2 | 출처 없는 표현 억제 | 2-6 | 4-2 씬 컨트롤 |
| 4-5 | 착지 | 9-1 (+2-3) | 없음 |
| 3-1 | 호칭 | 7-2 | 없음 |
| 3-3 | 말투와 반응 | 5-x, 2-1 | 없음 |
| 4-3 | 대화 리듬 | 1-1 | 4-3 인지 경계 |
| 1-0 / 4-1 | 시뮬레이터 / 화면 | 2-1 / 2-4 | 없음 |

**② 원본에 있던 밀도 문장은 v5에 넘어오지 않았다.**
- D1~D4는 테스트판에서 "시스템 프롬프트가 맡는다"며 빼거나 약하게 만든 문장이다.
- 그런데 v5는 처음부터 "문체와 묘사 밀도는 맡지 않는다"로 만들었다.
- 그래서 지금 구성(v5 단독)에서는 D1~D4가 맡던 일을 아무 문장도 맡지 않는다.
