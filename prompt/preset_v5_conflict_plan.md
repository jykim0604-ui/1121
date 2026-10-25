# 프리셋 수정 방향 (테스트용 프리셋 ↔ 원본 프리셋 비교 기준)

- 비교 대상
  - 원본: `preset_toggle_only.md` (원본 프리셋, 테스트 토글값만 고정)
  - 테스트판: `test_paste.md` ①·③ (일전에 쓰던 테스트용 프리셋)
- 원칙 (사용자 지시)
  - 삭제보다 우선순위와 예외 조항을 추가하는 방향으로 고친다.
  - 테스트판에 이미 반영된 수정이 있으면 그대로 가져온다. 테스트판이 삭제로 처리한 경우도 그 판을 가져온다.
  - 1, 2, 3, 6: 시스템 프롬프트(v5)가 우선이다. 프리셋에 그 사실을 적고, 충돌 지점은 v5 절로 앵커링한다.
  - 4, 5, 7: 양쪽을 모두 반영한다.
  - 8: 보류 (NSFW는 직접 테스트하며 다시 수정).
- 번호: 테스트판의 앵커는 v1/v2 번호를 가리키므로 가져올 때 v5 번호로 바꾼다.

  | 테스트판 | v5 |
  |---|---|
  | 1-0 | 2-1 |
  | 3-1 | 7-2 |
  | 3-2 | 6-2·6-3 |
  | 3-3 | 2-1·5-x |
  | 4-1 | 2-4 |
  | 4-2 | 2-6 |
  | 4-3 | 1-1 |
  | 4-5 | 9-1 (+2-3, 1-1) |

- 상태: 방향만 정리했다. 아직 반영하지 않았다.

---

## 0. 공통: 프리셋에 v5 우선 명시 (신규)

| 위치 | 원본 | 테스트판 | 방향 |
|---|---|---|---|
| ③ [Response controls] 첫머리 | "These are the operator's current settings for your next response…" | 없음. v1/v2 쪽 제목 `[Operator Directions — …]`과 개별 앵커로만 연결했음 | 신규 한 문장. 시스템 프롬프트 `[이 작품의 고정 지시]`가 Charter ②의 operator directions이며, 구조(입력 처리, 대사 블록, 표기, 호칭, 착지)는 아래 응답 설정보다 이 지시가 우선한다. 프리셋 안의 "operator directions (○-○)"는 이 블록의 절 번호를 가리킨다. |

## 1. 입력 처리와 인용 (v5 우선)

| # | 위치 | 원본 | 테스트판 | 방향 | 앵커 |
|---|---|---|---|---|---|
| 1-a | ③ Continuation point | "When the input states that something is complete or gives a result, treat it as already shown and begin with the first new outcome…" | 이 문장 삭제 | **테스트판 차용 (삭제)** | — |
| 1-b | ③ Collaborative RP (micro-action 문단) | 문장 끝에서 "leave that move to the operator." | 끝에 "In a scene with only {{user}} and one NPC, {{user}}'s responses follow the operator directions (4-5)." | **테스트판 차용**, 번호만 바꿈 | 4-5 → 1-1, 2-2, 9-1 |
| 1-c | ③ Input status | 입력의 각 진술을 그대로 확정 | 변경 없음 | **신규 예외 한 문장**: 입력 대사를 어떻게 인용하고 옮기는지는 operator directions를 따른다 | 2-2 |

## 2. 대사 블록과 빠른 주고받기 (v5 우선)

| 위치 | 원본 | 테스트판 | 방향 | 앵커 |
|---|---|---|---|---|
| ① [Writing the Passage] Speech 문단 | "…Volleys of short questions … are not the default …; use a rapid rhythm only where the work or the moment calls for it." | 뒷구절 삭제 + "The quick back-and-forth stretch that the operator directions (4-3) allow is not such a volley." | **테스트판 차용**, 번호만 바꿈 | 4-3 → 1-1 |
| 같은 문단 | 대사 블록 배치(산문 통합형)에 대한 별도 문장 없음 | 없음 | **신규 예외 한 문장**: 대사 블록의 배치와 형식은 operator directions를 따른다 | 1-1, 6-1 |

## 3. 농담·입담의 기본값 (v5 우선)

