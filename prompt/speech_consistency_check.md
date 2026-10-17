# 8-2 ↔ 플러그인 프롬프트 일치 검증

- 8-2: `speech_8-2_ko.md` (메인 프롬프트용, 한국어)
- 플러그인: `risupot_speech_revised.md` (리수폿용, 영어)

## 줄 단위 대응

| # | 8-2 줄 | 플러그인 대응 | 판정 |
|---|---|---|---|
| 1 | 본문 첫 문장 전 확정 / 이전 턴 값 이어 씀 / 처음 말하는 쌍만 계산 / 공적 판정을 위에 적용 | 기록 = 그 쌍이 이미 쓰는 값 / Use an established record first … initial judgment by the criteria below / store both | 일치 ("본문 첫 문장 전"은 출력 단계라 제외) |
| 2 | 과거 기록이 다르면 최근 기록이 현재 값 | When records conflict, the most recent record is the current value … | 일치 |
| 3 | {{user}}가 존댓말을 써도 NPC 존비어 유지 | {{user}}'s polite speech does not change an NPC's judged register | 일치 |
| 4 | 계산 요소: 나이, 직급, 친밀도, 공적/사적 | 축 표 + 불릿 전체 | 일치 |
| 5 | 선후배 = 먼저 들어온 쪽, 나이 무관 | Seniority 행 | 일치 |
| 6 | 공적 상황은 직급·역할·선후배 우선, 연상 하급자는 존댓말 | Public 불릿 | 일치 |
| 7 | 형/오빠/누나/언니는 사적 친분이 있는 사이에서만, 보통 합의 / 공적 접점만 있으면 선배·후배·직함 / 친분이 있어도 공적 자리는 선배·후배·직함, 사적 자리는 형 등 | 형, 오빠, 누나, 언니 불릿 + Colleagues 행 + store both 문장 | 일치 |
| 8 | 호칭 두 축 따로 (선후배는 들어온 순서, 형·누나는 나이) | judging seniority and age separately / Age 행 "Who is called … follows age only" | 일치 |
| 9 | 호칭과 존비어는 따로 정하고 따로 바뀌며 방향별, 호칭이 바뀌어도 존비어 그대로 | Address and register are judged and change separately, per direction … | 일치 |
| 10 | 초면은 나이 무관 상호 존댓말, 공적 관계 없으면 이름+씨, 붙임성 있는 연하는 초면에도 형 등 가능(나이 차 클수록 자연스러움) | First meeting 불릿 | 일치 |
| 11 | 반말은 방향별 허락·합의 / 연상은 연하 허락 시 친분 없이도 / 연하는 친분+합의, 먼저 정하면 무례 / 허락 없는 초면 반말은 껄렁한 성격 등 특이한 경우뿐 | Informal speech 불릿 | 일치 |
| 12 | 반대 방향(연상 후배·연하 선배 등)은 양쪽 존댓말, 공적·사적 무관, 합의 후에만 변경 | opposite directions 불릿 | 일치 |
| 13 | 관계 없거나 같은 방향이면 사적 자리에서 나이 우선 = 누가 형 등으로 불리는지·누가 반말을 허락하는지를 정함, 나이만으로 반말 시작 안 됨 / 동갑 / 연인 | Private 불릿 + Same age 불릿 | 일치 |
| 14 | 확정 대상은 호칭·존비어, 호명 생략해도 유지 | Store address and register … | 일치 |
| 15 | 말투 변경은 계기 서술 후 다음 턴부터 | Update it only when the conversation log narrates a catalyst … next turn | 일치 |
| 16 | 나이 = 생년, 선후배 = 들어온 시기 (하단 상태창) | Read birth year and entry timing (기준점) from the bottom status window | 일치 |
| 17 | 실존 인물 들어온 시기는 '웹 검색' | — | 의도적 미포함 (검색은 메인 모델이 함. 플러그인은 결과가 적힌 상태창을 읽음) |
| 18 | 검색값은 인지 자료 아님 / 검색에서는 들어온 시기만, 5-3 | — | 의도적 미포함 (메인 전용. 플러그인의 인지 경계는 Knowledge 섹션 담당) |
| 19 | 확인 안 되면 추정해 확정, 하단 상태창에 적음 | estimate … store it marked as an estimate and replace it once confirmed | 일치 (적는 곳만 저장으로 바뀜) |
| 20 | {{user}}도 같은 기준, 높이지 않음 | judged by the same criteria and never ranked higher | 일치 |

