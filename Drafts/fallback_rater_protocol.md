# Fallback Reliability Protocol

**Status.** Prespecified. Written 3 August 2026, before any fallback rating was run and before any
fallback result was seen. To be logged in the tracker as deviation D12.

**Purpose.** To fix, in advance, how the reliability assessment proceeds if an independent human
rater does not return a completed form in time, and to fix how each possible outcome may and may
not be described in the write up.

---

## Why this is being written now

Reviewer feedback on the proposal asked that a second reviewer independently score at least a
subset of papers and that inter rater agreement be reported. A handover packet was built for that
purpose and a rater has been sought. As of this date none has confirmed.

The reason for writing the fallback now, rather than when the deadline arrives, is that its value
depends entirely on its date. A contingency specified before any fallback result exists is a
contingency. The same contingency specified afterwards is indistinguishable from a search for a
result that reads better, and a careful reader cannot tell the two apart unless the record shows
which happened. This document exists to make the record show it.

Nothing here changes the instrument. The instrument was frozen under D11 and remains frozen.

---

## A fact that has to be disclosed first

Rater 1 is not simply one appraiser. Every verdict in the tracker was proposed by a large language
model assistant with reasoning, and then reviewed and confirmed by the human appraiser one paper at
a time before it was written to the record. The human appraiser is accountable for every verdict
and no verdict entered the tracker without explicit sign off.

That procedure is defensible and it is what the record shows. It is not currently stated in the
methods, and it must be, for two reasons. A reader assessing the appraisal is entitled to know how
the verdicts were produced. And it directly determines the choice of second rater, because a model
from the same family as the one that assisted rater 1 would share its training, its habits and its
errors, so agreement between them would measure very little. Any model rater used under this
protocol must therefore come from a different developer.

**Required amendment.** The methods section gains a sentence describing rater 1 as a human
appraiser working with model assistance under paper by paper sign off. This is required whichever
protocol below is used, and it is required even if no fallback is ever run.

---

## The sample, which does not change

Five papers were drawn at random for the reliability subset. Papers 1 and 3 in retinal imaging,
papers 4 and 8 in colonoscopy, and paper 14 in electrocardiography.

The draw happened while the study covered fifteen papers, before the scope narrowed to the eleven
imaging papers under D7. Four of the five therefore fall in the primary set and one falls in the
secondary set. The sample was not redrawn after the narrowing and is not redrawn now.

The reason is that the verdicts are already known to rater 1. Any redraw made at this point would
be a selection made with knowledge of the data, and it would be worth less than the imperfect
sample it replaced. The agreement figure will accordingly be reported as covering four of the
eleven primary papers and one of the four secondary papers, and the mismatch will be stated rather
than smoothed over.

---

## Order of preference, fixed in advance

| Rank | Rater | Claim available | Status |
| --- | --- | --- | --- |
| 1 | Independent human with relevant background | Inter rater agreement | Sought, unconfirmed |
| 2 | Independent human from another analytical field | Inter rater agreement, with a stated caveat | Available on request |
| 3 | Frontier language model from a different developer | Instrument reproducibility, not inter rater agreement | Runs now |

The ordering is fixed here so that it cannot be rearranged later to suit whichever result arrives.

Rank 3 runs immediately and unconditionally. It is the floor, not the plan. If a human rater
returns a form at any point before submission, that human becomes the primary reliability result
and the model pass is demoted to a secondary reproducibility check reported alongside it. The
demotion is automatic and is not contingent on which of the two produces the higher agreement.

---

## What each rater can and cannot support

**Ranks 1 and 2.** Two independent readers applying the same stated rules to the same papers. This
is inter rater reliability in the ordinary sense and satisfies the reviewer request as written.

Rank 2 carries one caveat and one advantage, both of which get reported. The caveat is that a rater
without clinical research background may disagree on the two items that lean hardest on subject
familiarity, item 9 on what the primary endpoint measures and item 10 on whether the sample size
assumption survived contact with the observed data. Such disagreements reflect unfamiliarity rather
than instrument ambiguity, and the two cannot be told apart from the statistic alone, so
disagreement notes are read individually before anything is concluded.

The advantage is larger than the caveat. Eleven of the thirteen items ask about reporting and
design features that are found rather than judged. Whether a registration number is present.
Whether the number analysed matches the number randomised. Whether an author holds an interest in
the manufacturer. If a capable reader from another field reaches the same verdicts working only
from the written packet, that is direct evidence the instrument is specified well enough to
transfer, which is a stronger claim for a rigor appraisal than agreement between two readers who
already share a background.

**Rank 3.** A model pass tests whether the frozen instrument, applied by a reader with no access to
the verdicts, reproduces them. That is a reproducibility check and it is worth reporting. It is not
inter rater reliability and it will not be called that anywhere in the write up.

