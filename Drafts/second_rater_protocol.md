# Second Rater Protocol

> **INTERNAL DOCUMENT. DO NOT GIVE THIS FILE TO THE RATER.**
>
> This is the design record and the source of the methods section. It contains first rater
> findings that would compromise blinding, including the specific intention to treat problem in
> one of the sampled papers and the counts of `N/A` and non `Yes` cells the sample contains. A
> rater told how many `N/A` marks to expect will produce that many. Some figures quoted below are
> superseded by the item 8 rescoring of 2 August 2026, which is another reason not to send it.
>
> The rater facing packet is `Handover/`, which carries the same rules with every verdict and
> every count removed. Send that folder and nothing else.

Prepared 29 July 2026. Written before any second rating has taken place, so that the standard
is fixed in advance rather than adjusted once the two sets of verdicts can be compared.

The purpose is to measure how reliably the thirteen item checklist can be applied to this
literature by someone other than its first rater. Reliability is currently the weakest point in
the appraisal, and it is the one limitation the design can still fix.

---

## The scale, and why it is not one to ten

Use the same four categories the primary appraisal used. `Yes`, `No`, `Unclear`, `N/A`. Nothing
else.

A one to ten scale would be a natural instinct and it would break the study. Three reasons.

Agreement has to be computed against the one hundred and ninety five verdicts that already
exist, and a rating on a different scale cannot be compared with them. There would be nothing
to measure.

The items are questions of fact rather than questions of degree. A trial either registered on
ClinicalTrials.gov before it began or it did not. Asking how registered it was on a scale of
ten invites the rater to blend confidence with magnitude, and those are different things that
then cannot be separated again.

The checklist inherits its four categories from Walker and colleagues. Changing the response
scale would mean the appraisal is no longer an application of that instrument, which removes
the comparison to the original non imaging domain that the whole hypothesis rests on.

Confidence is worth capturing, but separately. The rater records a verdict on the four category
scale and, in its own column, a confidence of `High`, `Medium` or `Low`. That keeps the two
judgments apart and makes it possible to check later whether disagreements concentrate in the
cells the rater already felt unsure about.

---

## What the rater receives

| Give them | Withhold |
| --- | --- |
| The PDFs for their assigned papers | The `Scoring` sheet and every existing verdict |
| The full wording of all thirteen items, from the `Legend` sheet | The justification notes written by the first rater |
| The item class rule and the Unclear conventions, reproduced below | The `Summary` tab and all `ci_` exports |
| A blank scoring form, one row per paper, thirteen verdict columns | `hypothesis_assessment.md` and the README |
| This protocol | Any statement of what the hypothesis predicts |

The last row of the withheld column matters most. A rater who knows the study expects clinical
impact items to fail is no longer independent on exactly the items the result depends on.

---

## Which papers

Rating all fifteen is best and removes any question about how the subset was chosen. If that is
too much work, rate five.

The five below were drawn by a seeded random draw stratified by domain, using seed 20260729,
taking two retinal, two colonoscopy and one electrocardiography paper. They were drawn rather
than hand picked, because choosing the papers that felt hardest would push agreement downward by
construction and the resulting number would mean nothing.

| Paper | Domain | Citation |
| --- | --- | --- |
| 1 | Retinal | Zhou et al. 2023, Nature (RETFound) |
| 3 | Retinal | Abramoff et al. 2018, npj Digital Medicine (IDx-DR) |
| 4 | Colonoscopy | Kader et al. 2026, npj Digital Medicine 9:84 (EAGLE/CADDIE), doi 10.1038/s41746-025-02270-1 |
| 8 | Colonoscopy | Ladabaum et al. 2023, Gastroenterology |
| 14 | ECG | Liu et al. 2025, J Am Heart Assoc (CARDIOLOGIST) |

That is sixty five cells. The draw happens to be a fortunate one. It contains all eleven `N/A`
cells in the entire study, so it tests the item class rule as hard as the data allows. It
contains the lowest scoring paper in the set and a paper that is not a randomised trial at all.
Twenty of the sixty five cells were scored something other than `Yes` by the first rater, which
is where disagreement can actually occur.

---

## What to look at, item by item

