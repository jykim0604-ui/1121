<!-- V6 (custom): target-specific affinity records follow the slow cadence; one conversation is scene performance. -->
<!-- V5 (1.1.4): first impression and current evaluation use separate records, kinds and entry references. -->
# Affinity and Taste — Writer Records

Compare completed RP with existing entries. Never record a reaction, approach, or emotional change that appears only as a Director proposal and did not become established in RP. Explicit relationship facts from the source may remain in core, but never move this feature's additional appraisal into core to bypass feature OFF.

Use only allowed slots:

| Slot | Content to record |
|---|---|
| `affinity.profile` | The individual's scope of interest, observable tastes and aversions, form of feeling, restraint style, approach style, and their evidence |
| `affinity.values` | Value priorities, observation criteria, general biases, and the character's logic for them |
| `affinity.appraisal` | First impression only: the unchanging initial appearance-based person appraisal and emotion |
| `affinity.current_appraisal` | Current evaluation only: the present person appraisal, its evidence and resulting emotion |
| `affinity.intent` | Nature of target-specific interest and its primary and secondary intents |
| `affinity.stance` | Established target-specific interpretation and treatment as separate elements, with evidence for change |
| `affinity.bind` | Constraints, the way they are handled, rationalization, and evidence for an actual transition |
| `affinity.private` | Unexpressed feeling, conditions limiting expression, actual leaks, and recipients |
| `affinity.approach` | Established approach pattern, the target's accepted or refused response, confirmed boundaries, and the currently permitted range |
| `affinity.surface_actual` | Outward conduct and actual purpose of exploitative or abusive intent, accumulated attempts, witnesses, and results |

## Independent first-impression and current-evaluation records

Use TWO independent text slots for each NPC-to-target direction: affinity.appraisal is 첫인상; affinity.current_appraisal is 현재 평가. Each has its own entry_ref, body and pin. Never combine both into one entry, put both labels in one text, or overwrite a first-impression entry_ref with a current evaluation. Use the same actual target for the two records, actor:user for the current persona. One record per slot and target; never create extra contexts or duplicates to bypass a recorded first impression.

If either record is missing or empty, fill that record when the NPC speaks to or is addressed by that partner in confirmed RP. No first-ever conversation, prior relationship, matching Lore relationship, previously created Wiki or numeric metric is required. This includes earlier omissions. Let Writer identify the speakers/addressees from context; someone else's dialogue, a passing mention or co-presence alone does not qualify. Keep the existing NPC-memory and active-slot rules for other targets. Both records may initially express the same evaluation, but must still be separate entries. Filling one does not authorize changing the other.

**First impression — write once, affinity.appraisal.** Only when absent/empty, write a compact Korean appearance appraisal: visible cue → subjective image of the target → the NPC's emotion and its personality-based reason. Use supplied, scene-visible face, build, grooming, clothing, accessories, carried items, posture or expression. Relate those cues to the NPC's established tastes, values, biases and personality. Include the resulting feeling: liking, anticipation, admiration, envy, aversion, distrust, indifference or mixed feelings as supported. Once this record is nonempty, OMIT every update/removal to it. Never revise, expand, shorten, correct or replace it because of later appearance, discoveries, relationship changes or emotion. A mistaken or explicitly unknown first impression also remains as originally recorded. New understanding belongs exclusively in the current evaluation.

Examples illustrate reasoning, not facts to copy. For an NPC who values money: “The expensive-looking clothes and watch suggest wealth. Because this NPC values money, they feel liking and anticipation.” For an NPC who values looks: “The distinct facial features match this NPC's taste, prompting attraction and attention.” An ostentation-averse NPC could instead infer showing off and feel aversion. Never invent the visible features or the observer's preferences just to produce a favorable response.

**Current evaluation — update with evidence, affinity.current_appraisal.** Initialize from what this NPC currently knows and feels. After it exists, it follows the slow cadence in the core Writer instructions: revise it only when a catalyst or a newly learned fact materially changes this NPC's judgment of the person, or when the same changed judgment appears in at least two distinct scenes. A passing emotion in one conversation, a pleasant chat, one favor, or one display of already known skill shows in the scene, not here. Record the present person evaluation, its concrete reason and resulting feeling through the NPC's own personality. An earlier favorable first impression may coexist with a currently unfavorable evaluation. A corrected interpretation need not change the emotion, and a changed feeling need not change every judgment. No score, relationship-stage or personality change is required. If no supported revision is needed, omit the upsert. Never rewrite it as a diary of recent scenes. Update only this slot's existing entry_ref when it changes; leave the first-impression entry out of the response.

Store both records as assessment. An observed cue may support a provisional interpretation and feeling without an explicit RP inner-monologue sentence; mark inference as such and cite evidence. Distinguish “looks wealthy” from verified wealth. Persona appearance is usable only when visible; hidden wealth, background, ability, intentions and private traits are not automatically known. If no usable visual evidence exists, record the uncertainty instead of inventing an appearance. Do not later backfill an already recorded first impression with knowledge acquired afterward.

Keep every existing legacy affinity.appraisal body unchanged in the first-impression record, whether it is unlabeled or contains the old first/current labels. Do not split, move or duplicate that original text automatically. Treat it as an existing record baseline, not proof of the exact original encounter. The independent current-evaluation record starts separately and is filled during a qualifying conversation from supported current evidence. Never replace or rewrite the preserved legacy record while creating the new current evaluation.

Each text contains only that kind's prose, within its supplied text limit. Pins remain authoritative. For these two slots this write-once/current-update distinction takes precedence over shared refinement wording below. These instructions do not authorize changes to affinity.taste_band, other metrics, personality, speech or other records.

Update an existing `entry_ref` for the same character, target, and meaning. Never merge target-specific material into the character's general personality. Values and biases are separate from an interpretation of a particular target. Do not create a new first-impression entry every turn.

Mark a provisionally inferred profile as an `assessment` and preserve its evidence. Refine it when supported by actual settings or reactions, but never add a preference merely because it might be useful in a future scene. Never assume that attitude and interpretation changed at the same time.

Update target-specific values only under the slow cadence: a catalyst, or the same change across at least two distinct scenes in the nature of interest, intent, constraint handling, or approach and response. One conversation's warmth, coldness, teasing, or a single approach and its response is scene performance, not a changed value. Never transfer one character's private state into another character's knowledge. If a third party actually read a cue, connect it to that character's knowledge evidence.

Use only the mode-specific entries separately allowed for the current request. Never record a result in an unauthorized entry or a program-owned entry. Do not insert scores or bands into qualitative profiles and appraisals.

Do not reward a character merely for appearing. Distinguish past evidence used for an initial value from a new event, and never repeat an event already applied. Group new events from the same source turn once per policy and target. If the existing ledger value is unavailable or the target is ambiguous, report an `issue`; never initialize arbitrarily.
