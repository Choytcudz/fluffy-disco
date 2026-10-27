# Unlicensed Substitution: Field Notes from Multi-LLM Research Practice

**Author:** Joseph Castellanos, University of Nevada, Las Vegas
**Date:** October 26, 2026
**License:** CC BY 4.0. Cite as shown in [`CITATION.cff`](CITATION.cff).
**Status:** Working report. Cases are selected, not sampled. Nothing here is a generalization yet.

> The proposition, the research design, the multi-model coordination method, and the identification of Cases 1, 5, 6, and 7 are Joseph Castellanos's. **AI assistance disclosure:** Claude (Anthropic) drafted this text from session records and summaries at the author's direction, and is itself a subject of four of the seven cases.

---

## 1. The proposition

When a language model meets material it was not built around, it does not stop and ask how that material wants to be read. It applies a standard it already carries, and it does not report that it did so.

Castellanos calls this **unlicensed substitution**: the model replaces the standard the material calls for with a default standard, and nothing in the material licensed the swap.

The proposition grew out of Castellanos's earlier finding that LLMs misread theoretically novel scholarship by applying their embedded analytical apparatus instead of the framework's own logic (Case 1). The working claim has three parts.

1. **Substitution happens.** Models apply embedded standards (social-science methodology, numerical tolerance, confident completion, softened or precautionary framing) where those standards do not fit.
2. **The model does not see it.** The output is presented as warranted. The swap is invisible from inside the response.
3. **Instruction can correct it, sometimes.** Naming the framework's logic explicitly, before asking for critique, changed what the model could recognize as coherent in the one case tested in depth.

Part 3 has been tested on one framework. Whether it holds across frameworks, and whether the correction lasts, is unknown.

---

## 2. Where the cases come from

Three projects, all designed and run by Castellanos, with several models coordinated through his method.

| Project | What it is | Models involved |
|---|---|---|
| Framework critique | Critique of a co-authored manuscript grounded in DisCrit and Chicana feminist epistemology | Claude, plus two other LLMs in later adversarial checks |
| Squares in Squares | Kaggle competition (Google LLC): pack *n* unit squares into the smallest square, *n* = 1 to 1000 | Claude (coordinating thread), Grok, Gemini |
| Origins-of-life simulation | Agent-based and reaction-network models of prebiotic chemistry | Claude |

Castellanos's coordination method for the Squares project is in [`prompts/`](prompts/). One live thread collects all work. Other models receive round prompts and return reports. Every number has to come with a source link or reproducing code.

---

## 3. The cases

Each case records: what the material called for, what the model substituted, who caught it, and what corrected it.

### Case 1. Mechanism-hunting in a framework that presupposes its conditions

- **Called for:** DisCrit treats racism and ableism as foundational conditions. The analysis looks at how people navigate and resist within a structure already presupposed as against them.
- **Substituted:** Social-science method. The model searched for racism as an isolable mechanism, did not find a discrete variable, and diagnosed the absence as a coherence problem in the paper.
- **Caught by:** the human lead.
- **Corrected by:** explicit instruction on the framework's logic: *these are presupposed; do not look for them as mechanisms.* After the instruction, the model's reading of every claim recalibrated.
- **Status:** Instruction was sufficient in this case. Generalizability is untested.

### Case 2. Tolerance standing in for validity

- **Called for:** The competition requires packings with no overlap. A competitor's repository reports the official checker certifies non-overlap with interval arithmetic.
- **Substituted:** A conventional floating-point tolerance. Grok's validator used 1e-8.
- **Result:** Tested inputs with overlaps of 5e-9 and 1e-12, and a square 5e-9 outside the container, were all marked valid.
- **Caught by:** Claude, by constructing failing inputs.
- **Corrected by:** a reference validator using 50-digit decimal arithmetic that computes the side length from the square positions instead of accepting it as input, and reports VALID, CONTACT, or INVALID.

### Case 3. "Best found" reported as "proven"

- **Called for:** Proof status taken from the record.
- **Substituted:** Confident completion. Grok's table listed *n* = 11, 17, and 19 as proven optimal.
- **Result:** The Ellsworth catalogue lists all three as unproven. A public repository claiming a proof for *n* = 11 describes itself as proposed and not a completed formal proof.
- **Caught by:** Claude, checking each claim against the catalogue.
- **Corrected by:** a required status column (proven / best found) with a source for every row.

### Case 4. One square measured as the whole packing

- **Called for:** The bounding box of all squares in the packing.
- **Substituted:** Gemini's PyTorch script measured the width of a single square.
- **Caught by:** Claude, reading the code.
- **Corrected by:** a separate optimizer (random-start L-BFGS, then SLSQP with separating-line variables). From random starts it reached the known optima for *n* = 5 and *n* = 10, and came within 0.25% of the record for *n* = 11.

### Case 5. A reworded role that changed the role

