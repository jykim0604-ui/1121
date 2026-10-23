# 프리셋 1 관련 보류 목록

프리셋 2 작업 직후 처리한다. 기준은 시스템 프롬프트이며, 프리셋 1에서 겹치는 부분만 수정하거나 삭제한다. 시스템 프롬프트에는 문장을 더하지 않는다.

행 번호는 `test_paste.md` ① 프리셋 1 블록 안의 순번이다.

## P1-1. 소리·발성·강도 — 3-2와 겹침 (G14 반영 완료)

기준 상태: 시스템 3-2에 弱·中·强 신음 강도, 기승전결 페이싱, "의성어는 실제로 쓰이는 한국어 의성어만 쓴다" 반영. 프리셋 2는 성인 블록·문체 경계·레지스터 경계·Scene pacing에서 겹치는 부분을 지우고 3-2 앵커, 수식어 앵커는 지문 한정(In narration).

| 프리셋 1 문장 | 3-2와의 관계 | 판정 |
|---|---|---|
| 99행 끊긴 말은 지금 가능한 소리·호흡·제어만큼, 완성된 문장을 나중에 꾸미지 않음 / 한국어 끊김 표기 | 中·强 "문장이 시작되다 끊긴다", "끝까지 이어지지 않는다"와 같은 방향 | 이어짐 |
| 100행 소리는 실제 출처·재질·접촉·거리로 고르고, 같은 효과음을 돌려 쓰지 않음 | 3-2 "강도는 구체적 사실로", "실제로 쓰이는 한국어 의성어만"과 같은 방향 | 이어짐 |
| 100행 `No punctuation plan or planned peak creates tempo or a bodily event.` / `Keep intentional sound spelling.` | 문장부호로 강도를 만들지 않음. 3-2 弱·中·强은 이미 정해진 강도의 모양이라 같은 방향 | 이어짐 |
| 102행 `A caused peak keeps its duration and recovery…`, `Literary finish or restraint shapes form; it does not shrink what the scene supports.` | 强의 지속과 회복, 문체가 강도를 줄이지 않음. 프리셋 2 경계와 같은 방향 | 이어짐 |
| 100행 `When a cry, plea… really repeats, keep its recurrence, spacing, interruption, vowel length and density` | 성적 장면에서 신음의 반복·모음 늘이기는 3-2 弱·中·强이 정한다(弱은 되풀이 없음, 强은 모음 되풀이). 같은 대상을 두 층이 맡음 | 겹침 |
| 102행 `give it its full expression: duration, density, repetition, volume… follow the specific source, active genre…` | 성적 장면의 반복·음량은 3-2가 맡는다. "active genre"가 장르 최대치로 끌어당길 수 있음 | 겹침 |
| 102행 `no low-to-high curve is assigned in advance` | 3-2 "기승전결의 흐름으로 진행", "신음의 강도는 장면의 기승전결에 따라 달라진다"와 정반대 | 충돌 |

- 관찰된 증상과의 연결: 첫 대사부터 최고 강도는 충돌 줄, 대사마다 늘어진 신음은 겹침 두 줄과 맞닿는다.
- 현재 처리: Charter 순서상 운영자 지시(시스템 프롬프트)가 위라 결과는 3-2를 따르지만, 모델은 매 응답 두 방향을 저울질한다.
- 반영 완료(G14)
  - 겹침 두 줄(100행 반복음, 102행 full expression): 성적 장면에 한정되지 않은 일반 원칙이라 중복이어도 그대로 유지. 성적 장면 예외만 앵커로 추가.
    - 100행 끝: `In sexual scenes, the repetition and vowel length of characters' vocalization follow the operator directions (3-2).`
    - 102행 끝: `In sexual scenes, the repetition, volume and intensity of characters' vocalization and the pacing of the act follow the operator directions (3-2).`
  - 충돌(102행 `no low-to-high curve is assigned in advance`): 삭제. 일반 기능(정해진 상승 곡선을 씌우지 않음)은 59행(강조는 장면이 쌓은 무게를 따름), 102행 `A caused peak…`, 프리셋 2 Balanced가 맡는다. 성적 장면은 위 102행 앵커가 3-2로 넘긴다.

## P1-2. 한국어 존비어 고정 — 3-1과 충돌

| 프리셋 1 문장 | 부딪히는 시스템 프롬프트 |
|---|---|
| 97행 `Start with accepted speech and explicit relationships, then culture, milieu, age/generation/school year, status, familiarity and individual formality.` | 3-1 계산 요소와 순서(설정 → 관계 판정 → 나이·들어온 시기·직급·친밀도·공적/사적) |
| 98행 `Inherit each direction across completed utterances. Emotion, attraction, embarrassment, fear, intimacy and escalation do not themselves change speech level. A deliberate switch is a speaker-owned event with a cause and consequence…` | 3-1 첫 등장 관계 판정, 합의와 허락 줄(이미 지내 온 사이면 합의가 있는 것으로 봄) |

- 관찰된 증상: 합의 없이 천편일률적으로 존댓말. 그러지 않아야 할 인물까지 모두 같은 양상.
- 진단: 98행은 말투 전환을 "말하는 사람이 일으키는 사건"으로만 인정한다. 3-1이 관계로 반말을 정해도, 프리셋 1은 전환 장면이 없으면 기존(대개 존댓말) 상태를 물려받게 한다. 3-1 합의 줄의 증거 요건과 겹쳐 존댓말로 굳는다.
- 시스템 프롬프트 쪽 짝 항목(3-1 합의 줄)은 프리셋 2 작업 보고의 "커버 못할 위험군"에 있다.

## P1-3. 짧은 응수 — 4-3과 겹침 (낮음)

| 프리셋 1 문장 | 시스템 프롬프트 |
|---|---|
| 55행 `Volleys of short questions met by denials, reversals, quips or echoes are not the default way to sustain a scene…` | 4-3 짧은 티키타카 구간("This stretch is not the chain of short volleys the preset cautions against.") |

- 현재 4-3이 예외를 명시해 충돌은 해소돼 있다. 프리셋 1 쪽 문장을 정리하면 4-3의 예외 문장도 덜어낼 수 있다.
