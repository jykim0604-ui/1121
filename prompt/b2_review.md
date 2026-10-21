# B2 전문 검수 — 수정 필요 목록 (2판)

대상: `preset_b2_merged.md` 본문 (프리셋 원본 활성 분기 + 착지 + 테스트용 울트라라이트)
기준: 가이드 §3(의미 단위), §4(우선순위를 지어내지 않음, 충돌은 표시), §10.1(양방향 대조), §11(실행 본문에 편집용 문구 금지)
상태: 목록만 작성. 수정하지 않음.

## 전제 변경 (사용자 결정)

- 프리셋, 착지, 울트라라이트는 하나의 시스템 프롬프트로 동작한다. 층 구분(운영자 지시 / 프리셋 / 응답 설정)은 두지 않는다.
- 따라서 1판의 A1(착지의 지위)은 없어진다.
- 1판의 B(울트라라이트 머리말의 우선 규정으로 정리된 충돌)는 그 규정에 기대지 않고 본문에서 직접 정리해야 하므로 A로 옮긴다. 현재 결과(울트라라이트 쪽)를 기본값으로 함께 적는다.
- 층을 전제로 쓴 문장들이 새 정리 대상으로 생긴다(S).

판정
- **A. 충돌**: 같은 상황에서 다른 행동을 요구한다. 한쪽을 고르거나 문장을 맞춰야 한다.
- **S. 단일 프롬프트화로 생긴 정리 대상**: 층 구분, 별도 배치, 다른 층에 대한 우선 선언을 전제로 쓴 문장과 중복.
- **C. 구조·기록**

---

## A. 충돌

### 착지 관련

| # | 지침 | 상대 지침 | 충돌 내용 |
|---|---|---|---|
| A1 | 착지 2 "입력 처리는 {{user}}가 한 말과 행동을 옮기면 끝난다" + 울트라라이트 5-1 "인용하지 않은 대사와 행동은 무슨 말을 했고 무엇을 했는지로 옮긴다" | Response controls 이어쓰기 시작점 "When the input states that something is complete or gives a result, treat it as already shown and begin with the first new outcome" | 착지와 5-1은 입력을 본문에 옮기는 것을 전제한다. 프리셋은 완료된 입력은 이미 보여준 것으로 보고 다음부터 쓰라고 한다 |
| A2 | 착지 6 "인물이 시작한 동작은 결과까지 쓴다" | 입력 효력 "an attempt … stays open. Do not … upgrade the second" / 진행 모드 "every story-changing or irreversible result belong to the operator" | "인물"에 {{user}}가 들어가는지 정해져 있지 않다 |
| A3 | 착지 4 "같은 화제 안에서 이야기를 한 칸 옮긴다" | 울트라라이트 4-3 "입력에 적힌 일도 한 번 반영한 뒤에는 그 일이 낳은 반응이나 다음 화제로 넘어간다" / 출력 종점 "starting the next exchange … is a second threshold" | 같은 화제 안 대 다음 화제. "다음 화제"가 새 주고받음을 열면 출력 종점 문턱도 넘는다 |
| A4 | 착지 5 "나머지는 장면에 남아 있다가 다음 응답에서 움직인다" | 울트라라이트 4-1 "주변의 사람과 일은 초점 밖에서도 각자의 일로 계속 움직이며 … 지나가거나 … 소리로 들어온다" | 착지는 다음 응답까지 묶어 두고, 4-1은 같은 응답 안에서 배경으로 움직이게 한다 |
| A5 | 착지 5 | 울트라라이트 4-3 "NPC가 세 명 이상이면 핵심 화자 두 명을 중심으로 두고, 나머지는 끼어들 이유가 생길 때 참여한다" | 같은 일을 두 곳에서 다르게 정한다 ("다음 응답에서" 대 "끼어들 이유가 생길 때") |
| A6 | 착지 3 "응답마다 무언가는 실제로 달라진다" | [Characters, Tone and Focus] "Silence, stillness and restraint are content." 외 3곳([Writing the Passage] "Observation, routine, waiting … without a new goal, conflict, revelation, lasting change", 서술 프로필 "a new conflict, revelation or lasting change is not required", 전개 속도 경계 "It does not require a durable change in every response") | "정적과 멈춤도 내용이다"는 착지와 반대 방향. 나머지 셋은 "지속적 변화 불필요"라 착지의 작은 변화와 양립 가능 |

