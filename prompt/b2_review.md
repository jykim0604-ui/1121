# B2 전문 검수 — 수정 필요 목록

대상: `preset_b2_merged.md` 본문 (프리셋 원본 활성 분기 + 착지 + 테스트용 울트라라이트)
기준: 가이드 §3(의미 단위), §4(우선순위를 지어내지 않음, 충돌은 남겨 두고 표시), §10.1(양방향 대조), §11(실행 본문에 편집용 문구 금지)
상태: 목록만 작성. 수정하지 않음.

판정 기준
- **A. 결정 필요**: 같은 상황에서 서로 다른 행동을 요구하는데, 본문 어디에도 우선순위가 없다.
- **B. 의도 확인**: 충돌하지만 울트라라이트 머리말("여기 적힌 항목에 한해 일반 작법 규칙보다 우선")과 Charter 권한 순서(운영자 지시가 2순위)로 이미 울트라라이트가 이긴다. 그 결과가 의도한 것인지만 확인하면 된다.
- **C. 구조·기록**: 문구 충돌이 아닌 위치, 형식, 외부 의존.

---

## A. 결정 필요

| # | 지침 | 상대 지침 | 충돌 내용 |
|---|---|---|---|
| A1 | `[착지]`라는 블록 자체의 위치 | 울트라라이트 머리말, Charter 권한 순서 | 착지는 프리셋 블록 사이(`[Ending the Response]` 뒤)에 있어서 "운영자 지시"(2순위)인지 "일반 작법"(4순위)인지 정해져 있지 않다. 이게 정해져야 A3~A5에서 울트라라이트와 착지 중 어느 쪽이 이기는지가 정해진다 |
| A2 | 착지 2 "입력 처리는 {{user}}가 한 말과 행동을 옮기면 끝난다" + 울트라라이트 5-1 "{{user}} 블록 … 인용하지 않은 대사와 행동은 무슨 말을 했고 무엇을 했는지로 옮긴다" | Response controls 이어쓰기 시작점 "When the input states that something is complete or gives a result, treat it as already shown and begin with the first new outcome" | 착지와 5-1은 입력을 본문에 옮기는 것을 전제한다. 프리셋은 완료된 입력은 이미 보여준 것으로 보고 다음부터 쓰라고 한다 |
| A3 | 착지 6 "인물이 시작한 동작은 결과까지 쓴다" | Response controls 입력 효력 "an attempt … stays open. Do not … upgrade the second" / 진행 모드 "every story-changing or irreversible result belong to the operator" | "인물"에 {{user}}가 들어가는지 정해져 있지 않다. 들어가면 {{user}}의 시도를 결과까지 쓰게 되어 프리셋과 충돌한다. 줄 끝 "{{user}}의 선택에 달려 있으면 멈춘다"가 일부만 막는다 |
| A4 | 착지 4 "같은 화제 안에서 이야기를 한 칸 옮긴다" | 울트라라이트 4-3 "입력에 적힌 일도 한 번 반영한 뒤에는 그 일이 낳은 반응이나 다음 화제로 넘어간다" / 출력 종점 "starting the next exchange … is a second threshold" | 착지는 같은 화제 안, 4-3은 다음 화제로. 4-3의 "다음 화제"가 새 주고받음을 열면 출력 종점의 두 번째 문턱도 넘는다 |
| A5 | 착지 5 "나머지는 장면에 남아 있다가 다음 응답에서 움직인다" | 울트라라이트 4-1 "주변의 사람과 일은 초점 밖에서도 각자의 일로 계속 움직이며 … 말과 행동 사이로 지나가거나 … 소리로 들어온다" | 착지는 중심이 아닌 인물을 다음 응답까지 묶어 두고, 4-1은 같은 응답 안에서 배경으로 움직이게 한다 |
| A6 | 착지 5 | 울트라라이트 4-3 "NPC가 세 명 이상이면 핵심 화자 두 명을 중심으로 두고, 나머지는 끼어들 이유가 생길 때 참여한다" | 같은 일을 두 곳에서 다른 말로 정한다. 착지는 "다음 응답에서", 4-3은 "끼어들 이유가 생길 때" |
| A7 | 착지 3 "응답마다 무언가는 실제로 달라진다" | 프리셋에 남은 비슷한 문장 4곳: [Characters, Tone and Focus] "Silence, stillness and restraint are content." / [Writing the Passage] "Observation, routine, waiting or unresolved pressure can carry a passage without a new goal, conflict, revelation, lasting change or tidy conclusion." / 서술 프로필 "a new conflict, revelation or lasting change is not required" / 전개 속도 경계 "It does not require a durable change in every response" | 앞서 "A quiet scene may stay quiet."만 착지 쪽으로 정리했다. 같은 성격의 문장이 네 곳 더 남아 있다. "지속적 변화(lasting/durable)"는 착지의 "작은 변화"와 양립할 수 있지만, "정적과 멈춤도 내용이다"는 착지와 반대 방향이다 |

