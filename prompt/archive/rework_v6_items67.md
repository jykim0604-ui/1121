# v6 / 프리셋 v6: 6·7번 수정 방향

- 상태: 방향과 문장안만 정리했다. `preset_v6.md`에는 아직 넣지 않았다.
- 8번(성인 장면)은 전면 보류. NSFW 장면을 테스트한 뒤 확정한다.

---

## 6. 숫자 표기: 시스템 프롬프트 우선, 프리셋 문단 삭제

- 방향: 프리셋 ① [Language and Voice]의 `Numeric notation` 문단 전체를 지운다. 숫자 표기는 v6 6-1만 따른다.
- 삭제해도 되는지 확인하려고, 문단의 문장 6개를 v6 6-1과 하나씩 대조했다.

| # | 프리셋 문장 | v6에서 맡는 문장 | 묘사 관련 |
|---|---|---|---|
| 1 | "When presenting a numeric value as information, use Arabic digits (0-9) for resources, statistics, levels, counts, prices, percentages, dates, times and measured quantities." | 6-1 "측정값, 금액, 비율, 통계, 레벨, 날짜와 시각, 나이, 주소, 코드, 모델 번호, 큰 수량처럼 명시적인 수치 정보는 아라비아 숫자로 쓴다". 개수(counts)는 6-1 "아홉까지 고유어 수는 한글"이 정한다 (사용자 결정: 시스템 프롬프트 우선) | 없음 (표기) |
| 2 | "In Korean, write forms such as 마나 81, 레벨 7, 3개 and 12.5%; do not expand the value 81 into 여든하나 or 팔십일." | 6-1 예시 "(300킬로그램, 35000원, 404호, 150명)", "(12명, 16팀)", "(3번 X → 세 번 …)" | 없음 (표기) |
| 3 | "Apply this notation in narration, first-person inner language, ordinary dialogue and status text regardless of prose style or expression register." | 6-1 "문체나 표현 관습 설정과 관계없이 지문, 대사, 속마음, 상태창에 똑같이 적용한다" | 없음 |
| 4 | "Preserve the value, unit, sign, decimal precision, range and any approximate qualifier." | 6-1 "표기를 바꿔도 값은 그대로 옮긴다. 단위, 부호, 소수점 자릿수, 범위, 어림 표시를 지킨다" | 없음 |
| 5 | "Keep vague or idiomatic wording such as 수십, 한두 and 한번 해보자, proper names, source-required verbatim quotations and wording about pronunciation itself intact." | 6-1 "어림말(수십, 한두, 몇백만)은 숫자로 바꾸지 않는다", "관용 표현은 한글로 쓴다", "고유명사 속 숫자, 원문 그대로 옮기는 인용, 발음 자체를 말하는 표현은 그대로 둔다" | 없음 |
| 6 | "This governs the typography of a quantity already selected for expression; it cannot add precision, numeracy, knowledge, measurement, calculation or exposition, or make writer-only metadata available to a character." | 6-1 "이 항목은 이미 쓰기로 한 수의 표기만 정한다. 표기를 위해 없던 수치, 정밀도, 계산, 설명을 만들지 않는다. 수를 적었다고 인물이 그 수를 알거나 셈하게 되지는 않는다." / 8-2 "여기 적혔다는 사실이 인물의 인지 근거가 되지 않는다" | **유일하게 묘사와 닿는 문장.** 묘사를 늘리려고 치수나 수치를 덧붙이지 않게 막는 문장이다. v6 6-1이 같은 기능을 맡는다 ("measurement"는 6-1의 "없던 수치"에 든다) |

- 문단 밖 확인 1: 프리셋의 다른 묘사 문장(full expression, Description-led, Literary, 표현 관습)은 숫자 표기를 가리키지 않는다. 지워도 끊기는 참조가 없다.
- 문단 밖 확인 2: Expression register boundary의 "The register shapes … typography"가 숫자 표기까지 바꿀 여지는 v6 6-1 "문체나 표현 관습 설정과 관계없이"가 막는다.
- 결론: 문단을 지워도 묘사 기능이 줄지 않는다. 문장 6의 기능은 v6 6-1이 그대로 맡는다.

---

## 7. 멈춤 지점 (Output range) ↔ 착지: 문구 재작성

### 참고한 두 본문