| 위치 | 원본 | 테스트판 | 방향 | 앵커 |
|---|---|---|---|---|
| ① [Characters, Tone and Focus] | "Teasing, quips, comic reactions and rapid back-and-forth belong to characters and scenes that are actually comic." | "Teasing, quips and comic reactions belong to …" ("rapid back-and-forth" 삭제) | **테스트판 차용** | — |
| 같은 줄 | 받는 방식에 대한 위임 없음 | 없음 | **신규 예외 한 문장**: 후속 발화를 받는 방식(반박, 정정, 놀림, 맞장구, 말꼬리 잡기)은 operator directions를 따르고, 장소나 상황의 기본 어조는 설정이 정한 대로 따른다 | 1-1, 머리말(설정 우선) |
| 외부 | WORLD CARTRIDGE WC-2·WC-4, #Comedy 태그 | — | 이 저장소 밖. 수정하지 않는다 | — |

## 4. 시점·내면 ↔ 카메라 연출 (둘 다 반영)

| 위치 | 원본 (토글 고정판) | 테스트판 | 방향 | 앵커 |
|---|---|---|---|---|
| ③ Viewpoint | Omniscient ensemble (여러 인물의 마음과 동시 진행 허용) | 같음 | 유지 | — |
| ③ Narrator person | "…close third person around the focal character" | 같음 | 유지 + **신규 예외 한 문장**: 이 작품에서 장면은 카메라에 담기는 장면으로 보여 주고, 인물의 속마음은 operator directions가 정한 형식과 빈도로만 드러낸다 | 1-3, 2-4 화면, 5-4 |
| ③ Narrative distance | "Keep interior access sparse…" | 같음 | 유지 (5-4 "드물게"와 같은 방향) | — |

## 5. 문학적 문체 ↔ 수식어 억제 (둘 다 반영: 효과를 단정하는 수식어를 뺀 문학적 산문, 카메라 서술)

| 위치 | 원본 | 테스트판 | 방향 | 앵커 |
|---|---|---|---|---|
| ③ Prose style: Literary | "Viewpoint-shaped diction, varied syntax, subtext, motif and symbolic resonance…; not purple or obscure." | 끝에 "Motifs and images appear only where the sources or the scene ground them, as the operator directions (4-2) set." | **테스트판 차용**, 번호만 바꿈 | 4-2 → 2-6 |
| ③ Composition: Description-led | 원문 분기 | 끝에 "Setting, period and surroundings come in through the objects…, and atmosphere and imagery through the concrete actions, sounds and things that produce them, as the operator directions (1-0, 4-1, 4-2) set." | **테스트판 차용**, 번호만 바꿈 | 1-0, 4-1, 4-2 → 2-1, 2-4, 2-6 |
| ③ [Before writing] | 없음 | "In narration, write the actions, sounds, reactions and concrete people and things … instead of modifiers …; keep only modifiers whose value can be seen or counted, and make the person or thing that acts the subject …, as 4-2 sets." | **테스트판 차용**, 번호만 바꿈 | 4-2 → 2-6 |
| v5 2-6 문체 줄 | — | B2판 "문체 설정(문학적, 라이트 문예 등)과 웹소설 관습은 …" | **신규** (v5 쪽): 문체 줄 앞에 프리셋 문체 설정을 가리키는 구절을 되살린다. 문학적 문체의 함축과 문장 결은 이 항목과 함께 적용된다 | — |

참고 (기록): 표본 4(v5 + 원본 프리셋)에서는 위 세 앵커 없이도 수식어가 다시 나오지 않았다.

## 6. 숫자 표기 (v5 우선)

| 위치 | 원본 | 테스트판 | 방향 |
|---|---|---|---|
| ① [Language and Voice] Numeric notation 문단 | 개수까지 아라비아 숫자(3개) | 문단 삭제 (S2, 시스템 프롬프트 6-1로 넘김) | **테스트판 차용 (삭제)** |

## 7. 분량·멈춤 지점 ↔ 착지 (둘 다 반영)

방향: 새 사건이나 다음 단계가 없어도 지금 순간의 지각, 내면, 상호작용, 문장 결을 깊게 쓴 뒤, 시스템 프롬프트 착지 지침대로 착지한다. 분량("길게")에 관한 부분은 뺀다.