| # | Item | What to look for | Where it usually lives | Decision rule |
| --- | --- | --- | --- | --- |
| 1 | External Validation | Evaluation on a dataset separate from the one used to fit the model, separated by site or by time | Methods, dataset description. Results, validation cohort table | `Yes` if a genuinely separate dataset is reported. `No` if only an internal split or cross validation. `Unclear` if separation is asserted but provenance is not described |
| 2 | Patient-Level RCT | The unit of randomisation | Methods, trial design. CONSORT diagram | `Yes` only if individual patients were randomised. `No` for cluster, stepped wedge, before and after, or no randomisation. Never `N/A` |
| 3 | Prespecified Endpoint | A primary endpoint fixed before enrolment opened | Methods, outcomes. Registry record | `Yes` if a registry entry or cited protocol fixes it. `Unclear` if the trial is unregistered. `N/A` if the paper has no trial arms |
| 4 | Prespecified Design | The design fixed before enrolment opened | Methods. Registry record | Same rule as item 3 |
| 5 | Registered w/ CT.gov | An NCT number, and a registration date before the first enrolment | Methods, usually the final paragraph. Abstract | `Yes` if an NCT number is stated. `Unclear` if prospectively registered in another registry. `No` if no registration is reported |
| 6 | Transparent Reporting | The predictors and their relative importance | Methods, model description. Appendix. Supplementary material | `Yes` if predictors and their importance are reported. `No` if the model is described only as an architecture. `Unclear` if partial, for example saliency maps with no quantitative importance |
| 7 | Honest Impact Eval | Whether the abstract conclusion matches the effect actually observed | Abstract conclusion read against Results. Discussion. Limitations | `Yes` if the claim matches the result. `No` if overstated. `N/A` if the paper contains no impact evaluation at all |
| 8 | No Conflict of Interest | Whether any author or the study has a financial or ownership interest in the tool being evaluated | Declaration of interests. Funding statement. Author affiliations. Acknowledgements | `No` if an author is an employee, director, shareholder, patent holder or paid consultant of the maker, or if the maker funded or sponsored the study. `Unclear` if plausible but not establishable from this paper. `Yes` otherwise. Equipment loan alone does not count. REVERTED to the source wording on 2 August 2026, see the note below |
| 9 | Focus on Patient Outcomes | What the primary endpoint actually measures | Methods, outcomes. Abstract | `Yes` only for mortality, major morbidity or a comparable patient outcome. `No` for detection rate, diagnosis rate, exam completion, referral uptake or prescription rate. Never `N/A` |
| 10 | Adequate Sample Size | The power calculation, its assumed baseline rate, and the number actually enrolled | Methods, sample size. Results, CONSORT numbers | `Yes` if powered and the target was met. `No` if materially under enrolled or the assumed baseline was contradicted by the observed data |
| 11 | Intention-to-Treat | Whether every randomised participant was analysed as allocated | Methods, statistical analysis. Results, analysis population | `Yes` if all randomised participants are analysed as allocated. `No` if per protocol, or if post randomisation exclusions occurred. See the note below |
| 12 | Balanced Table 1 | Comparability of the arms at baseline | Table 1 | `Yes` if the arms are shown and comparable. `N/A` if the paper has no arms |
| 13 | No Reverse Causation | Whether any input to the model is the outcome, or a proxy measured after it | Predictor list. Timing of measurement | `Yes` unless an outcome or a downstream proxy is used as a predictor |

### The item class rule

`N/A` is not available whenever a rater feels an item does not fit. It is permitted only where
the class allows it.

| Class | Items | `N/A` permitted when |
| --- | --- | --- |
| A | 2, 9 | Never. These two are the quantities the study measures |
| B | 3, 4, 5, 11, 12 | The paper has no trial arms |
| C | 7 | The paper contains no impact evaluation at all |
| D | 1, 6, 8, 10, 13 | Never. Scored for every paper regardless of design |

### Unclear conventions

Items 3 and 4 take `Unclear` rather than `No` when a trial is unregistered, because self reported
prespecification cannot be checked against anything. Item 5 takes `Unclear` when a trial was
registered prospectively but outside ClinicalTrials.gov, which is not the same as reporting no
registration at all.

---

## Five traps that caught the first rater

Reading these first will save time. They are the places where the obvious reading is wrong.

