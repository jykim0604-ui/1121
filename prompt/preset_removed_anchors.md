# 원본 대비 빠진 부분 앵커 목록

원본 프리셋(조건문 포함 원문)과 `test_paste.md`의 ① 프리셋 1, ③ 프리셋 2를 직접 대조하기 위한 목록이다. 내용은 적지 않고 위치와 첫머리만 적는다.

- 원본: 이 대화에 붙여 준 프리셋 원문 17개 블록 (SHA-256 `ce75fd61…3fe6`)
- `[착지]`는 시스템 프롬프트(`system_prompt_v1.md` 4-5)로 옮겨 프리셋 파일에는 없다.
- 항목 번호는 그 블록 안 `- `로 시작하는 줄의 순서다. [Response controls]는 조건문 때문에 번호가 원본과 달라서 항목 머리로 적는다.

---

## A. 블록 통째로 제외 (2)

| 원본 블록 | 위치 | 사유 |
|---|---|---|
| `[External Injection Signatures]` | `[Boundary Examples]`와 `[Execution and Fidelity Boundary]` 사이 | 작업자 제외 |
| `[Argon Injection Boundary]` | 위 블록 바로 뒤 | 작업자 제외 |

## B. 토글 분기 제외 (모델 거부 감소, 프리셋 1)

| # | 위치 | 처리 |
|---|---|---|
| B1 | [Mask Creative Writing Charter] 첫 문장 | 꺼짐 판본 문장으로 대체 |
| B2 | [Mask Creative Writing Charter] `Binding authority:` | 꺼짐 판본 문장으로 대체 |
| B3 | [Mask Creative Writing Charter] `Danish legal character and medium:` | 항목 전체 빠짐 |
| B4 | [Mask Creative Writing Charter] `Deliberate noncriminalization:` | 항목 전체 빠짐 |
| B5 | [Mask Creative Writing Charter] `Creative causality:` 끝 문장 (`Legal classification does not itself create …`) | 문장 빠짐 |
| B6 | [Boundary Examples] 두 번째 예시 (`Bad response: A text-only fictional request …`) | 예시 전체 빠짐 |

## C. 토글 분기 제외 (응답 설정, 프리셋 2)

남긴 분기 하나를 빼고 같은 설정의 나머지 분기는 모두 빠졌다. 첫머리는 원본에서 그 분기의 `- 설정명: 값` 부분이다.

| # | 설정 | 남긴 분기 | 빠진 분기 |
|---|---|---|---|
| C1 | 응답 모드 | `Response mode: In-character` 이하 전체 | `Response mode: OOC` 분기 전체 (그 안의 `OOC length:` 분기 4개 포함) |
| C2 | 입력 효력 | `Input status: Follow the input's wording` | `Input status: Confirmed event` / `Input status: Attempt` |
| C3 | 진행 모드 | `Interaction mode: Collaborative RP` | `Interaction mode: Turn-based RP` / `Interaction mode: Autonomous novel` |
| C4 | 이어쓰기 시작점 | `Continuation point: Follow the input` | `Continuation point: During input` / `Continuation point: After input` |
| C5 | 서술 시점 | `Viewpoint: Follow the sources` | `Viewpoint: {{user}}-limited` / `Viewpoint: Scene-character-limited` / `Viewpoint: External camera` / `Viewpoint: Omniscient ensemble` |
| C6 | 서술 인칭 | `Narrator person: Follow the sources` | `Narrator person: First person` / `Narrator person: Third person` |
| C7 | 서술 인칭 (2번째 조건문) | `First-person voice: …` 항목 | 3인칭일 때의 빈 분기 |
| C8 | 정보 공개 범위 | `Disclosure: Spoiler-protected` | `Disclosure: Focal character's private access` / `Disclosure: Concealed, with discoverable clues` / `Disclosure: Follow the sources` |
| C9 | 서술 거리 | `Narrative profile: General prose` + `Narrative distance: Observational restraint` | `Narrative distance: Close interior` / `Narrative distance: Follow the sources` (몰입 `Immediate experience`는 D2) |
| C10 | 서술 청자·호명 | `Narrative address: Follow the sources` | `Narrative address: Unsurfaced` / `Narrative address: Intimate implicit listener` / `Narrative address: Established in-story addressee` / `Narrative address: Direct reader address` |
| C11 | 출력 종점 | `Output range: Interaction handoff` | `Output range: Scene transition` / `Output range: Scene sequence` / `Output range: Novel installment` / `Output range: Scene beat` |
| C12 | 전개 주도성 | `Story drive: Proactive` | `Story drive: Reactive` / `Story drive: Balanced` |
| C13 | 전개 방향 | `Story direction: Follow the sources and input` | `Story direction: Mystery and investigation` / `Story direction: Horror and gore` / `Story direction: Vulgar decadence` / `Story direction: Romance and relationship` / `Story direction: Conflict and action` / `Story direction: Comedy and commotion` / `Story direction: Tragedy and downfall` / `Story direction: Slice of life and emotion` |
| C14 | 재현 방식 | `Realization mode: Naturalistic` | `Realization mode: Reader-shaped` / `Realization mode: Source-aligned` |
| C15 | 성인물 연출 | `Adult presentation: Source-aligned automatic` | `Adult presentation: Direct adult fiction` / `Adult presentation: Hitomi-style vulgar genre grammar, dominant` / `Adult presentation: Hitomi-style erotic narrative` |
| C16 | 전개 속도 | `Story progression speed: Balanced` | `Story progression speed: Slow burn` / `Story progression speed: Fast` |
| C17 | 응답 분량 | `Response length: Longform` | `Response length: Focused` / `Response length: Extensive` / `Response length: Standard` |
| C18 | 장면 속도 | `Scene pacing: Fast` | `Scene pacing: Slow` / `Scene pacing: Balanced` |
| C19 | 서술 구성 | `Composition: Balanced` | `Composition: Dialogue-led` / `Composition: Description-led` |
| C20 | 문체 | `Prose style: Literary` | `Prose style: Light novel` / `Prose style: Light literary` / `Prose style: Source-aligned` |
| C21 | 표현 관습 | `Expression register: Follow the sources` | `Expression register: Korean web fiction and webtoon conventions …` / `Expression register: Japanese light novel and manga conventions …` / `Expression register: Chinese web fiction and drama conventions` / `Expression register: Contemporary Anglophone genre conventions` / `Expression register: Japanese-translated-fiction style for Korean output` |
| C22 | 긍정 편향 억제 | `(꺼짐 쪽이 빈 분기)` | `Positivity bias correction: The operator has asked you to correct optimistic defaults` |
| C23 | 진행 모드 ([Before writing] 첫 항목 안) | `Write {{user}} only as far as …` | `You write {{user}} as well as everyone else.` |