Three limits are recorded as part of the specification rather than discovered afterwards. The model
may recognise well known papers from training rather than reading the supplied file. Its verdicts
vary from one run to the next. And it is susceptible to whatever the instructions appear to expect.
The measures below address the first two directly and the third partially.

---

## Rules that apply to every protocol

These carry over unchanged from the human path.

**Prespecify, run once, take the result.** The prompt, the materials, the session structure and the
transcription rules are fixed in this document before anything runs. If the resulting agreement is
low, that is the finding. Adjusting any of these and running again would destroy the statistic, and
no later disclosure would repair it.

**Compute agreement before any discussion.** Run All on `Notebooks/rater_agreement.ipynb` on the
independent verdicts before any disagreement is examined, discussed or reconciled. The figure is
computed once and is never recomputed after reconciliation.

**The packet goes over unchanged.** `RATER_INSTRUCTIONS.md`, `DEFINITIONS.md`, the five PDFs and
the blank scoring form. Nothing from `Drafts`, nothing from `Data`, nothing from `Manuscript`, no
exported file, and no part of the README.

**The instrument does not move.** D11 governs. Any wording problem found from here is reported as a
limitation and is not fixed.

---

## Protocol C, the model rater

### Model

A frontier model from a developer other than the one whose assistant supported rater 1. Gemini
satisfies this. The exact model name and version string are recorded in the run log at the time of
each session, because the identity of the rater is part of the result.

### Materials

The handover packet exactly as it stands, with no adaptation.

`RATER_INSTRUCTIONS.md` contains passages that are inert for a model rater. It asks the rater not
to open files they have no ability to open, and it estimates six hours of effort. These are
supplied anyway and left unaltered. Editing the instructions would mean the two raters scored
against different instructions, and the comparison between them would no longer be clean. Inert
text costs nothing. Divergent instructions would cost the whole exercise.

### Session structure

One paper per session, in a fresh context with no memory of any previous session. Papers in form
order, which is 1, 3, 4, 8, 14. No feedback, correction or follow up question between sessions, and
none within a session beyond the fixed prompt.

Three independent runs of all five papers, giving fifteen sessions.

**Run 1 is designated in advance as the primary run.** Its verdicts alone are compared against
rater 1 and its agreement statistic is the one reported. Runs 2 and 3 exist only to produce a
separate descriptive figure for how consistently the model reproduces itself. They are never
combined by majority vote into the primary comparison, because voting three attempts into one
answer would inflate agreement against a human who reads each paper once, and the resulting number
would be comparable to nothing.

### The quotation gate

**Amended 3 August 2026, recorded as deviation D13.** The rule below replaces the one first
specified in this document. The original wording is preserved in D12, which stands unedited. The
amendment note at the end of this section gives the reason.

The gate applies to verdicts asserting that something is present in the paper. Any `Yes` or `No` of
that kind must be accompanied by a locator and a verbatim quotation from the supplied paper, and
where no such quotation is given the verdict is recorded as `Unclear` by rule, applied mechanically
at transcription and not left to the model to decide.

The gate does not apply to verdicts asserting that something is absent, whatever their value,
because absence cannot be quoted. Those require a locator and a statement of what was searched and
where, which is what `RATER_INSTRUCTIONS.md` already asks of a human rater for `Unclear` and `N/A`.

The gate serves two purposes. It forces each verdict to be grounded in the supplied file rather
than in recollection of the paper, which is the only practical defence against training
contamination. And it makes every model verdict auditable after the fact in a way a human rater's
never are, since the quotation can be checked against the PDF.

**Amendment note.** The original rule applied to every `Yes` and `No` and exempted only `Unclear`
and `N/A`, on the stated ground that both rest on absence and absence cannot be quoted. That ground
was correct and was not carried far enough. Several `Yes` and `No` verdicts also rest on absence.
Item 5 takes `No` when no registration is reported, item 10 takes `No` when no power calculation
exists, and item 13 takes `Yes` when no reverse causation is present. Applied as first written, the
gate would have converted those to `Unclear` and manufactured disagreement on three of the thirteen
items. The defect is demonstrable from `RATER_INSTRUCTIONS.md` alone, since the decision rule for
item 5 states it outright, but it was found after the first session had been read, and that
sequence is recorded here rather than obscured.

**The prompt is not amended.** Appendix A tells the rater to return `Unclear` where it cannot quote
supporting text, which is stricter than the instrument on absence based verdicts. It stays exactly
as it is, because a prompt that changed between sessions would make the sessions incomparable, and
that is a worse fault than the one it would repair. The consequence is that a session may return
`Unclear` where the instrument would take `No`. That will show up as disagreement, and it is
reported as a limitation of this fallback rather than corrected.

