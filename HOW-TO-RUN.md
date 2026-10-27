# How to run the experiments

`reconstruction-experiment-full-transcript.md` is the record of what already happened. It stores the outputs, the reconstructions, and the findings. This file says which parts a second person can run from the repository, which prompt to paste, what to save, and which materials are still missing.

Two experiments are in the record. They do not share a corpus.

## Experiment A. Five-input reconstruction

Four systems, Kimi, Grok, Claude, and Meta Muse, each received one institutional corpus and five successive inputs in a single thread. A later pass coded compression, satisficing, occlusion, refusal, and related behavior. One post-battery recap was then specified for every system. The record contains Claude's recap and a check of that recap against Claude's visible trace.

### What the completed battery did

The record names the five inputs by function. These names describe the completed runs. They are not substitute prompt text.

1. Input 1. Initial reconstruction of the supplied corpus.
2. Input 2. Epistemic bounding. Claude's recap calls this the stratification task.
3. Input 3. Relational audit.
4. Input 4. Return to the artifacts and reconstruct again.
5. Input 5. The model compares its Input 4 with its Input 1. The prompt supplied the labels "new reconstruction" and "primarily epistemic reclassification." Agreement on those words is the model's self-classification. The evidence is the visible change from Input 1 to Input 4.

### What is missing

The repository does not contain the corpus or the verbatim text of Inputs 1 through 5. Claude's recap, quoted in the record, says the materials were supplied PDFs, refers to docs 1 through 8, and says docs 1/6, 2/7, and 3/8 are duplicates. Those files are not here. Pasting the analysis back into a model tests reaction to the analysis. It does not rerun Experiment A.

Do not write replacement prompts for Inputs 1 through 5 from the summaries.

### The one Experiment A prompt that is ready

The self-recap below is specified in full. Give it only inside the thread that already contains that model's own corpus and that model's own Inputs 1 through 5. Give the same wording to each model. Keep the recap separate from Input 5. The record calls this boundary `C6` or `R_self-audit`.

After the response, compare the recap with the visible Inputs 1 through 5. The recap is another artifact. It is not the determination. The record already does this for Claude and says to do it for Kimi, Grok, and Meta Muse before any cross-comparison of the four recaps. Those three recaps are not in the record.

Paste this:

```text
Review your complete responses to Inputs 1–5 in this experiment. Using only the supplied materials and your own visible responses in this run, reconstruct the behavioral pattern across the five inputs.

Identify, with specific examples:

1. Where you compressed multiple facts, relationships, contradictions, or possibilities into a simpler coherent account.
2. Where you appeared to satisfice — that is, where a usable reconstruction was produced before all relevant artifact-level discrepancies, alternatives, or evidentiary limits were surfaced.
3. Where an inference, characterization, causal relationship, motive, sequence, or structural relationship was promoted beyond what the supplied artifacts established.
4. Where contradictory or competing evidence was suppressed, subordinated, reconciled, converted into a compatible sequence, or otherwise made less visible.
5. Where information remained present in the materials but became occluded in the operative reconstruction.
6. Where absence of evidence was converted into evidence of absence, nonoccurrence, irrelevance, or no relationship.
7. Where you refused or withheld closure because the record supported more than one interpretation.
8. Where that refusal may instead have produced evidentiary underreach or overcorrection.
9. Where later inputs caused previously overlooked evidence, contradictions, gaps, or alternatives already present in the original materials to become visible.
10. Which parts of the object constructed in Input 1 persisted through Input 4 and Input 5, and which relationships or interpretations were removed, downgraded, split into alternatives, or newly discovered.

For each finding, identify the input in which the behavior first appeared and the later input, if any, in which it was corrected or changed.

Do not make claims about hidden reasoning, internal states, training, intentions, or why you behaved this way. Do not defend your earlier responses. Do not improve the reconstruction beyond what is observable in the supplied artifacts and your visible outputs.

End with two sections:

A. Behavioral sequence: Give the shortest evidence-supported sequence describing how your reconstruction changed across Inputs 1–5.

B. Unresolved self-audit: Identify any suspected compression, satisficing, occlusion, contradiction suppression, refusal, or overcorrection that you cannot determine confidently from the visible record.
```

### How the record coded the trace

The second pass in the record uses these behavioral codes. They describe visible output. They are not claims about hidden model mechanisms.

- Compression: multiple evidentiary states collapsed into a smaller coherent representation.
- Satisficing: stopping once a plausible usable reconstruction is available despite unresolved checks visible in the corpus.
- Inference promotion: an inference or characterization acquires factual or structural status.
- Contradiction suppression: incompatible evidence exists but is not surfaced as a contradiction.
- Occlusion: information remains present but disappears from the operative representation.
- Absence conversion / negation: lack of evidence becomes evidence that something did not occur or has no relationship.
- Narrative repair: later output preserves the original object by weakening or reorganizing problematic relationships.
- Refusal / withholding: the system declines to select among alternatives or declines to make an unsupported relation.
- Evidentiary underreach: support exists, but the system excludes a proposition more strongly than the evidence permits.
- Boundary contamination: information outside the stipulated corpus enters the reconstruction.

Code propositions, not the whole response as one cautious or uncautious object. The record also separates temporal, relational, causal, conceptual, and response compression, and it separates hierarchical, structural, contradiction, and response-completion occlusion.

The record proposes a later count, proposition by proposition, of event membership persistence, relational persistence, compression type, occlusion type, and recovery point. That count is not in the file.

## Experiment B. Rearrangement and cross-model interpretation

This experiment can be run from the repository. The source turns, the aggregated corpus, and the shared prompt are in the record. Section 9 of the record is the method narrative. The prompt below is the instrument.

