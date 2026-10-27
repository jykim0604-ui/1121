# 테스트용 프리셋 1/2 점검: 확인된 문제 9개를 막는 문장이 있는가 (짝: v5)

- 대조
  - 원본: `preset_toggle_only.md`
  - 테스트판: `test_paste.md` ①·③
  - 짝: `system_prompt_v5_ko.md`
- 문제 9개: `v5_standalone_issues.md` (출력 예시 3 기준)
- 근거로 쓴 출력: `output_samples.md`
  - 예시 1: 테스트판 + v2
  - 예시 2: 원본 + v5
  - 예시 3: v5 단독
- 상태 표기
  - **같음**: 원본 문장이 테스트판에 그대로 있음
  - **약해짐**: 테스트판에서 구절을 지우거나, 반대 방향의 예외를 붙임
  - **보강**: 테스트판에서 원본에 없는 앵커를 더함

---

## 0. 먼저 확인할 것: 테스트판 앵커의 절 번호가 v5와 맞지 않음

테스트판의 앵커는 v1/v2 번호를 가리킨다. v5와 짝지으면 엉뚱한 절을 가리키거나 가리킬 절이 없다.

| 테스트판 앵커 | 개수 | 원래 뜻 (v1/v2) | v5에서 같은 번호 | v5의 해당 절 |
|---|---|---|---|---|
| operator directions (3-1), "the state 3-1 sets", "as 3-1 sets" | 3 | 호칭·존비어 | 없음 (v5 3은 하위 절 없는 설정 처리) | 7-2 |
| operator directions (3-2), "as 3-2 sets" | 7 | 성적 장면 | 없음 | 6-2·6-3 |
| "as 3-3 allows" | 1 | NPC 잡담 | 없음 | 2-1 하위 줄 |
| operator directions (4-2), "as 4-2 sets", (1-0, 4-1, 4-2) | 3 | 출처 없는 표현 억제 / 시뮬레이터, 화면 | 4-2 씬 컨트롤 | 2-6 / 2-1, 2-4 |
| operator directions (4-3) | 1 | 대화 리듬 | 4-3 인지 경계 | 1-1 |
| operator directions (4-5) | 3 | 착지 | 없음 | 9-1 (+2-3, 1-1) |

아래 판정은 앵커가 v5의 해당 절을 가리킨다고 가정한 것이다(번호를 고친 경우).

---

## 문제별 대조

