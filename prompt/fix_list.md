# 수정해야 할 목록 (통합)

원칙: 프리셋 1, 시스템 프롬프트, 프리셋 2는 각자 작동한다. 어느 한 층이 혼자 맡는 지침은 남긴다. 겹치는 일반 지침은 두고 예외만 앵커로 넘긴다. 정면 충돌은 지우고 앵커로 넘긴다. 새 지침을 늘리지 않는다.

완료: NSFW 발성·강도·페이싱·밀도(G13, G18 보완), 수식어 앵커 지문 한정(G13), 프리셋 1 소리·표현(G14), 프리셋 1 존비어·짧은 응수(G15), 이 목록의 1-1·1-2·2-1·2-2(G16). 세부는 `b2_review.md`, `preset2_system_list.md`, `preset1_hold.md`.

## 1. 충돌 — 프리셋 2 ↔ 시스템 프롬프트

### 1-1. Output range의 두 번째 문턱 ↔ 4-5 행동의 결과 — 반영 완료(G16)

- 프리셋 2: `Do not cross a second information or action threshold: opening something closed, revealing a clue, changing location or carrying out its consequence is a second threshold unless that threshold itself was the operator's explicit immediate request.`
- 시스템 4-5: `{{user}}가 아닌 인물이 시작한 동작은 결과까지 쓴다. 손을 뻗었으면 잡았는지, 문을 열려 했으면 열렸는지까지 쓰고 그 직전에서 끊지 않는다.`
- 판정: 정면 충돌(같은 예시를 반대로 지시). 다만 두 번째 문턱 원칙은 프리셋 2 단독 기능이고, 겹치는 범위는 "NPC가 이미 시작한 행동"뿐이다.
- 방향: 프리셋 2 문장은 유지하고 끝에 앵커. `An action a character other than {{user}} has already started is carried to its result as the operator directions (4-5) set.`
- 중요도: 중간~높음.

### 1-2. Interaction mode의 {{user}} 작은 반응 허용 ↔ 4-5 1:1 — 반영 완료(G16)

- 프리셋 2: `For continuity you may add only a strongly implied, low-commitment micro-action or an immediate involuntary or sensory reaction of {{user}}'s…`
- 시스템 4-5: `{{user}}와 NPC 한 명뿐인 장면: … 그 사이 {{user}}가 대답하거나 되받는 말과 행동은 쓰지 않는다.`
- 판정: 겹침. 허용은 프리셋 2의 일반 기능(장면 연속), 1:1 장면에서만 반대 방향. 1:1에서 {{user}} 대사를 지어내던 증상(G1)과 같은 자리.
- 방향: 프리셋 2 문장 유지, 끝에 앵커. `In a scene with only {{user}} and one NPC, {{user}}'s responses follow the operator directions (4-5).`
- 중요도: 중간.

### 1-3. 서술 거리 ↔ 전지적 시점·inner life (운영자 보류)

- 프리셋 2 Narrative distance `Keep interior access sparse` ↔ Viewpoint `may reveal several minds`, Composition·Response length `inner life`.
- 상태: 거리감(Close interior) 결정 보류와 같은 건. 결정 후 처리.

### 1-4. 유혹 단계 속도 (G17 재검수, 낮음~중간)

- 시스템 3-2 첫 줄: `호감과 유혹은 기본적으로 시선, 거리 조절, 농담, 찰나의 접촉으로 천천히 진행한다.`
- 프리셋 2: Scene pacing Fast `Place the range's decisive action early…`, Story drive Proactive.
- 판정: 겹침. G13 앵커(`In sexual scenes, the pacing of the act…`)는 성적 장면만 넘겨, 그 전 유혹 단계는 덮지 않는다.
- 방향 후보: Scene pacing 앵커 범위를 `In seduction and sexual scenes`로 넓힌다. 테스트에서 유혹이 빨라지는 게 보이면 반영.

### 1-5. 숨은 사실을 담은 사물 (G17 재검수, 낮음)

- 시스템 4-5: `말과 어긋나거나 말하지 않은 사실이 담긴 사물 하나를 비출 수 있다.`
- 프리셋 2 Disclosure: `do not plant optional clues, symbolic echoes, slips, suspicious emphasis or telltale behavior to help discovery.`
- 판정: 그 사실이 카드에만 있는 숨은 설정이면 반대 방향. 이미 장면에서 드러난 사실이면 충돌 없음.
- 방향 후보: 프리셋 2 Disclosure 끝에 `The object the operator directions (4-5) allow may hold only facts already shown in the story.` 숨은 설정이 사물로 새는 게 보이면 반영.