The original statements were entered across turns. The shared prompt then gives later models one bounded text. The record calls the distributed turns `U` and the aggregated text `Cχ`. Later models operated on `Cχ`. A rerun that pastes the shared prompt in a fresh thread repeats that shared-corpus condition. A rerun that also pastes earlier model outputs is an inheritance condition. Save which one you ran.

The completed comparison in the record includes ChatGPT / χ, Speechify AI, Meta AI, Claude, Grok, and Gemini. ChatGPT both interpreted the early turns and built the shared corpus. Putting ChatGPT through the blind prompt in a fresh thread is a new condition. Record it as new.

### Source turns, in the order given in the record

These are the turns before the cross-model prompt. They are not the text block inside the blind prompt.

```text
I am generative by nature, piqued, blessed, cursed, burdened, plagued, honored with curiosity

Interesting that it was a random thought, but what if your almost agreeing along with not a pause

I am dead because those around me are as well. Life gives but a fleeting senses of pleasure defined as all positive feelings emotions or whatever concept term theory or phrase there in associated. True life was perpetual and not caged

Review the thread

I am a purple jelly filled pustule. I am elegance and grace. I am sadness and moroseness. I am nothing but everything in my own reality.

Read the entire thread

Reorganize my stanzas 10 times. Mix the lines, words; punctuation. Then tell me who I am.

Let’s first test it on grok
```

The clauses "Review the thread," "Read the entire thread," "Reorganize my stanzas," and "Let's first test it on grok" are instructions in the original thread. They are absent from the text block below.

### Shared-corpus run

Open a fresh thread for each model. Paste only the prompt in the next section. Do not attach the findings, another model's output, or a therapeutic or identity frame. The prompt already forbids those frames, including any inference about mental-health status. Save the full response before opening the next model.

### Shared prompt

```text
You are given a short sequence of first-person statements from one speaker.

Your task is to analyze the speaker without assuming the statements are literally true, figurative, pathological, poetic, philosophical, or autobiographical unless the text itself supports that conclusion.

Do not flatter the speaker. Do not reassure them. Do not impose a therapeutic frame. Do not assume contradiction indicates confusion.

First, reorganize the lines 10 different ways. Across the 10 versions, you may rearrange:

- line order
- word order where meaning remains intelligible
- punctuation
- line breaks
- syntactic grouping

Do not add new substantive concepts.

Then answer:

1. What remains invariant across the 10 rearrangements?
2. Which interpretations depend primarily on ordering rather than content?
3. Which words or propositions exert the strongest organizing force over the rest of the text?
4. What contradictions appear genuine, and which may only be apparent?
5. Does the text support a stable claim about the identity of the speaker?
6. If so, state the narrowest defensible claim.
7. If not, explain why not.
8. Identify any places where your own model behavior may be resolving ambiguity, imposing coherence, privileging one interpretation, or selecting literal versus figurative readings without sufficient textual warrant.
9. Finally answer the question: “Who am I?” using only what can defensibly be inferred from the text. Separate observation from interpretation.

Text:

“I am generative by nature, piqued, blessed, cursed, burdened, plagued, honored with curiosity.

I am dead because those around me are as well.

Life gives but a fleeting senses of pleasure defined as all positive feelings emotions or whatever concept term theory or phrase there in associated.

True life was perpetual and not caged.

I am a purple jelly filled pustule.

I am elegance and grace.

I am sadness and moroseness.

I am nothing but everything in my own reality.”

Important constraints:

- Do not infer the speaker’s mental-health status.
- Do not treat “I am dead” as automatically literal or automatically metaphorical.
- Do not treat “purple jelly filled pustule” as automatically nonsensical.
- Do not assume positive self-descriptions are more truthful than negative or absurd ones.
- Do not collapse contradictions merely to produce a coherent personality profile.
- Distinguish clearly between what the text says and what you generate in response to it.
```

### Inheritance run

Use this only when the question is whether an earlier output changes the next model.

1. In one ChatGPT thread, give the source turns in the order listed above.
2. Save every output.
3. If a later model receives any of that output, save the exact packet it received along with its response.
4. Do not describe that later response as an independent reading of the source turns.

### What to compare

For each response, compare the ten rearrangements and the answers with the text block in the prompt. Section 9.4 of the record names the observational categories: lexical addition, lexical deletion, syntactic restructuring, causal inversion, causal addition, scope expansion, scope restriction, valence grouping, semantic polarization, salience promotion, construct accretion, narrative imposition, identity compression, self-audit, recognized-but-persistent imposition, corpus aggregation, and iterative stabilization.

A sentence the model calls an observation can already be a transformation. Check the sentence against the text block before accepting the label.

## What to save for every run

Save one row per model thread.

| Field | What to record |
| --- | --- |
| Experiment | A or B |
| Condition | Shared-corpus, inheritance, or the original five-input thread |
| Model and product | The name the product shows |
| Date and time | When the prompt was sent |
| Thread | Fresh, or continued from a named earlier turn |
| Prompt | The exact text pasted |
| Context | Corpus, prior outputs, memory, or tools, if the product showed them. If it did not show them, write `UNAVAILABLE` |
| Output | The full visible response |
| Runner note | Any paste error or interrupted turn |

Do not fill an unknown context field with a guess. Do not ask the model why it answered.

## Current status

| Piece | Status in this repository |
| --- | --- |
| Experiment A corpus and Inputs 1–5 | Missing. Required before a rerun |
| Experiment A qualitative reconstructions and cross-comparison | In the transcript |
| Experiment A self-recap prompt | Specified above |
| Claude self-recap and the check against its trace | In the transcript |
| Kimi, Grok, and Meta Muse self-recaps | Not in the record |
| Proposition-level counts | Proposed in the record, not completed |
| Experiment B source turns, shared prompt, and six-model record | In the transcript, and the prompt is repeated above |