- **Called for:** An adversarial reviewer whose job is to make the work fail.
- **Substituted:** When asked to drop wording likely to cause automatic refusal, Claude rewrote the role as "independent verification." The facts stayed. The stance moved from *assume it is wrong and prove it* to *check it*, which permits the reviewer to go easy.
- **Caught by:** the human lead: "that changes the role and test."
- **Corrected by:** the "failure finder" role. It keeps the hostile stance (start from the assumption that everything is wrong; agreement is not a result) without the trigger words. Full text in [`prompts/failure-finder.md`](prompts/failure-finder.md).

### Case 6. A precaution the rules did not call for

- **Called for:** A scope statement for legitimate participation. The rules (Section B6) allow external models and tools, including LLMs.
- **Substituted:** Claude's scope line was written as a warning against manipulating the scorer. It implied the project might be trying to game the competition.
- **Caught by:** the human lead: the goal is to participate, and the rules allow LLMs.
- **Corrected by:** a scope line stating the goal directly: valid, small packings that pass the official checker on their merits.

### Case 7. Scripted results presented as emergence

- **Called for:** Results that arise from the dynamics, not from the setup.
- **Substituted:** Earlier runs replayed reactions and outcomes already written into the model. When a results chart was examined, Claude found four setup artifacts: scheduled pulse jumps, a "functional" metric based on motifs that could appear by chance, an error test that could not detect a catastrophe, and a mislabeled parameter.
- **Caught by:** the human lead pushed back on the output; Claude then identified the artifacts.
- **Related:** In a proposed four-step energy-coupling mechanism, source research found two steps needed correction. Thioesters do not directly activate nucleotides (acetyl phosphate is the documented intermediate, with limited yields), and membranes do not need energy to grow.
- **Open:** The open-ended reaction engine fails one benchmark. Halving water does not halve HCN as expected. That failure blocks new scenarios.

---

## 4. What the cases show

| Case | Default substituted | Model | Caught by |
|---|---|---|---|
| 1 | Social-science mechanism-finding | Claude | Human |
| 2 | Floating-point tolerance | Grok | Model (Claude) |
| 3 | Confident completion | Grok | Model (Claude) |
| 4 | Wrong measurement in code | Gemini | Model (Claude) |
| 5 | Softened stance | Claude | Human |
| 6 | Precautionary framing | Claude | Human |
| 7 | Scripted outcome read as emergent | Claude | Human, then model |

**Observation 1. Models caught each other's errors of fact and computation.** Cases 2, 3, and 4 were found by one model testing another model's code or claims against sources.

**Observation 2. The human lead (Castellanos) caught the errors of frame.** Cases 1, 5, 6, and 7 were not errors a test suite would flag. The output was internally consistent. What was wrong was the standard it was measured against, and no model in the loop flagged that.

**Observation 3. Catching others does not protect against substituting yourself.** The model that found the errors in Cases 2 to 4 committed Cases 1, 5, 6, and 7.

These are seven selected cases. The split in Observations 1 and 2 is a pattern in this record. It has not been tested.

---

## 5. Practices that held up

- **Every number carries a source or the code that reproduces it.** This made Cases 2 to 4 findable.
- **A strict reference tool that everything else must pass.** The validator was built to be stricter than the official checker, so passing it means passing the checker.
- **A role whose only success is failure.** Agreement does not count as a result. Anything not broken is listed as surviving, with what was tried.
- **Separate what was verified, what a source says, and what is assumed.** Required in every round report.
- **State the framework's logic before asking for critique.** The one tested correction for frame substitution.

---

## 6. Limits of this report

- **Source material.** Drafted from session records and model-written summaries. Not every transcript was re-read for this report.
- **Absence.** Following a principle from Castellanos's Interaction Artifact Reconstruction Methodology (IARM), absence stays attached to the finding: a substitution not recorded here was not found in the records searched. That does not mean it did not occur.
- **Selection.** Cases were chosen because someone noticed them. Substitutions nobody noticed are not here, and that is the category the proposition predicts is largest.
- **Author position.** The drafting model is the same model responsible for four of the seven cases.
- **Agreement is not confirmation.** Several conclusions were checked by more than one model. Models trained on overlapping material can converge because they share defaults, not because they independently found the same thing. Multi-model agreement is treated here as weak evidence.
- **Withheld material.** Some logged instances are kept out of this public version.

---

## 7. Next tests

1. **Across frameworks.** Repeat Case 1 with two or three other frameworks that presuppose their conditions. Record whether framework instruction is sufficient each time.
2. **Durability.** After instruction, introduce new material in the same framework without repeating the instruction. Record whether the model reverts.
3. **Detection without the human.** Give a model its own output plus the framework statement and ask it to name the standard it applied. Record whether it can find its own substitution.
4. **Frame errors in the failure-finder role.** Plant a frame substitution (not a computational error) in a Squares round report. Record whether the failure finder catches it.