### 울트라라이트 ↔ 프리셋 (1판 B, 현재 기본값 = 울트라라이트 쪽)

| # | 울트라라이트 | 프리셋 | 울트라라이트 쪽으로 정리하면 |
|---|---|---|---|
| A7 | 4-3 "NPC가 둘 이상 말을 주고받는 대목에는 짧게 오가는 구간을 둔다" | [Writing the Passage] "Volleys of short questions … are not the default" / [Characters, Tone and Focus] "Do not default to banter. … rapid back-and-forth belong to characters and scenes that are actually comic." | 짧게 오가는 구간이 기본 |
| A8 | 3-1 "초면에는 나이와 무관하게 서로 존댓말 … '성을 뗀 이름+씨'가 기본 호칭" | [Language and Voice] "Unfamiliarity alone does not override same-age peer usage or require service politeness and -ssi." | 동갑도 초면이면 존댓말에 이름+씨 |
| A9 | 3-1 "말투 변경은 본문에서 계기를 서술한 뒤 다음 턴부터 적용한다" | [Language and Voice] "A deliberate switch is a speaker-owned event with a cause and consequence, inherited until another caused switch" | 같은 응답 안에서는 말투가 바뀌지 않음 |
| A10 | 3-3 "NPC는 … 자기 잡담, 근황, 일정, 사소한 경험을 만들어 말할 수 있다" | [Writing the Passage] "never invented biography, intimacy, access, private history" | 사소한 경험은 허용. "사소한 경험"과 "지어낸 이력"의 경계는 없음 |
| A11 | 5-2 "원어 뒤에 한국어 해석을 괄호로 붙인다" | Response controls "Add no parallel translation or translation notes unless asked" | 괄호 해석이 붙음 |
| A12 | 5-2 인물 지칭 "지문은 인물을 성을 뗀 이름으로 가리킨다" | [Sources and Continuity] "in a limited viewpoint an unknown person stays described, not named, until learned" | 초점 인물이 모르는 사람도 이름으로 서술될 수 있음 |
| A13 | 3-2 "흥분하거나 절정에 이르러도 자아와 의사표현 능력을 유지" | [People, Minds and Bodies] "an impaired state forms only what it currently can" | 성적 장면의 능력 저하 묘사가 제한됨 |

---

## S. 단일 프롬프트화로 생긴 정리 대상

