# 리수폿 관계·말투 판단 규칙 — 8-2 정렬 변경 내역

- 원문: `risupot_speech_original.md`
- 수정본: `risupot_speech_revised.md`
- 손대지 않은 범위: 제목, 첫 문단, `Read each direction separately` 문단, 관계별 호칭 예시표 중 배우자·연인·친척·사제·초면 행, `## Conditions for transition`부터 끝까지 전부 (원문과 바이트 단위 동일 확인)

## 변경 내역

| # | 원문 | 수정 / 삭제 | 이유 (8-2 기준) |
|---|---|---|---|
| 1 | Treat each target-specific speech record as slow-changing canon. | Treat each target-specific speech record as the address and speech register the pair is already using. | 요구 5. 저장 기록 = 8-2 "이전 턴에 쓴 호칭과 존비어" |
| 2 | An explicit accepted agreement or confirmed relationship/status transition may change it immediately; otherwise require consistent changed use across at least two distinct scenes. | Update it only when the conversation log narrates a catalyst under Conditions for transition; the new value applies from the next turn. | 요구 2. 8-2 "말투 변경은 본문에서 계기를 서술한 뒤 다음 턴부터 적용". 즉시 변경과 장면 2개 조건 삭제. 계기 목록은 Conditions for transition 문단을 참조해 중복 방지 |
| 3 | If durability is uncertain, preserve the existing record … | Otherwise, preserve the existing record … | 장면 2개 조건이 없어져 "지속성 판단"이 필요 없어짐 |
| 4 | … then a provisional judgment grounded in relationship, status, age, and intimacy. | … then an initial judgment by the criteria below. | 8-2 "처음 말하는 쌍만 아래 기준으로 계산" |
| 5 | When usage is mixed, look for an actual transition catalyst; without one, prioritize the earliest consistently established pattern and repeated use. | When records conflict, the most recent record is the current value; treat older records as the value at their time. | 요구 1. 8-2 "오래된 쪽은 그 시점의 값, 가장 최근 기록을 현재 값" |
| 6 | 판정 축 표 4행 (Relationship type / Status difference / Age and seniority — "Never infer an unknown age and assert it as fact" / Degree of intimacy) | 2행으로 교체: Seniority(먼저 들어온 쪽이 선배, 나이 무관) / Age(형·누나·오빠·언니는 나이로만, 연하가 연상에게 사용). 도입문에 "seniority and age separately" | 요구 3. 8-2 선후배 정의, 두 축 분리, 관계 호칭. 나이 단정 금지 문장은 요구 4(추정 저장)와 충돌해 삭제 |
| 7 | (없음) | 불릿 6개 추가: 공적 상황 / 사적 상황 / 동갑·연인 / {{user}} / 판정 근거·추정 / 저장 대상 | 요구 3·4. 8-2 해당 줄을 판정·저장 문맥으로 옮김 (새 규칙 없음) |
| 8 | Strangers of the same age do not automatically use informal speech, and workplace hierarchy may apply differently in a private meeting. | 삭제 | 불릿의 "동갑 초면 존댓말", "사적 상황 나이 우선"과 중복 |
| 9 | Colleagues: A name or title matching the actual environment and agreement. Conditions may differ outside the workplace | Colleagues: A title by rank and seniority at work; outside work, age decides | 8-2 공적=직급·선후배 우선, 사적=나이 우선 |
| 10 | When age and organizational seniority conflict, … may avoid the problem with a title or safe form of address. Never use these conventions as mandatory rules … | 문단 삭제 | 요구 3. 회피 문장 삭제, 공적/사적 우선순위로 판정. "관례를 의무로 쓰지 않는다"는 8-2 규칙이 의무라 충돌 |
| 11 | Distinguish status differences that apply everywhere, only within a particular institution, or are temporarily suspended in the current situation. | 삭제 | 8-2는 공적 상황이면 항상 직급·선후배 우선. "일시 정지" 개념 없음 |
| 12 | Never record temporarily relaxed formality as a permanent change. | 삭제 | 둘째 문단 "Keep it unchanged through temporary … one-scene shift"와 중복 |
| 13 | Separate public and private registers only for relationships where a real conditional distinction exists; | When the public and private rules above give a pair different registers, store both; | 8-2 "공적 상황 판정만 그 위에 적용" — 모든 쌍에 공적 판정이 덧씌워짐 |

유지한 원칙: "Never force a pet name or informal speech from the relationship label alone", 연인 행 "The relationship label alone does not establish informal speech", 방향별 판정 문단 전체.

## 분량

| | 단어 수 | 토큰 (Gemma 3 근사) |
|---|---|---|
| 원문 | 1,363 | 1,656 |
| 수정본 | 1,361 | 1,692 |

단어 수는 원문 이하. 토큰은 +36(약 2%) — 요구 3에 따라 넣은 한국어 호칭어(선배, 형, 누나, 오빠, 언니, 기준점)가 영어보다 토큰을 많이 씀.

## 검증 (수정본으로 판정)

1. **나이 많은 후배가 회사에서 선배에게:** 공적 상황 → 직급·역할·선후배가 나이보다 우선 → 존댓말, 호칭은 선배(선후배는 들어온 순서). 
2. **같은 두 사람이 퇴근 후 둘만:** 사적 상황 → 나이 우선 → 연하인 선배가 연상인 후배를 형/누나/오빠/언니로 부름. 공적·사적 값이 다르므로 두 값을 모두 저장. 연상 쪽이 반말로 바뀌는지는 수정본·8-2 모두 자동 규칙이 없어 기존 기록·설정을 따름.
3. **동갑 초면:** 존댓말. **반말 합의 후:** 합의가 로그에 서술되면 계기(Conditions for transition) → 다음 턴부터 반말로 갱신. 한쪽만 허락했다면 그 방향만 갱신.
4. **{{user}}가 연하 NPC에게 존댓말:** NPC 말투는 판정값 유지({{user}}의 존댓말이 NPC 존비어를 바꾸지 않음). 방향별 판정이라 {{user}} 쪽 기록과 NPC 쪽 기록은 따로 저장.
5. **과거 기록 존댓말, 최근 기록 반말:** 최근 기록(반말)이 현재 값, 과거 존댓말은 그 시점의 값. 단, 최근 것이 저장된 기록이 아니라 한 번 튄 문장이면 덮어쓰지 않음.
6. **다투다 일시적으로 반말이 섞임:** 일시적 감정(anger)·한 장면 변화 → 기록 유지, 그 장면에서만 표현. 결별처럼 실제 관계 단절이 서술되면 계기로 보고 다음 턴부터 갱신.