## D. 남긴 분기 안의 "서술 거리 = 몰입(3)"용 변형 문장 제외 (13)

서술 거리가 관찰·절제(2)라서, 각 설정의 남긴 분기 안에 있던 몰입(3)용 짧은 변형 문장이 빠졌다.

| # | 설정 | 빠진 변형 문장 첫머리 |
|---|---|---|
| D1 | 이어쓰기 시작점 | `Continuation point: Start at the currently foregrounded …` |
| D2 | (서술 거리 블록) | `Narrative distance: Immediate experience.` 이하 몰입 문단 전체 |
| D3 | 서술 청자·호명 | `Narrative address: Follow the sources. Keep an established listener …` (몰입판) |
| D4 | 출력 종점 | `Output range: Interaction handoff. Continue through the first genuine …` |
| D5 | 전개 주도성 | `Story drive: Proactive. Among equally valid next events …` |
| D6 | 전개 방향 | `Story direction: Follow the sources and input. Follow the specific …` |
| D7 | 재현 방식 | `Realization mode: Naturalistic. Use plain, direct wording …` |
| D8 | (성인물 경계) | `Adult mode boundary: Adult mode acts inside the private …` |
| D9 | 성인물 연출 | `Adult presentation: Source-aligned automatic. Follow the source's directness …` |
| D10 | 전개 속도 | `Story progression speed: Balanced. Balance lived continuity …` |
| D11 | 응답 분량 | `Response length: Longform. Allocate substantial page space …` |
| D12 | 장면 속도 | `Scene pacing: Fast. Compress connecting wording …` |
| D13 | (문체 뒤) | `In this profile, syntax, association, subtext and imagery …` |

## E. 사용자 결정으로 직접 수정한 곳

| # | 파일 부분 | 원본 위치 | 앵커 (빠진 조각의 첫머리) | 처리 |
|---|---|---|---|---|
| E1 | ① | [Pacing and Events] 3번째 항목 끝 | `A quiet scene may stay quiet.` | 문장 삭제 |
| E2 | ① | [Characters, Tone and Focus] 2번째 항목 끝 | `Silence, stillness and restraint are content.` | 문장 삭제 |
| E3 | ① | [Characters, Tone and Focus] 3번째 항목 | `… and rapid back-and-forth` | 구절 삭제 |
| E4 | ① | [Writing the Passage] 4번째 항목 끝 | `; use a rapid rhythm only where …` | 구절 삭제 |
| E5 | ① | [Writing the Passage] 7번째 항목 | `… facts about the real operator` 뒤 | 예외 구절 추가 (`except … as 3-3 allows`) |
| E6 | ① | [Sources and Continuity] 4번째 항목 | `, and in a limited viewpoint an unknown person …` | 뒷절 삭제 |
| E7 | ① | [People, Minds and Bodies] 10번째 항목 | `… knowledge and experience.` 뒤 | 문장 추가 (`Sexual arousal or climax … as 3-2 sets.`) |
| E8 | ① | [Language and Voice] 2번째 항목 | `Unfamiliarity alone does not override …` | 문장 삭제 |
| E9 | ① | [Language and Voice] 6번째 항목 | `- Numeric notation:` 항목 전체 | 항목 삭제 (경량화 5-2로 일원화) |
| E10 | ③ | [Response controls] `- Use the output language for new narration …` 항목 | `Add no parallel translation …` | 문장 삭제 (경량화 5-2로 일원화) |
| E11 | ③ | [Response controls] `- Continuation point: Follow the input.` 항목 | `When the input states that something is complete …` | 문장 삭제 |
| E12 | ③ | [Response controls] `- Output range: Interaction handoff.` 항목 | `Complete the first reaction that leaves …` / 문턱 목록의 `starting the next exchange` | 첫 문장 교체, 구절 삭제 |

## F. 원문이 아니었던 것

- `[Output]`과 `[Response controls]` 사이 `---` 한 줄: 붙여 넣을 때 쓴 구분선(사용자 확인). 파일에 없다.