플러그인에만 있는 문장 중 8-2와 부딪히는 것: 없음 (관계별 호칭 예시표, 방향별 판정, Conditions for transition 이하 섹션 확인). Conditions for transition의 "If permission applies in only one direction, update only that direction"은 8-2 11번 줄과 같은 방향.

## 사례 판정 (양쪽 문서에 각각 대입)

| 사례 | 8-2 결과 | 플러그인 결과 | 일치 |
|---|---|---|---|
| 1. 회사에서 연상 후배 → 연하 선배 | 공적 + 반대 방향 → 양쪽 존댓말. 친분 없음 → 호칭은 선배·후배·직함 | 동일 | O |
| 2. 같은 두 사람이 퇴근 후 둘만 (친분 없음) | 반대 방향 → 양쪽 존댓말 유지. 친분 없음 → 형 등 호칭 안 씀 | 동일 | O |
| 3. 동갑 초면 / 반말 합의 후 | 초면 상호 존댓말 / 합의 서술 → 다음 턴부터 반말 (합의한 방향만) | 동일 | O |
| 4. {{user}}가 연하 NPC에게 존댓말 | NPC 존비어는 판정값 유지 | 동일 | O |
| 5. 과거 존댓말, 최근 반말 기록 | 최근 = 현재 값, 과거 = 그 시점 값 | 동일 (튀는 문장 하나는 기록으로 보지 않음) | O |
| 6. 다투다 일시적으로 반말 | 계기 아님 → 확정값 유지 (메인 6-1 감정 관성과 함께 작동) | temporary anger → 기록 유지 | O |
| 7. 조직 관계 없는 연상·연하가 사석에서 처음 만남 | 초면 → 상호 존댓말, 이름+씨. 붙임성 있는 연하라면 형 등도 가능 | 동일 | O |
| 8. 예시 대화 A(연상)·B(연하) 초면 | ① 서로 "씨"+존댓말 ② B "말씀 편하게 하세요" → 연상 A의 반말은 연하 B의 허락으로 시작 ③ A "형이라고 해" → B→A 호칭만 형 ④ B→A는 친분·합의 없음 → 존댓말 유지 ("네 형. 식사는 하셨어요?") | 동일 (Informal speech 불릿 + Address and register separately 불릿) | O |
| 9. 초면 연하가 "형이시네 편하게 할게 형" | 연하가 먼저 반말을 정함 → 무례 (해당 성격이 아니면 생성하지 않음) | a younger person deciding on informal speech first is rude | O |
| 10. 친분 있는 직장 선후배(연상 선배·연하 후배) | 회의 자리: 선배·직함 / 퇴근 후: 형 등. 존비어는 별도로 판정·합의된 값 | 공적·사적 호칭이 달라 둘 다 저장, 존비어 별도 | O |

## 사용자 확인이 필요한 점 (두 문서끼리는 일치)

- **변경 적용 시점:** 8-2의 "말투 변경은 본문에서 계기를 서술한 뒤 다음 턴부터 적용한다"를 그대로 따르면, 사례 8처럼 한 턴 안에서 "편하게 하자"라고 합의한 직후 바로 반말로 넘어가는 대사는 규칙상 다음 턴으로 미뤄짐. 예시 대화에서는 합의 직후 같은 대화 안에서 바로 반말로 바뀜. 같은 턴 안의 즉시 전환을 허용할지 정해야 함 (바꾼다면 8-2와 플러그인 서두 문단에 같은 문장으로).