| 위치 | 원본 | 테스트판 | 방향 | 앵커 |
|---|---|---|---|---|
| ③ Output range | "Complete the first reaction that leaves a meaningful choice, then stop … starting the next exchange or carrying out its consequence is a second threshold …" | "Continue through the reactions the input causes and the development that follows, then stop at the point where {{user}}'s next speech, decision or action is needed. … changing location beyond where the input is already heading … An action a character other than {{user}} has already started is carried to its result as the operator directions (4-5) set. The response does not end where the input ends; what follows the input runs as the operator directions (4-5) set." | **테스트판 차용**, 번호만 바꿈 | 4-5 → 9-1 (+2-3) |
| 같은 줄 (추가) | Longform 분기(토글 고정판에는 없음): "Deepen the selected material through distinct interaction, perception, choice, consequence, setting, inner life and sentence texture." | 없음 (G19에서 Standard로 교체) | **신규 한 문장**: Longform의 심화 문장을 분량 말 없이 가져온다. 새 사건이나 다음 단계가 없어도 지금 순간의 지각, 내면, 상호작용, 문장 결을 깊게 쓰고, 착지는 operator directions를 따른다 | 9-1 |
| ③ Response length | Standard | Standard | 유지 (분량 문장은 더하지 않음) | — |
| ① [Pacing and Events] | "A quiet scene may stay quiet." | 삭제 (B1 착지 3 결정: 뜻을 착지로 합침) | **원본 유지** (둘 다 반영: v5 9-1 "조용한 장면은 조용한 채로 둔다. 그래도 … 달라진다"와 같은 방향) | — |
| ① [Characters, Tone and Focus] | "Silence, stillness and restraint are content." | 삭제 (B3 A6 결정: 착지 쪽) | **원본 유지 + 신규 예외 한 문장**: 응답마다의 진전과 착지는 operator directions를 따른다 (둘 다 반영) | 9-1 |

## 8. NSFW (보류)

- 원본 그대로 둔다. 테스트판의 성인 장면 위임(성인 장면 기준, Prose style·표현 관습 boundary, 소리, Scene pacing, 자아 유지 앵커)은 가져오지 않는다.
- 직접 테스트한 뒤 다시 정한다.

---

## 9. 1~8 밖의 테스트판 변경 (구조 관련은 차용)

| 변경 | 테스트판 | 방향 | 앵커 |
|---|---|---|---|
| 존비어 (A8) | [Language and Voice] "Unfamiliarity alone does not override same-age peer usage or require service politeness and -ssi." 삭제 | 차용 (v5 우선, 호칭) | — |
| 존비어 (G15, G27) | 같은 블록에 "In this work, address and speech level between characters are set by the operator directions (3-1)." / "…each direction inherits the state 3-1 sets; an utterance that departs from it … is the uncaused switch to correct…" | 차용, 번호만 바꿈 | 3-1 → 7-2 |
| 선배 (G10, G28) | [Before writing] "Keep the address and speech level each pair already uses … as 3-1 sets; do not call someone 선배 who joined after the speaker, even when they are absent." | 차용, 번호만 바꿈 | 3-1 → 7-2 |
| NPC 잡담 (A10) | [Writing the Passage] "…except a character's own small talk, recent news, schedule and minor experiences as 3-3 allows." | 차용, 번호만 바꿈 | 3-3 → 2-1 |
| 인물 지칭 (A12) | [Sources and Continuity] "…and in a limited viewpoint an unknown person stays described, not named, until learned." 삭제 | 차용 (삭제) | — |
| 번역 병기 (F1) | 출력 언어 "Add no parallel translation or translation notes unless asked." 삭제 | 차용 (삭제, v5 6-1 외국어 줄이 맡음) | — |

## 반영 순서

1. 0 (v5 우선 명시)
2. 1·2·3·6·9 (테스트판 차용과 번호 교체, 신규 예외 문장)
3. 4·5·7 (양쪽 반영. 5의 v5 2-6 구절 포함)
4. §10.1 양방향 검토: 원본 대비 바뀐 문장 목록이 이 표와 일치하는지, 8(NSFW) 문장이 그대로인지 확인