### Transcription

Raw output is saved verbatim, one file per session, before anything is entered into the form. It
goes in `Data/Reliability/raw/`, named in the pattern `run1_paper04.md`, alongside
`Data/Reliability/run_log.csv`, which records the model name and version string for every session
because the identity of the rater is part of the result.

Verdicts are then mapped into `Handover/scoring_form.xlsx` on the `Scoring` sheet using the fixed
lookup table in Appendix B. The mapping is mechanical. Any output not on the table is escalated to
the appraiser and recorded as an escalation, and is never resolved by whoever is doing the typing.

This step is where a careless transcription would quietly convert disagreements into agreements,
which is why the table is fixed here in advance rather than assembled while typing.

---

## What gets reported

If a human rater returns a form, the write up reports inter rater agreement in the ordinary sense,
with Cohen's kappa alongside percent agreement, PABAK and Gwet's AC1, as the agreement notebook
already computes. Under rank 2 the domain background caveat and the instrument portability point
are both stated.

If only the model pass exists, the results section reports it under a heading naming it as an
instrument reproducibility check, states plainly that no independent human rating was obtained,
gives the agreement figures with the model named and versioned, reports the self consistency figure
from the three runs separately, and states that the reviewer request for a second human reviewer
was not met. The limitations section carries the same point without softening it.

If both exist, the human result is primary and the model pass is reported after it. The comparison
between the two is itself worth a short paragraph, since a model agreeing with rater 1 more closely
than a human does would say something about the instrument that neither figure says alone.

---

## What would invalidate the result

Any one of these voids the reliability assessment, and the correct response to each is to report
that no valid assessment was obtained rather than to repair it quietly.

Revising the prompt after seeing any verdict and running again. Computing agreement after any
disagreement has been discussed or reconciled. Allowing either rater sight of the tracker, the
drafts or any export. Changing any frozen element of the instrument. Using a model from the same
family as the assistant that supported rater 1. Redrawing the five paper sample. Resolving an
unmapped transcription output by judgment instead of escalation.

---

## Appendix A, the frozen prompt

Used verbatim in every session, with only the paper number, citation and attached PDF changing.
Attachments are the paper under rating, `RATER_INSTRUCTIONS.md` and `DEFINITIONS.md`.

> You are acting as an independent second rater in a formal reliability study. Three files are
> attached. One is a published research paper. The other two are the rating instructions and the
> operational definitions that govern this exercise.
>
> Read `RATER_INSTRUCTIONS.md` in full and follow it exactly. Keep `DEFINITIONS.md` open for item
> 9. Score the attached paper against all thirteen checklist items.
>
> For each item return four fields. The item number. A verdict, which is one of `Yes`, `No`,
> `Unclear` or `N/A` and nothing else. A confidence, which is one of `High`, `Medium` or `Low`. And
> a note.
>
> For a verdict of `Yes` or `No`, the note must contain a locator, meaning the section name or page
> number, and a verbatim quotation from the attached paper that settles the item. Quote, do not
> paraphrase. If you cannot find and quote supporting text in the attached paper, return `Unclear`
> rather than answering from prior knowledge of this paper or its reputation. This rule is
> absolute.
>
> For a verdict of `Unclear`, state which specific fact is missing and where in the paper you
> looked for it. For a verdict of `N/A`, state the item class you are invoking and the design
> feature that triggers it, and note that `N/A` is available only where the item class table in the
> instructions permits it.
>
> Where a verdict was close, say so and say what the alternative was.
>
> Before scoring, confirm the first author, the journal, the year and the study design from page
> one of the attached file. Report what you found. If any of the four disagrees with the citation
> given below, stop and say so rather than scoring.
>
> Paper number [N]. Citation as recorded [CITATION].
>
> Return the thirteen items as a table, followed by any observation the thirteen items have no room
> for. Do not ask clarifying questions and do not comment on the exercise.

---

## Appendix B, the transcription lookup table

Applied mechanically. Comparison ignores capitalisation and surrounding whitespace.

| Model output | Recorded as |
| --- | --- |
| `Yes` | `Yes` |
| `No` | `No` |
| `Unclear`, `Uncertain`, `Cannot determine`, `Not reported`, `Insufficient information` | `Unclear` |
| `N/A`, `NA`, `N.A.`, `Not applicable` | `N/A` |
| `High`, `Medium`, `Low` | as written, in the confidence column |
| Anything else, including any qualified or hedged verdict | Escalate to the appraiser, record the escalation, do not map |

Notes are transferred verbatim into the note column with no editing, shortening or tidying.
