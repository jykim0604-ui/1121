# B2~B4 검수 — 남은 항목 (3판)

대상: `preset_b4.md` 본문
구조: 프리셋 1 → `[착지]` → 경량화 → `---` → 프리셋 2 (하나의 시스템 프롬프트)
상태: A1~A13 모두 반영 완료(내역은 `preset_b3.md`, `preset_b4.md` 상단). S8은 위 구조로 확정. 아래는 남은 항목이다.

---

## S. 단일 프롬프트화 정리 대상

| # | 위치 | 현재 문장 | 문제 | 선택지 |
|---|---|---|---|---|
| S1 | 경량화 머리말 | `[Operator Directions — 이 작품의 고정 지시]` / "아래는 이 작품에 대한 운영자의 명시적 지시다. 여기 적힌 항목에 한해 일반 작법 규칙보다 우선하는 이 작품의 구체적 예외로 적용하고, 여기 적히지 않은 것은 프리셋의 규칙과 응답 설정을 따른다." | "프리셋"이라는 별도 문서를 가리킨다. 찾아낸 충돌은 본문에서 모두 정리했으므로 우선 선언은 찾지 못한 충돌에만 작동한다 | ① 그대로 ② "프리셋" 언급만 빼고 우선 선언은 유지 ③ 제목만 두고 둘째 문장 삭제 |
| S2 | 프리셋 1 [Language and Voice] / 경량화 5-2 | `Numeric notation: …` 한 문단 / "숫자 표기 [CRITICAL]: 프리셋의 Numeric notation 대신 이 항목만 따르며" | 같은 프롬프트에 숫자 규칙이 둘 있고, 하나가 다른 하나를 무효로 선언한다 | ① 그대로 ② 프리셋 문단 삭제 + 경량화의 "프리셋의 Numeric notation 대신" 삭제 |
| S3 | 프리셋 1 [Output] / 경량화 6 | "In-character output begins with the story itself, without a title, heading or other wrapper unless the requested format or the sources require one" / "'제목이나 머리말 없이 이야기로 시작한다', '상태 표기를 출력에 넣지 않는다'는 일반 규칙의 예외다." | 출력 형식이 두 곳. 다만 경량화 문장은 "프리셋"을 언급하지 않고 "일반 규칙"이라고만 해서 하나의 프롬프트에서도 뜻이 통한다 | ① 그대로 (수정 불요) ② [Output]에 상태창 예외를 옮기고 경량화 문장 삭제 |
| S4 | 프리셋 1 [Role] | "Story sources come before the conversation; the settings for your next response come after the operator's latest turn." | 하나의 시스템 프롬프트에서는 응답 설정도 대화 앞에 있으므로 뒷절이 사실과 다르다 | ① 뒷절 삭제 ② 뒷절을 "the settings for your next response are in [Response controls]"로 교체 |
| S5 | 프리셋 2 [Response controls] 첫 줄 | "These are the operator's current settings for your next response. They are not part of {{user}}'s message." | 둘째 문장은 설정이 입력 뒤에 붙을 때를 위한 안내다. 시스템 프롬프트 안에서는 할 일이 없다(해는 없음) | ① 그대로 ② 둘째 문장 삭제 |
| S6 | 프리셋 1 Charter | "(1) this Charter; (2) explicit current operator directions and corrections; (3) accepted fictional sources, canon, character state, and active response controls; (4) general craft heuristics" | 경량화 제목이 "Operator Directions"로 남아 있으면 경량화는 (2), 프리셋 규칙은 (4)로 읽힌다. 대화 중 OOC 정정에도 (2)가 쓰인다 | S1 결정에 따름. 제목을 유지하면 수정 불요 |
| S7 | 프리셋 1 [Sources and Continuity], 프리셋 2 성인물 연출 | "… the supplementary information and the writer note …" / "The writer note directs the current response and is not something the characters know." / "an active genre or writer note" | 경량화가 원래 작가 노트 자리에 있었다면 가리키는 대상이 바뀐다. 앱의 작가 노트(유저노트)를 계속 쓰면 문제없다 | 작가 노트(유저노트)를 계속 쓰는지에 따름. 쓰면 수정 불요, 안 쓰면 그대로 둬도 해는 없음 |
| S9 | 중복 (충돌 아님) | ① 중·고교 같은 학년 반말: [Language and Voice] "In a contemporary Korean secondary school, same-year peers ordinarily use peer casual speech" / 경량화 3-1 "중·고등학교 같은 학년끼리는 초면에도 서로 반말이 기본이다" ② 말투 방향별 유지: [Language and Voice] "Inherit each direction across completed utterances" / 경량화 3-1 "이전 턴에 쓴 호칭과 존비어는 그대로 이어 쓰고" ③ {{user}} 차례 표시 금지: [Ending the Response] / [Before writing] | 같은 내용이 두 곳 | 압축 단계로 넘김 |

S1 관련 참고: A10, A13에서 프리셋 문장에 붙인 예외가 경량화 절 번호(`as 3-3 allows`, `as 3-2 sets`)를 가리킨다. 머리말을 바꿔도 절 번호를 유지하면 영향 없음.

---

## C. 구조·기록

| # | 위치 | 내용 | 선택지 |
|---|---|---|---|
| C1 | 경량화와 `[Response controls]` 사이 `---` | 붙여 넣을 때 쓴 구분선일 가능성이 높다. 블록은 `[제목]`으로 이미 구분되고, 프리셋 [Output]은 `---`를 장면 재개 표시로 쓰라고 정한다 | ① 그대로 ② 삭제 |
| C2 | 조건문 제거 흔적 | Charter, Response controls의 연속 빈 줄 | 압축 단계로 넘김 |
| C3 | 외부 의존 | 경량화 6 헤드라인은 별도 로어북(`headline_ko.md`). 태그 수정값은 앱 입력란에 넣어야 함 | 기록만 |
