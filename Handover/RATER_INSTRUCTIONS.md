# Second Rater Instructions

Thank you for agreeing to do this. It should take about six hours, and it fixes the single
biggest weakness in the study.

---

## What this is

Fifteen published papers on artificial intelligence tools in medicine have been appraised
against a thirteen item rigor checklist. Every verdict so far was assigned by one person, which
means nobody knows how much of the result depends on that person's judgment.

You are rating five of those papers independently. The two sets of verdicts will then be
compared and an agreement statistic reported in the write up. Your ratings are not a check on
the first rater's work and they will not be corrected to match. Disagreement is data. If the
checklist turns out to be hard to apply consistently, that is a genuine finding and it gets
reported.

---

## What you must not look at

Independence is the whole point, so please do not open any of the following, and tell me if you
already have.

- The scoring tracker workbook, any sheet of it
- Any file in the `Drafts` folder
- The project README
- Any exported CSV
- Anything describing what the study expects to find

If you have already seen any of it, that is fine and not a problem, but say so, because it
changes how the agreement figure should be reported.

The rules in this document and in `DEFINITIONS.md` are shared with you deliberately. A
reliability study measures whether two people applying the same stated rules reach the same
verdicts. It does not measure whether two people independently invent the same rules. So the
conventions below are given to you in full, and the verdicts are not.

---

## The scale

Four categories. `Yes`, `No`, `Unclear`, `N/A`. Nothing else, and no numeric scale.

Record a separate confidence for each cell, `High`, `Medium` or `Low`. Confidence is not a
hedge on the verdict. Commit to a verdict, then say how sure you were. Cells you mark `Low` are
the interesting ones.

---

## Your five papers

| Paper | Domain | Citation |
| --- | --- | --- |
| 1 | Retinal | Zhou et al. 2023, Nature (RETFound) |
| 3 | Retinal | Abramoff et al. 2018, npj Digital Medicine (IDx-DR) |
| 4 | Colonoscopy | Kader et al. 2026, npj Digital Medicine 9:84 (EAGLE/CADDIE), doi 10.1038/s41746-025-02270-1 |
| 8 | Colonoscopy | Ladabaum et al. 2023, Gastroenterology |
| 14 | ECG | Liu et al. 2025, J Am Heart Assoc (CARDIOLOGIST) |

The PDFs are in `Handover/Papers/`. The numbering is not sequential because these five were
drawn at random from the fifteen, and the original numbers are kept so the two sets of ratings
line up.

That is sixty five cells in total, five papers by thirteen items.

---

## Before you score anything

Open each PDF and read page one. Confirm the first author, the journal, the year and the study
design against the table above. Two of the original files in this project turned out to hold a
different paper from the one the manifest named, so this check is now mandatory. If any of the
four fields disagrees, stop and tell me rather than scoring it.

One caution on the year, so that the check does not fire when nothing is wrong. A journal's digital
object identifier often carries the year the paper was accepted, which can be a year earlier than
the issue it finally appeared in. Match the year against the issue line or the running footer
rather than against the identifier, and treat a difference between those two as ordinary rather
than as a mismatch. Paper 4 is the one where this arises. Its identifier reads 2025 and its issue
line reads 2026, and the table above gives both so that you can see they agree.

---

## What to look at, item by item

| # | Item | What to look for | Where it usually lives | Decision rule |
| --- | --- | --- | --- | --- |
| 1 | External Validation | Evaluation on a dataset separate from the one used to fit the model, separated by site or by time | Methods, dataset description. Results, validation cohort table | `Yes` if a genuinely separate dataset is reported. `No` if only an internal split or cross validation. `Unclear` if separation is asserted but provenance is not described |
| 2 | Patient-Level RCT | The unit of randomisation | Methods, trial design. CONSORT diagram | `Yes` only if individual patients were randomised. `No` for cluster, stepped wedge, before and after, or no randomisation. Never `N/A` |
| 3 | Prespecified Endpoint | A primary endpoint fixed before enrolment opened | Methods, outcomes. Registry record | `Yes` if a registry entry or cited protocol fixes it. `Unclear` if the trial is unregistered. `N/A` if the paper has no trial arms |
| 4 | Prespecified Design | The design fixed before enrolment opened | Methods. Registry record | Same rule as item 3 |
| 5 | Registered w/ CT.gov | An NCT number, and registration before the first enrolment | Methods, often the final paragraph. Abstract | `Yes` if an NCT number is stated. `Unclear` if prospectively registered in another registry. `No` if no registration is reported |
| 6 | Transparent Reporting | The predictors and their relative importance | Methods, model description. Appendix. Supplementary material | `Yes` if predictors and their importance are reported. `No` if the model is described only as an architecture. `Unclear` if partial, for example saliency maps with no quantitative importance |
| 7 | Honest Impact Eval | Whether the abstract conclusion matches the effect actually observed | Abstract conclusion read against Results. Discussion. Limitations | `Yes` if the claim matches the result. `No` if overstated. `N/A` if the paper contains no impact evaluation at all |
| 8 | No Conflict of Interest | Whether any author or the study itself has a financial or ownership interest in the tool being evaluated | Declaration of interests. Funding statement. Author affiliations. Acknowledgements | `No` if an author is an employee, director, shareholder, patent holder or paid consultant of the tool's maker, or if the maker funded or sponsored the study. `Unclear` if such a relationship is plausible but cannot be established from this paper. `Yes` otherwise. Equipment loan alone does not count, and relationships with unrelated products do not count |
| 9 | Focus on Patient Outcomes | What the primary endpoint actually measures | Methods, outcomes. Abstract | Assign a tier using `DEFINITIONS.md`. `Yes` only at tier four. Never `N/A` |
| 10 | Adequate Sample Size | The power calculation, its assumed baseline rate, and the number actually enrolled | Methods, sample size. Results, CONSORT numbers | `Yes` if powered and the target was met. `No` if materially under enrolled or the assumed baseline was contradicted by the observed data |
| 11 | Intention-to-Treat | Whether every randomised participant was analysed as allocated | Methods, statistical analysis. Results, analysis population | `Yes` if all randomised participants are analysed as allocated. `No` if per protocol, or if post randomisation exclusions occurred |
| 12 | Balanced Table 1 | Comparability of the arms at baseline | Table 1 | `Yes` if the arms are shown and comparable. `N/A` if the paper has no arms |
| 13 | No Reverse Causation | Whether any input to the model is the outcome, or a proxy measured after it | Predictor list. Timing of measurement | `Yes` unless an outcome or a downstream proxy is used as a predictor |