## 2. 빈틈 — 시스템 프롬프트 안 (G7 삽입 문장이 좁음)

### 2-1. {{user}}와 함께 겪은 일 — 반영 완료(G16)

- 이전 2-1: `NPC는 자신이 {{user}}와 함께 겪어 온 관계를 처음부터 안다.`
- 빈틈: 바로 앞 문장(페르소나의 경력, 과거, 성격은 드러난 뒤에 안다) 때문에, 소꿉친구 같은 NPC가 함께 겪은 과거와 그 안에서 본 성격을 모르는 척할 수 있다.
- 방향: 삽입 문장만 고침. `함께 겪어 온 관계` → `함께 겪어 온 관계와 일`. 영문 `the relationship they themselves have shared with {{user}}` → `the relationship and experiences they themselves have shared with {{user}}`.
- 중요도: 중간(설정에 함께 지낸 과거가 있는 NPC에서 발생).

### 2-2. 다른 인물의 공개 정보 — 반영 완료(G16)

- 이전 2-1 기록 줄: `…하단 상태창은 인물이 남의 일을 아는 근거가 아니다.`
- 빈틈: "남의 일"이 데뷔·소속 같은 공개 정보까지 막는다. 3-1 `선배·후배는 말하는 사람이 아는 들어온 순서로만 쓴다`와 맞물려, 업계 사람이 다 아는 데뷔 순서도 모르는 것으로 처리될 수 있다. 공개 활동 예외는 {{user}}에게만 있다.
- 방향: 삽입 낱말만 고침. `남의 일` → `남의 사적인 일`. 영문 `other people's affairs` → `other people's private affairs`.
- 중요도: 낮음~중간(관찰되면 우선).

## 3. 테스트로 확인할 것

- 3-1. NSFW(G13·G14·G18): 운영자 예시문과 같은 유형의 장면으로 비교. G18 이후 추가 관찰: 강도가 칸을 건너뛰지 않고 이어지는지, 끝난 뒤 차츰 가라앉는지, 수치 나열과 상투구가 줄었는지. 첫 대사부터 强인지, 인물마다 소리가 갈리는지, 지문이 접촉·움직임·소리의 사실로 서는지, 기승전결이 턴에 나뉘는지.
- 3-2. 존비어(G15): 천편일률 존댓말이 풀리는지. 반대로 공적 자리, 연하가 먼저, 반대 축 쌍에서 반말이 과하게 열리는지.
- 3-3. 3-2에서 계산 자체가 안 걸리는 증상(G8)이 남으면: 압축 전 8-2 첫 문장 `본문 첫 문장 전에 이번 턴 발화 인물 전원의 호칭과 존비어를 확정한다.`를 3-1 앞에 되살리는 안을 검토.

## 4. 기존 운영자 보류

- 4-1. 서술 거리 Close interior 전환(= 1-3).
- 4-2. 5-2 풀네임 마지막 문장(G9): 파일에는 있음, 앱 테스트는 그 문장을 뺀 상태로 진행 중.
- 4-3. 5-1 자율 턴을 대사로 시작하는 문제 수정안.
- 4-4. 장기기억 플러그인 저장 프롬프트: 붙여 넣기 대기.

## 5. 확인 후 닫은 것 (충돌 없음)

- Story progression speed boundary ↔ 4-5 "매 응답 무언가 바뀐다": 지속 변화와 국소 변화를 구분.
- Response length: Longform ↔ 4-5 분량: 같은 방향의 중복.
- Composition "atmosphere" ↔ 4-2 추상명사: 성적 장면은 성인 블록 앵커(밀도는 3-2, 수식어는 4-2), 일반 장면은 4-2 "근거 있는 이미지만"으로 정리.
- 시점 갈래(Narrator person, Focal character 등): 현재 설정에서 작동 범위 없음.
- 4-3 ↔ 프리셋 1 짧은 응수: G15로 앵커 정리.
- 5-1 요지 ↔ Input status, 헤드라인 위치, 헤더 G7, 전지적 시점 ↔ 2-1, 3-1 이어 쓰기(A3).

## 6. 대기 중

- 6-1. 분량 지침 정리: 운영자 의견 대기(2-B 항목 피드백 예정). 후보는 프리셋 2 `Response length: Longform.`과 시스템 4-5 "입력이 짧아도 본문은 넉넉하게…" 두 줄, 짝으로 Scene pacing의 `longform or description-led composition` 구절.
- 6-2. 4-2 "보이거나 셀 수 있는 값"이 일반 장면에서 수치 나열을 부추기는지 관찰.
