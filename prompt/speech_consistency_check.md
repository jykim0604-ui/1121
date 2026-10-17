# 8-2 ↔ 플러그인 프롬프트 일치 검증

- 8-2: `speech_8-2_ko.md` (메인 프롬프트용, 한국어)
- 플러그인: `risupot_speech_revised.md` (리수폿용, 영어)

## 이번에 바꾼 곳

| 위치 | 변경 |
|---|---|
| 8-2 | 반대 방향 규칙 1줄 추가 ("나이 축과 선후배·직급 축이 반대 방향인 사이…") |
| 8-2 | "사적 상황… 나이가 우선" 줄에 적용 범위 추가 ("선후배·직급 관계가 없거나 나이와 같은 방향인 사이에서는") |
| 플러그인 | 같은 내용의 불릿 1개 추가 (When age and seniority or rank point in opposite directions…) |
| 플러그인 | Private 불릿에 같은 적용 범위 추가 (between people with no seniority or rank relation or whose age points the same way) |
| 플러그인 | 동료 행: "outside work, age decides" → "outside work, the register stays the same unless an agreement changes it" (반대 방향 규칙과 충돌해서) |

8-2의 나머지 줄은 메인 원본(`original_ko.md`)과 같음. '검색 채팅' → '웹 검색'은 사용자가 이미 바꾼 표기를 따름.

## 줄 단위 대응

| 8-2 줄 | 플러그인 대응 | 판정 |
|---|---|---|
| 이전 턴 호칭·존비어 이어 씀, 처음 말하는 쌍만 계산 | 기록 = 그 쌍이 이미 쓰는 값 / Use an established record first … initial judgment by the criteria below | 일치 |
| 본문 첫 문장 전에 확정 | — | 의도적 미포함 (출력 단계 지시) |
| 공적 상황 판정만 그 위에 적용 | When the public and private rules above give a pair different registers, store both | 일치 |
| 과거 기록이 다르면 최근 기록이 현재 값 | When records conflict, the most recent record is the current value … | 일치 |
| {{user}}가 존댓말을 써도 NPC 존비어 유지 | {{user}}'s polite speech does not change an NPC's judged register | 일치 |
| 계산 요소: 나이, 직급, 친밀도, 공적/사적 | 축 표(선후배·나이) + 공적/반대 방향/사적/동갑·연인 불릿 | 일치 |
| 선후배 = 먼저 들어온 쪽, 나이 무관 | Seniority 행 | 일치 |
| 공적 상황은 직급·역할·선후배 우선, 연상 하급자는 존댓말 | Public 불릿 | 일치 |
| 연하가 연상에게 형/오빠/누나/언니 | Age 행 | 일치 |
| 두 축 따로, 늦게 들어오면 선배 아님 | judging seniority and age separately / regardless of age | 일치 |
| **반대 방향이면 양쪽 존댓말, 공적·사적 무관, 합의 후에만 변경** | **opposite directions 불릿** | 일치 |
| **사적 나이 우선 (관계 없거나 같은 방향일 때만)**, 동갑, 연인 | **Private 불릿**, Same age 불릿 | 일치 |
| 확정 대상은 호칭·존비어, 호명 생략해도 유지 | Store address and register … | 일치 |
| 말투 변경은 계기 서술 후 다음 턴부터 | Update it only when the conversation log narrates a catalyst … next turn | 일치 |
| 나이 = 생년, 선후배 = 들어온 시기 (하단 상태창) | Read birth year and entry timing (기준점) from the bottom status window | 일치 |
| 실존 인물 들어온 시기는 '웹 검색' | — | 의도적 미포함 (검색은 메인 모델 기능. 플러그인은 그 결과가 적힌 상태창을 읽음) |
| 검색값은 인지 자료 아님 / 검색에서는 들어온 시기만, 5-3 | — | 의도적 미포함 (메인 전용. 플러그인의 인지 경계는 Knowledge 섹션이 담당) |
| 확인 안 되면 추정해 확정, 하단 상태창에 적음 | estimate … store it marked as an estimate and replace it once confirmed | 일치 (적는 곳만 저장으로 바뀜) |
| {{user}}도 같은 기준, 높이지 않음 | judged by the same criteria and never ranked higher | 일치 |

플러그인에만 있는 내용 중 8-2와 부딪히는 문장: 없음 (관계별 호칭 예시표, 방향별 판정, Conditions for transition 이하 섹션 확인).

## 사례 판정 (양쪽 문서에 각각 대입)

| 사례 | 8-2 | 플러그인 | 일치 |
|---|---|---|---|
| 1. 회사에서 연상 후배가 연하 선배에게 | 공적 → 선후배 우선 + 반대 방향 → 양쪽 존댓말, 호칭은 선배 | Public + opposite directions → 양쪽 존댓말, 선배 | O |
| 2. 같은 두 사람이 퇴근 후 둘만 | 반대 방향 → 사적이어도 양쪽 존댓말 유지 (사적 나이 우선은 적용 범위 밖) | opposite directions → holds in private → 양쪽 존댓말 | O |
| 3. 동갑 초면 / 반말 합의 후 | 초면 존댓말 / 합의 서술 → 다음 턴부터 반말 | 초면 polite / 합의 = 계기 → 다음 턴부터 갱신 (한쪽만 허락하면 그 방향만) | O |
| 4. {{user}}가 연하 NPC에게 존댓말 | NPC 존비어는 확정값 유지 | NPC 판정값 유지, 방향별 따로 저장 | O |
| 5. 과거 존댓말, 최근 반말 기록 | 최근 = 현재 값, 과거 = 그 시점 값 | 동일 (튀는 문장 하나는 기록으로 보지 않음) | O |
| 6. 다투다 일시적으로 반말 | 계기 없음 → 확정값 유지 (메인 6-1 "태도와 말투는 관성을 따른다"와 함께 작동) | temporary anger → 기록 유지 | O |
| 7. 조직 관계 없는 연상·연하가 사석에서 | 관계 없음 → 나이 우선 → 연하가 존댓말, 형/누나 등 | 관계 없음 → age takes priority → 동일 | O |

## 남은 확인 사항 (일치 문제 아님)

- 반대 방향 쌍의 **호칭**: 두 문서 모두 "연하가 연상을 부를 때 형/오빠/누나/언니"를 조건 없이 두고 있어, 연하 선배도 연상 후배를 형/누나 등으로 부르는 것으로 읽힘(두 문서끼리는 일치). 직장 같은 공적 자리에서 이 호칭이 실제 관습과 맞는지는 별도 확인이 필요하며, 바꾼다면 양쪽에 같은 문장으로 넣어야 함.