| # | 문제 (예시 3) | v5에서 맡는 절 | 원본 프리셋에서 막는 문장 | 테스트판 | 출력 근거 | 판정 (테스트판 + v5) |
|---|---|---|---|---|---|---|
| 1 | 끝맺음이 매번 {{user}}에게 묻는 형태 | 1-3 버튼, 9-1 | [Ending the Response] "Do not manufacture an ending that hands the turn back: a question … not the default way to stop." / [Before writing] "stop … without a question … aimed at {{user}} unless the scene itself ends there" | 같음. Output range는 재작성되고 4-5 앵커 2개가 붙음 | 예시 1·2·3 모두 질문으로 끝남 | **막는 문장은 있음, 효과는 확인 안 됨.** 세 구성 모두 같은 끝맺음이 나왔다 |
| 2 | 호칭·말투가 설정과 다름 | 7-2 | [Language and Voice] 방향별 존비어 상태, 상속, 원인 없는 전환은 교정. "Unfamiliarity alone does not … require service politeness and -ssi." | **보강**: -ssi 문장 삭제. "address and speech level … set by the operator directions (3-1)", "each direction inherits the state 3-1 sets; an utterance that departs … is the uncaused switch to correct" 추가. [Before writing] 출력 직전에 선배 앵커 | 예시 1을 냈을 때 "존비어는 해결했다"(사용자 확인). 원본을 쓴 예시 2와 프리셋 없이 쓴 예시 3은 무너짐 | **테스트판이 막음** (번호를 7-2로 고쳐야 함) |
| 3 | 대화 전개·화제: 근거 없는 화제, 화제가 튐, 상대가 아는 정보 설명 | 3, 2-1, 1-1 | [Writing the Passage] "Another character is not an interface for exposition … need that speaker's present reason", "Use details the sources support … never invented biography …", "Let a speaker finish a connected thought …; use a rapid rhythm only where … calls for it", "End or reshape an exchange once its work is done". [Characters, Tone and Focus] "The world does not revolve around {{user}}" / ③ Output range 원문 "Complete the first reaction …" | **약해짐**: "use a rapid rhythm only where…" 삭제(A7). "never invented biography"에 "except a character's own small talk, recent news, schedule and minor experiences" 예외 추가(A10). Output range를 "Continue through the reactions the input causes and the development that follows"로 재작성. 나머지 문장은 같음 | 예시 1(테스트판): 손목 → "기타라도 쳤어?" → 폭로 → 손목 반복. 예시 2(원본): 장면에 있는 것에서 대사마다 이어짐 | **테스트판은 부족함.** 원본이 막았던 것을 세 수정이 다시 열었다. 특히 Output range의 "the reactions the input causes"가 입력(고기 굽기)에서 {{user}}의 상태를 지어내는 문으로 쓰였다 |
| 4 | 묘사·표현: 굳은 몸짓, 감정 표지 | 2-6 (수식어만 다룸). 굳은 몸짓을 다루는 문장은 없음 | [Writing the Passage] "Let the scene carry emotion and meaning through what people do, say, avoid and how their bodies respond", "Keep connecting prose plain, speech tags simple, and action beats for actions that matter", "without disguising a volley by inserting gestures". [People, Minds and Bodies] full expression. Composition Description-led, Prose style Literary | 문장은 같음. **보강(앵커)**: Composition 끝 "atmosphere and imagery through the concrete actions…(1-0, 4-1, 4-2)", Prose style 끝 "Motifs and images … (4-2)", [Before writing] 수식어 앵커(4-2) | 예시 1(테스트판): "눈을 반짝이며 … 총총", "얼굴이 붉어진 … 손사래". 예시 2(원본): 감정을 행동 결과로 보여 줌. 예시 3(v5 단독): 예시 1과 같은 계열 | **막는 문장은 같지만 테스트판에서 효과가 없었다.** 앵커를 더한 판(예시 1)과 프리셋이 없는 판(예시 3)에서 같은 굳은 몸짓이 나왔다 |
| 5 | 입력 나레이션 일부가 흐린 요약 | 2-2 나레이션 입력, 1-2 예시 | Composition Description-led "Develop distinct setting, observation, sensation…". full expression. ③ Continuation point "When the input states that something is complete … treat it as already shown and begin with the first new outcome…". [Writing the Passage] "compress connecting material whose work is done" | Continuation point 문장 **삭제**(1-a). 나머지는 같음 | 예시 1: "이러쿵저러쿵 투닥거리며". 예시 2: "2시 30분 … 한 시간 가까이". 예시 3: "한참 동안 말장난" | **프리셋 쪽은 두 판이 거의 같음.** 이 항목의 주인은 v5 2-2다 |
| 6 | 입력에 없는 사실 세부(공항, 시각)가 예시마다 다름 | 2-4 사실 세부 | "Use details the sources support or that follow from established conditions". [Sources and Continuity] "Each fact belongs to its own person, relationship, time, place and condition" | 같음 | 예시 2 김포·2시, 예시 3 인천·1시 30분 | **두 판 같음.** 설정과 기록에 맞는지 확인이 필요함 |
| 7 | {{user}}의 상태를 지어냄 (피곤함, 다크서클) | 2-2 (행동·대사만 명시), 2-1 "{{user}}의 일은 만들지 않는다" | ③ Collaborative RP "you may add only a strongly implied, low-commitment micro-action or an immediate involuntary or sensory reaction of {{user}}'s … lasting emotions … belong to the operator" | 같음 + 1:1 장면 앵커(4-5). **약해짐**: Output range "Continue through the reactions the input causes" | 예시 1: 손목. 예시 2: 없음. 예시 3: 피곤함 | **테스트판은 부족함.** 재작성된 Output range가 입력의 결과를 {{user}}에게 붙이는 쪽으로 열려 있다 |
| 8 | 대화 밖 인물이 멈춰 있음 | 2-4 화면 | [Characters, Tone and Focus] "Other people have their own business, attention and priorities". Viewpoint Omniscient ensemble "several minds and simultaneous processes" | 같음 | 예시 1: 여덟 명 중 둘만 들어옴. 예시 2: 대화 밖 인물도 움직임. 예시 3: 네 명은 한 문장뿐 | **문장은 같으나 테스트판(예시 1)에서 효과가 없었음** |
| 9 | 지문 없는 대사 연속 | 1-1 (짧게 오가는 구간 허용, 몇 차례 뒤 끊음) | [Writing the Passage] "Build the scene's flow and paragraphs first, then decide how much of it is direct speech", "Volleys … are not the default…; use a rapid rhythm only where … calls for it", "without disguising a volley by inserting gestures" | **약해짐**: 빠른 리듬 제한 삭제 + "The quick back-and-forth stretch that the operator directions (4-3) allow is not such a volley." (대사만 잇는 구간을 명시적으로 허용) | 예시 1: 이안–지우 한 줄씩 여섯 번. 예시 2: 다섯 번 이어짐(원본도 완전히 막지는 못함). 예시 3: 네 번 | **테스트판은 부족함.** 원본보다 대사 연속을 더 연다 |

---

## 정리

| 판정 | 문제 |
|---|---|
| 테스트판이 원본보다 잘 막음 | 2 호칭·말투 (번호를 7-2로 고쳐야 함) |
| 두 판이 같음 | 1 끝맺음, 5 나레이션, 6 사실 세부, 8 대화 밖 인물 |
| 테스트판이 원본보다 약함 | 3 대화 전개·화제, 7 {{user}} 상태, 9 대사 연속 |
| 문장은 같지만 테스트판 출력에서 효과가 없었음 | 4 묘사·표현 (테스트판은 앵커를 더한 판), 8 대화 밖 인물 |

- 테스트판을 v5와 짝지으면 9개 중 제대로 막는 것은 2번 하나다. 그것도 앵커 번호를 고쳐야 한다.
- 3, 7, 9번을 약하게 만든 테스트판 수정은 세 가지다.
  - Output range 재작성: "Continue through the reactions the input causes …"
  - A7: 빠른 리듬 제한 삭제
  - A10: 잡담 예외 추가
  - 여기에 (4-3) 짧게 오가는 구간 예외가 더해졌다.
- 4번과 8번은 막는 문장이 두 판에 똑같이 있다. 그런데 원본을 쓴 예시 2에서만 효과가 났다. 테스트판에서 더한 앵커(Composition, Prose style, [Before writing] 수식어 앵커)와 위 세 수정이 함께 들어간 상태에서는 효과가 나지 않았다.