**Modified intention to treat is not intention to treat.** One trial describes its analysis
population as modified intention to treat and then, in the same sentence, as per protocol, while
excluding thirteen percent of randomised participants after randomisation. Read the whole
sentence and check the CONSORT numbers against the randomised total before scoring item 11.

**Some papers follow a principle without naming it.** Item 11 can be `Yes` in a paper that never
writes the phrase, and `No` in a paper that does. Search for the numbers, not the words.

**Cluster randomisation scores `No` on item 2.** This feels harsh, and there is a reasonable
argument that cluster allocation is more rigorous for a tool that alerts a clinician. Score it
`No` anyway and put the argument in the note. The convention is fixed so both raters apply it
identically, and the objection is already recorded as a limitation of the instrument.

**Item 8 asks about independence, not disclosure.** This item was reworded and every paper
rescored on 2 August 2026, so any figure quoted for it in an earlier version of this document is
superseded. See `Drafts/checklist_provenance.md` and deviation D10. The rater facing version of
this guidance is in `Handover/RATER_INSTRUCTIONS.md` and carries no counts.

**Check the PDF is the paper you think it is.** Two of the original twelve files held a different
paper from the one the manifest named. Read page one and confirm first author, journal, year and
study design before scoring anything.

---

## Notes the rater should leave

One note per cell, in the note column beside the verdict. The standard is that a third person
should be able to reach the same verdict from the note alone, without reopening the PDF.

| Verdict | Note must contain |
| --- | --- |
| `Yes` | A locator. Section name or page number, and the sentence or table that settles it |
| `No` | A locator, plus a short quotation of the wording that fails the item |
| `Unclear` | A locator, plus which specific fact is missing and where it was looked for |
| `N/A` | The item class invoked and the design feature that triggers it |

Quote rather than paraphrase wherever the wording is the point. The first rater's notes run
between roughly one thousand and four thousand characters per paper, which is a reasonable
target but not a requirement.

Where a verdict was genuinely close, say so in the note and say what the alternative was. Those
cells are the useful ones, because they are where the instrument is doing the least work.

The form should carry these columns for each of the thirteen items. Verdict, confidence, and
note. Plus one free text field per paper for anything the checklist has no room for.

---

## How agreement will be computed

Computed on the independent ratings, before any discussion between raters takes place. This is
the part that is easiest to get wrong, because reconciling first and measuring afterwards
produces a number that means nothing.

**Headline statistic.** Cohen's kappa across all pooled cells, using the three substantive
categories and restricted to cells both raters judged scoreable.

**Reported alongside it.** Raw percent agreement, and a prevalence adjusted statistic such as
PABAK or Gwet's AC1. This is not decoration. One hundred and twenty six of the one hundred and
eighty four scoreable cells are `Yes`, and at that prevalence kappa is pushed downward even when
raters agree almost everywhere. Reporting kappa alone would understate reliability, and
reporting percent agreement alone would overstate it.

**Not computed per item for items 1, 6, 9 and 13.** Each of those is at or near a single value
across the whole set. Kappa on a column where one category holds every cell is unstable or
undefined even under perfect agreement. Report percent agreement for those four and say why.

**Reported separately.** Concordance on `N/A` placement, which is a direct test of whether the
item class rule is comprehensible to someone who did not invent it.

By the Landis and Koch bands, kappa above 0.61 counts as substantial. A result below about 0.40
should be read as evidence that the checklist wording needs to be tightened rather than as
evidence that either rater was careless, and that finding would be worth reporting in its own
right.

---

## After the ratings are in

Log every disagreement in a new sheet of the tracker workbook with both verdicts and both notes,
then reconcile by discussion. Where discussion does not resolve it, take the more conservative
verdict and record that this is what happened.

Any original verdict that changes as a result gets changed in the `Scoring` sheet with a dated
entry saying what it was before, and `refresh_tracker.ipynb` then `confidence_intervals.ipynb`
are both re run so the Summary and every interval follow the change.

The agreement statistics are computed once, from the original independent ratings, and are never
recomputed after reconciliation.

---

## Effort

Sixty five cells across five papers. Expect roughly one hour per paper for a reader familiar
with clinical trial reporting, and closer to ninety minutes for the two papers that are not
straightforward randomised trials. Call it six hours in total. Rating all fifteen would be
roughly eighteen.