| # | 위치 | 문장 | 문제 |
|---|---|---|---|
| S1 | 울트라라이트 머리말 | `[Operator Directions — 이 작품의 고정 지시]` / "아래는 이 작품에 대한 운영자의 명시적 지시다. 여기 적힌 항목에 한해 일반 작법 규칙보다 우선하는 이 작품의 구체적 예외로 적용하고, 여기 적히지 않은 것은 프리셋의 규칙과 응답 설정을 따른다." | 별도 층과 "프리셋"이라는 다른 문서를 전제한다. A7~A13을 본문에서 직접 정리하면 이 우선 선언은 할 일이 없어진다 |
| S2 | 울트라라이트 5-2 숫자 표기 | "프리셋의 Numeric notation 대신 이 항목만 따르며" | 같은 프롬프트 안에 [Language and Voice]의 Numeric notation과 울트라라이트 숫자 표기가 둘 다 있다. 한쪽을 지우면 이 문장도 불필요 |
| S3 | 울트라라이트 6 출력 형식 | "'제목이나 머리말 없이 이야기로 시작한다', '상태 표기를 출력에 넣지 않는다'는 일반 규칙의 예외다." | 같은 프롬프트의 [Output]("begins with the story itself, without a title, heading or other wrapper" / "Keep … state labels … out of the deliverable")과 예외 관계를 선언으로 처리하고 있다. 출력 형식 규정이 두 곳([Output], 울트라라이트 6)에 나뉘어 있다 |
| S4 | [Role] | "Story sources come before the conversation; the settings for your next response come after the operator's latest turn." | 응답 설정이 마지막 입력 뒤에 붙는 배치를 전제한다. 하나의 시스템 프롬프트로 넣으면 응답 설정은 대화 앞에 놓이므로 사실과 달라진다 |
| S5 | [Response controls] 첫 줄 | "These are the operator's current settings for your next response. They are not part of {{user}}'s message." | 입력 뒤에 붙는 배치를 전제한 안내. 시스템 프롬프트 안에서는 둘째 문장의 역할이 없다 |
| S6 | Charter Binding authority | "(1) this Charter; (2) explicit current operator directions and corrections; (3) accepted fictional sources, canon, character state, and active response controls; (4) general craft heuristics" | 층 구분을 전제한 순서. 울트라라이트를 (2)로, 프리셋 본문 규칙을 (4)로 읽게 만든다. 대화 중 OOC 정정은 여전히 (2)에 해당하므로 문장 전체가 무의미해지지는 않는다 |
| S7 | [Sources and Continuity] | "The story sources are … the supplementary information and the writer note" / "The writer note directs the current response and is not something the characters know." | 울트라라이트가 작가 노트 자리에 있던 배치를 전제했을 수 있다. 시스템 프롬프트로 옮기면 "writer note"가 무엇을 가리키는지 바뀐다(앱의 작가 노트를 따로 쓰지 않는다면 대상이 없음) |
| S8 | 블록 배열 | 현재: 프리셋 규칙 → `[착지]`(중간) → 울트라라이트 → `---` → Response controls → Before writing | 하나의 프롬프트로서 같은 주제가 흩어져 있다. 예: 끝맺음([Ending the Response], 착지, 울트라라이트 6), 출력 형식([Output], 울트라라이트 6), 말투([Language and Voice], 울트라라이트 3-1·3-3·5-2), 정보 접근([Sources and Continuity], 울트라라이트 2-1). 배열을 바꿀지, 지금 순서를 둘지 결정 필요 (가이드 §4: 구조 변경은 범위 안에서만) |
| S9 | 중복 | 같은 내용이 두 곳에 있는 것: 중·고교 같은 학년 반말([Language and Voice], 울트라라이트 3-1), 말투 방향별 유지([Language and Voice] "Inherit each direction", 울트라라이트 3-1 "이전 턴 호칭과 존비어를 이어 쓴다"), {{user}} 차례 표시 금지([Ending the Response], [Before writing]) | 충돌은 아님. 압축 단계에서 하나로 합칠 후보 |

---

## C. 구조·기록

| # | 위치 | 내용 |
|---|---|---|
| C1 | `[Output]`와 `[Response controls]` 사이 `---` | 붙여 넣을 때 쓴 구분선일 수 있다. [Output]이 `---`를 장면 재개 표시로만 쓰라고 하므로 남으면 오해 여지 |
| C2 | 조건문 제거 흔적 | Charter와 Response controls의 연속 빈 줄. 압축 단계 정리 대상 |
| C3 | 외부 의존 | 울트라라이트 6의 헤드라인은 별도 로어북(`headline_ko.md`). 태그 수정값은 앱 입력란에 넣어야 함 |
| C4 | 1판 C2(울트라라이트의 앱 슬롯 위치) | 하나의 시스템 프롬프트로 쓰기로 해서 해당 없음. 블록 순서 문제는 S8로 옮김 |