| 본문 | 확인한 것 | 문구에 반영한 것 |
|---|---|---|
| 올바른 예시 2번 (최근 본문) | 대화가 그 자리에 있는 것에서 이어진다: 들어오는 순서, 반말, 백참, 기사, 가이드 음원. 대사마다 앞 대사를 받는다. 다만 끝은 하람이 {{user}}에게 "누구부터 먼저 들어가면 될까요?"라고 묻고 기다리는 자리다(착지 무너짐) | ① 박자는 장면에 이미 있는 것으로 짓는다. ② 다른 인물은 {{user}}의 대답을 기다리며 서 있지 않는다 |
| '데이트인가?' 예시 | 입력: 운전, 대화, 내려 줌, 엘리베이터 혼잣말. 자율 전개 턴. 압축 전 단독 프롬프트는 입력을 옮긴 뒤 지연이 숙소에 들어서고, 숙소 인물(연희)과 그 자리의 일로 이어 갔다. 테스트 당시 문제는 입력만 늘여 옮기고 혼잣말에서 끝난 것이었다 (b2_review G24·G25) | ③ 입력이 끝나는 자리는 응답이 끝나는 자리가 아니다. ④ 입력이 이미 향하던 곳(숙소)의 장소와 인물이 장면을 잇는다. 그곳으로 옮겨 가는 것은 두 번째 문턱이 아니다 |
| (참고) 이전 본문 | 입력(이틀 동안 고기를 구움)에서 {{user}}의 손목 상태를 지어내고 대화가 그것을 쫓아감 | ⑤ {{user}}에게 생긴 결과를 지어내지 않는다 ("입력이 낳은 반응을 이어 쓴다"는 표현은 쓰지 않음) |

### 두 쪽 문장
- 프리셋 (③ Output range, 원문 그대로 둠): "Interaction handoff. Complete the first reaction that leaves a meaningful choice, then stop before new input is needed. Do not cross a second information or action threshold: opening something closed, revealing a clue, changing location, starting the next exchange or carrying out its consequence is a second threshold unless that threshold itself was the operator's explicit immediate request. …"
- v6: 2-3 "입력 처리는 … 끝난다. 새로 생긴 일이 적어도 입력 처리로 본문을 닫지 않는다", 4-2 자율 전개 턴, 9-1 박자·진행 중 착지·정체 방지·"{{user}}가 답하지 않아도 인물은 다음 동작으로 넘어간다"
- 두 쪽을 함께 쓰는 방법
  - 원문의 "first reaction"을 9-1의 박자 하나로 읽는다.
  - 원문의 "두 번째 문턱"은 박자 밖의 새 사건과 다음 단계로 둔다.
  - 원문의 "new input is needed"는 다음 걸음이 {{user}} 자신의 결정에 달려 있을 때로 둔다.
  - 그 결과, 박자 안의 주고받음, 입력이 향하던 곳으로의 이동, 작은 진전은 문턱이 아니게 된다.
- 분량("길게")에 관한 말은 넣지 않는다.

### 문장안 (③ Output range 끝에 덧붙임)

> In this work, the response does not stop where the input stops. After the input is rendered, the characters present carry the scene through one beat as the Fixed Directions for This Work ([이 작품의 고정 지시]) (9-1) set; when the input ends with someone already on the way somewhere, the place and people they are heading to carry it on. Build that beat from what the scene already holds: what was just said, the objects, distance and people present, and what each character has directly experienced; deepen its interaction, perception, inner life and sentence texture instead of inventing a new event or a consequence for {{user}}. Moving on to where the input is already heading, the next exchange among the characters present, and the small advance in position, information, relationship or situation within the beat are not second thresholds. New input is needed only when the next step depends on {{user}}'s own decision; the other characters do not stand waiting for it, and the response stops while their own next movement is in progress.

### 문장안 대조

| 문장안 구절 | 근거 |
|---|---|
| the response does not stop where the input stops | '데이트인가?' (혼잣말에서 끝난 문제), v6 2-3 |
| the place and people they are heading to carry it on | '데이트인가?' (숙소, 연희) |
| Build that beat from what the scene already holds | 예시 2번 (대화가 그 자리에 있는 것에서 이어짐) |
| instead of inventing a new event or a consequence for {{user}} | 이전 본문 (손목), 원문 두 번째 문턱 |
| deepen its interaction, perception, inner life and sentence texture | 사용자 방향 (분량 말 없이 지금 순간을 깊게) |
| … are not second thresholds | 원문 문턱 목록(changing location, starting the next exchange)의 범위를 9-1 박자 밖으로 한정 |
| the other characters do not stand waiting for it, and the response stops while their own next movement is in progress | 예시 2번의 무너진 착지(질문하고 기다림), v6 9-1 |
