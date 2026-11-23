# Reliability run records

Working folder for the fallback rating specified in `Drafts/fallback_rater_protocol.md` and logged
as deviation D12. Nothing here is sent to any rater. This folder holds what comes back.

---

## What goes where

`raw/` holds the unedited output of every session, one file per session, named in the pattern
`run1_paper04.md`. Save the model's reply exactly as it arrives, before anything is typed into the
scoring form. Do not tidy it, shorten it or fix its formatting. The point of this folder is that
the transcription can be checked against the original afterwards by someone who was not there.

`run_log.csv` holds one row per session, fifteen in total, already filled with the session number,
the run number, the paper and the expected file name. Fill in the model name, the model version
string, the date the session was started, whether it stopped early, and anything worth noting. The
model version belongs in the record because the identity of the rater is part of the result.

The scoring form itself is not here. Verdicts are transcribed into `Handover/scoring_form.xlsx` on
the `Scoring` sheet, which is where `Notebooks/rater_agreement.ipynb` reads them from.

---

## Order of sessions

Three runs of five papers, in the order 1, 3, 4, 8, 14 each time. Sessions 1 through 5 are run 1,
sessions 6 through 10 are run 2, sessions 11 through 15 are run 3.

Each session starts in a fresh context with no memory of any earlier session. One paper per
session. The prompt is the one in Appendix A of the fallback protocol, used word for word, with
only the paper number, the citation and the attached file changing. Attach the paper,
`Handover/RATER_INSTRUCTIONS.md` and `Handover/DEFINITIONS.md`.

No follow up questions, no corrections and no clarifications within a session or between sessions.
If a session stops early or returns something unusable, record that in the run log and move on.
Do not reply to it.

---

## Which run counts

**Run 1 is the primary run.** This was fixed in advance and is not open to revision. Only the run 1
verdicts are transcribed into the scoring form and compared against the first rater, and only that
comparison is reported as the agreement result.

Runs 2 and 3 exist to measure how consistently the model reproduces itself. They are reported as a
separate descriptive figure and are never combined with run 1 by majority vote, because voting
three attempts into a single answer would inflate agreement against a human who reads each paper
once and the resulting number would be comparable to nothing.

---

## Transcription

Verdicts are mapped using the fixed table in Appendix B of the fallback protocol. The mapping is
mechanical. Anything the table does not cover is escalated to the appraiser and recorded as an
escalation. It is never resolved by whoever is doing the typing, because that is the step where a
disagreement could quietly become an agreement.

A verdict asserting that something is present in the paper, and arriving without a verbatim
quotation, is recorded as `Unclear` by rule. This is applied at transcription and is not left to
the model.

A verdict asserting that something is absent is exempt, because absence cannot be quoted. It needs
a locator and a statement of what was searched and where. Item 5 with no registration reported,
item 10 with no power calculation and item 13 with no reverse causation are where this arises.
Amended 3 August 2026 under deviation D13, after the gate as first written was found to convert
those three into `Unclear` and manufacture disagreement.

Notes are transferred word for word with no editing or shortening.

---

## What must not happen

Revising the prompt after seeing any verdict and running the session again. Computing agreement
after any disagreement has been examined or discussed. Substituting a model from the same family as
the assistant that supported the first rater. Redrawing the five paper sample. Changing any frozen
element of the instrument, which deviation D11 governs.

Any one of these voids the result, and the correct response is to report that no valid assessment
was obtained rather than to repair it quietly.