---

## B. 의도 확인 (울트라라이트 우선으로 이미 정리됨)

| # | 울트라라이트 | 프리셋 | 지금 적용되는 결과 |
|---|---|---|---|
| B1 | 4-3 "NPC가 둘 이상 말을 주고받는 대목에는 짧게 오가는 구간을 둔다" | [Writing the Passage] "Volleys of short questions … are not the default way to sustain a scene" / [Characters, Tone and Focus] "Do not default to banter. … rapid back-and-forth belong to characters and scenes that are actually comic." | 짧게 오가는 구간이 기본이 된다. 태그 #Comedy가 있어 프리셋 쪽 예외에도 걸친다 |
| B2 | 3-1 "초면에는 나이와 무관하게 서로 존댓말을 쓰고 … '성을 뗀 이름+씨'가 기본 호칭" | [Language and Voice] "Unfamiliarity alone does not override same-age peer usage or require service politeness and -ssi." | 초면이면 동갑이어도 존댓말과 "이름+씨"가 기본이 된다(중·고교 같은 학년 예외는 양쪽 모두 있음) |
| B3 | 3-1 "말투 변경은 본문에서 계기를 서술한 뒤 다음 턴부터 적용한다" | [Language and Voice] "A deliberate switch is a speaker-owned event with a cause and consequence, inherited until another caused switch" | 같은 응답 안에서 계기와 함께 말투가 바뀌는 것이 막힌다 |
| B4 | 3-3 "NPC는 … 자기 잡담, 근황, 일정, 사소한 경험을 만들어 말할 수 있다" | [Writing the Passage] "never invented biography, intimacy, access, private history" | NPC가 사소한 경험을 지어내는 것이 허용된다. 어디까지가 "사소한 경험"이고 어디부터 "지어낸 이력"인지는 경계가 없다 |
| B5 | 5-2 "원어 뒤에 한국어 해석을 괄호로 붙인다" | Response controls "Add no parallel translation or translation notes unless asked" | 운영자 지시가 곧 요청이므로 괄호 해석이 붙는다 |
| B6 | 5-2 인물 지칭 "지문은 인물을 성을 뗀 이름으로 가리킨다" | [Sources and Continuity] "in a limited viewpoint an unknown person stays described, not named, until learned" | 초점 인물이 이름을 모르는 사람도 이름으로 서술될 수 있다 |
| B7 | 3-2 "흥분하거나 절정에 이르러도 자아와 의사표현 능력을 유지" | [People, Minds and Bodies] "an impaired state forms only what it currently can" | 성적 장면에서는 능력 저하 묘사가 제한된다 |

이미 문구로 명시해 정리된 것 (수정 불요)
- 5-2 숫자 표기: "프리셋의 Numeric notation 대신 이 항목만 따르며"
- 6 출력 형식: "'제목이나 머리말 없이 이야기로 시작한다', '상태 표기를 출력에 넣지 않는다'는 일반 규칙의 예외다" ([Output]와의 관계)

---

## C. 구조·기록

| # | 위치 | 내용 |
|---|---|---|
| C1 | `[Output]`와 `[Response controls]` 사이 `---` | 원문에 있던 줄이라 남겼다. 붙여 넣을 때 쓴 구분선일 수 있다. 프리셋의 [Output]은 `---`를 시간·장소가 바뀐 재개 지점에만 쓰라고 하므로, 실행 본문에 남으면 그 규칙의 예처럼 읽힐 여지가 있다 |
| C2 | 울트라라이트 위치 | `[Response controls]` 앞으로 추정했다. 실제 앱에서 울트라라이트가 들어가는 슬롯과 순서는 확인하지 않았다 |
| C3 | 조건문 제거 흔적 | Charter와 Response controls에 연속 빈 줄이 남아 있다. 의미 문제는 아니며 압축 단계에서 정리 대상 |
| C4 | 외부 의존 | 울트라라이트 6의 "헤드라인(출력 조건을 충족할 때)"은 별도 로어북(`headline_ko.md`)에 달려 있다. 태그 수정값은 앱의 입력란에 넣어야 하며 파일 본문에는 매크로만 있다 |
