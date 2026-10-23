# 프리셋 1 관련 보류 목록

프리셋 2 작업 직후 처리한다. 기준은 시스템 프롬프트이며, 프리셋 1에서 겹치는 부분만 수정하거나 삭제한다. 시스템 프롬프트에는 문장을 더하지 않는다.

행 번호는 `test_paste.md` ① 프리셋 1 블록 안의 순번이다.

## P1-1. 소리·발성·강도 — 3-2와 충돌

| 프리셋 1 문장 | 부딪히는 시스템 프롬프트 |
|---|---|
| 102행 `Once the event is chosen, give it its full expression: duration, density, repetition, volume, directness, imagery, syntax and page space…` / `no low-to-high curve is assigned in advance` | 3-2 발성 강도 줄("처음부터 높지 않고", "끝까지 크게 오르지 않는 인물도 있다"), 단계 제한 |
| 100행 `When a cry, plea, refusal, breath, impact or environmental sound really repeats, keep its recurrence, spacing, interruption, vowel length and density` / `Keep intentional sound spelling.` | 3-2 말끝 늘이기·감탄부호 반복 제한, 의성어 제한 |

- 관찰된 증상: 성적 장면 대사마다 신음, 첫 대사부터 최고 강도, 말끝 모음 늘이기, 인물이 달라도 같은 소리(운영자 예시문).
- 짝 항목: 프리셋 2의 Expression register boundary("adult vocal surface", "repeated sound… duration")와 Prose style boundary("sound density" 및 성적 장면 예외 문장). 프리셋 2 쪽은 프리셋 2 작업에서 먼저 처리한다.
- 현재 처리: 헤더와 Charter 순서상 시스템 프롬프트가 이기지만, 반대 방향 지시를 매 응답 저울질한다.
- 수정 기준: 압축 전 7-2 페이싱·7-3 신음 단계화. 시스템 프롬프트·프리셋 2 쪽은 `preset2_system_list.md` 1·2번과 같은 기준으로 맞춘다.

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