---

## When `N/A` is allowed

`N/A` is not available whenever an item feels like a poor fit. It is permitted only where the
item's class allows it.

| Class | Items | `N/A` permitted when |
| --- | --- | --- |
| A | 2, 9 | Never. These two are the quantities the study measures |
| B | 3, 4, 5, 11, 12 | The paper has no trial arms |
| C | 7 | The paper contains no impact evaluation at all |
| D | 1, 6, 8, 10, 13 | Never. Scored for every paper regardless of design |

`N/A` is excluded from both the numerator and the denominator, so it never counts against a
paper. `No` and `Unclear` both do.

---

## When `Unclear` is the right answer

`Unclear` is a real verdict, not a way of skipping a cell. Two conventions are fixed.

Items 3 and 4 take `Unclear` rather than `No` when a trial is unregistered, because self
reported prespecification cannot be checked against anything.

Item 5 takes `Unclear` when a trial was registered prospectively but in a registry other than
ClinicalTrials.gov, because scoring it `No` would wrongly equate it with reporting no
registration at all.

---

## Five places where the obvious reading is wrong

These are reading techniques rather than answers. None of them tells you what any paper scores.

**Read the whole sentence around intention to treat.** The phrase is often qualified in the same
sentence by a second phrase that contradicts it. Whatever the text claims, reconcile the number
analysed against the number randomised in the CONSORT diagram and score on the numbers.

**A paper can follow a principle without naming it, and name it without following it.** Item 11
can be `Yes` in a paper that never writes the phrase, and `No` in a paper that does. Search for
the numbers, not the words.

**Cluster randomisation scores `No` on item 2.** This will feel harsh, and there is a reasonable
argument that cluster allocation is more rigorous for a tool that alerts a clinician rather than
treating a patient. Score `No` anyway and put your objection in the note. The convention is
fixed so that both raters apply it identically.

**Item 8 asks about independence, not disclosure.** A thorough declaration does not earn a
`Yes`. It is common in this literature for a paper to disclose, fully and honestly, that its
authors work for or hold shares in the company whose product is under test. That is a disclosed
conflict, and it is still a conflict. Read the declaration to find out whether an interest exists,
then score the interest rather than the quality of the disclosure. Note the specific relationship
either way.

**Check the sample size assumption against the observed data.** A power calculation rests on an
assumed baseline event rate. Find that assumption, then find what the control arm actually did,
and compare them before scoring item 10.

---

## Notes

One note per cell, in the note column. The standard is that a third person should be able to
reach the same verdict from your note alone, without reopening the PDF.

| Verdict | Note must contain |
| --- | --- |
| `Yes` | A locator. Section name or page number, and the sentence or table that settles it |
| `No` | A locator, plus a short quotation of the wording that fails the item |
| `Unclear` | A locator, plus which specific fact is missing and where you looked for it |
| `N/A` | The item class invoked and the design feature that triggers it |

Quote rather than paraphrase wherever the exact wording is the point. A couple of sentences per
cell is usually enough, and there is no length requirement.

Where a verdict was genuinely close, say so and say what the alternative was. Those cells are
the most useful ones in the whole exercise, because they are where the checklist is doing the
least work.

The form also has a free text box per paper for anything the thirteen items have no room for.

---

## Effort

Sixty five cells across five papers. Expect roughly an hour per paper, and closer to ninety
minutes for the two that are not straightforward randomised trials. About six hours in total.

You do not have to do them in one sitting or in order. Do finish a paper once you start it,
rather than scoring one item across all five papers, because judgment drifts differently when
you work down a column instead of across a row.

---

## What happens afterwards

Your ratings are compared against the existing ones and an agreement statistic is computed from
the independent verdicts, before any discussion between us. Then we go through every
disagreement together and reconcile it. Any verdict that changes as a result is changed on the
record with a note saying what it was before.

The agreement figure is computed once, from the independent ratings, and is never recomputed
after reconciliation. That is why it matters that you score everything before we talk.
