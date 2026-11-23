# Methods

Draft 2 August 2026. Figures are current as of the instrument freeze recorded that day.

---

## Design

This is a targeted rigor appraisal rather than a systematic review. A defined set of published
papers describing imaging based artificial intelligence tools was identified through a prespecified
search, and each paper was scored against a fixed thirteen item checklist. The term systematic
review is deliberately not claimed. The protocol named two secondary databases that were not
searched, and it was frozen after ten of the fifteen papers had already been scored, so both
shortfalls are reported in the limitations rather than absorbed into a stronger label. The unit of
analysis is the paper by item cell, and the outcome is the proportion of papers satisfying each
item.

The study tests two claims stated in the proposal before any appraisal was carried out. First,
that these papers score well on the items asking whether the model works and poorly on the items
asking whether it helps patients. Second, that the distance between those two groups is wider in
imaging than in the domain where the checklist was first applied.

---

## The instrument

### Source

The checklist is the thirteen item appraisal instrument taught in Module 9 of the course, held at
`Refs/Lecture 9A Slides.pdf`. The items appear as a table on slide 3, repeated unchanged on slide
31, under the heading "Feature of the AI Project and Evaluation Approach" beside a second column
headed "Our Typical Approach". The lecture applies the instrument to a single exemplar, the CLOT
trial of a paediatric venous thromboembolism prognostic model, reported across three papers and
marked as satisfying all thirteen items.

All thirteen items are reproduced from that source in the same order. None was added, dropped or
reordered. Where the wording used here is longer than the slide, the additional wording is drawn
from the lecture's own explanatory slides and is cited item by item in
`Drafts/checklist_provenance.md`. One elaboration, the phrase "external temporal or geographic" in
item 1, is this study's own gloss and is declared as such.

### Items

| # | Item |
| --- | --- |
| 1 | External validation of the model |
| 2 | Pragmatic patient level randomised controlled trial of impact |
| 3 | Prespecified primary endpoint |
| 4 | Prespecified study design |
| 5 | Registered with ClinicalTrials.gov |
| 6 | Transparent reporting of the model, as opposed to black box or proprietary |
| 7 | Honest, rigorous evaluation of the impact published |
| 8 | Clear of any conflict of interest |
| 9 | Focus on improving patient outcomes |
| 10 | Sufficiently large sample size |
| 11 | Analysis based on the intention to treat principle |
| 12 | Two study arms are balanced in Table 1 |
| 13 | Avoided reverse causation or data leakage |

### Response scale

Each item takes one of four verdicts. `Yes`, `No`, `Unclear`, `N/A`. No numeric or ordinal scale
was used, because the items are questions of fact rather than of degree and because a numeric
scale would blend confidence with magnitude in a way that cannot afterwards be separated.

`Yes` counts in the numerator and the denominator. `No` and `Unclear` count in the denominator
only, so both lower a rate. `N/A` is excluded from both and therefore never counts against a
paper.

### When N/A is permitted

Marking an item `N/A` because a paper's design does not reach it is superficially fair and, for
two items, destroys the quantity under study. If only papers that ran an impact trial are scored
on whether they ran an impact trial, the denominator collapses onto exactly the papers that pass.

Items were therefore assigned to four classes, and `N/A` is available only where the class permits
it. This rule was adopted at the third paper scored and applied to every paper thereafter and
retrospectively to the first two.

| Class | Items | `N/A` permitted when |
| --- | --- | --- |
| A | 2, 9 | Never. These two are the quantities under study |
| B | 3, 4, 5, 11, 12 | The paper has no trial arms |
| C | 7 | The paper contains no impact evaluation at all |
| D | 1, 6, 8, 10, 13 | Never. Scored for every paper regardless of design |

### When Unclear is used

`Unclear` is a substantive verdict rather than missing data. Two conventions were fixed in advance
of the papers to which they applied.

Items 3 and 4 take `Unclear` rather than `No` when a trial is unregistered, because self reported
prespecification cannot be checked against any external record.

Item 5 takes `Unclear` when a trial was registered prospectively in a registry other than
ClinicalTrials.gov, because scoring `No` would wrongly equate prospective registration elsewhere
with reporting no registration at all.

### Operationalising item 9

Item 9 asks whether the endpoint is a genuine patient outcome. Applied to this literature a binary
reading proved to conceal a distinction, because endpoints fail the item at four different
distances from the patient. Every primary endpoint was therefore assigned to one of four tiers,
and item 9 scores `Yes` only at tier four.

| Tier | Definition | Item 9 |
| --- | --- | --- |
| 1 | Model performance metric, a property of the classifier computed outside any care pathway | `No` |
| 2 | Process measure, what the health system or clinician did | `No` |
| 3 | Surrogate or intermediate clinical finding, located in the patient but not experienced by them | `No` |
| 4 | Patient outcome, an event or state the patient experiences | `Yes` |

The operative test for tier four is whether the patient would experience the thing if nobody told
them about it. Two rulings follow. Diagnosing a disease is tier three, because a diagnosis changes
what is known about a patient rather than what happens to them. A model performance metric remains
tier one even when the predicted target is a genuine outcome, because predicting an outcome is not
measuring one.

Item 9 is scored on the primary endpoint alone. Composite and co primary endpoints take the lowest
tier among their components. Full definitions, boundary rules and the classification of every
endpoint in the study are in `Drafts/operational_definitions.md`.

**Disclosure.** These definitions were written after all papers were scored and formalise the rule
applied during scoring. They were not prespecified. What can be verified, and has been, is that
every item 9 verdict follows from the tier assignment with no exceptions and no discretionary
calls.

### Modification to item 8, and its correction

One substantive departure from the source occurred and was corrected during the study.

The source reads "Clear of any conflict of interest". From the first paper scored until 2 August
2026 the item was applied as "The study is clear of undisclosed conflicts of interest". That is a
different question. Under the narrowed wording the item returned no negative verdict in sixteen
papers and became one of four columns holding a single value, and that degeneracy was initially
written up as a limitation of the instrument.

On obtaining the source the modification was identified, the wording reverted, and all sixteen
papers rescored with sign off on 2 August 2026. The earlier finding was withdrawn.

Read at maximum strictness the reverted item fails the lecture's own exemplar, because an author
of the CLOT trial declares fees from seven anticoagulant manufacturers while the trial's
intervention is a recommendation to begin anticoagulation. Since the source marks that exemplar as
satisfying all thirteen items, the intended threshold must be narrower than the literal reading.
The rule adopted is the strictest under which the exemplar still passes.

> A conflict exists when an author or the study has a financial or ownership interest in the
> specific tool under evaluation, or when the tool's maker funded or sponsored the study.
> Equipment loan alone does not count. Relationships with unrelated products do not count.

The rule was fixed and recorded before any paper was rescored. Two verdicts under it are flagged
in their scoring notes as genuinely arguable. The full account, including the effect on every
downstream figure, is in `Drafts/checklist_provenance.md` and deviation D10.

### Instrument freeze

The instrument was frozen on 2 August 2026, recorded as deviation D11. The item wordings, the item
class rule, the `Unclear` conventions, the tier taxonomy and the item 8 threshold are closed to
further change while the reliability assessment is outstanding, because a change made after the
second rating begins would render the two sets of verdicts incomparable and would present an
instrument revision as rater unreliability. Any wording problem identified after that date is
reported as a limitation rather than corrected.

---

## Eligibility criteria

Inclusion required all of the following. A primary report of a prospective clinical study
evaluating an imaging based AI tool in human patients. An imaging domain of retinal imaging,
colonoscopy video or twelve lead electrocardiography. A design that is a randomised trial of any
randomisation unit, a prospective diagnostic accuracy or pivotal trial, or a model development
study with prospective or external clinical evaluation. Publication between 1 January 2018 and 28
July 2026. English full text. Full text obtainable.

Any one of the following excluded a record. Systematic review, meta analysis or pooled analysis.
Editorial, commentary, letter or conference abstract. Protocol or design only paper reporting no
results. Secondary, companion, post hoc or qualitative analysis of a trial reported elsewhere.
Retrospective only model development with no prospective or external clinical evaluation. Non
human, phantom or simulation study. Duplicate report of a trial already included.

---

## Information sources and search

The search protocol was written and frozen on 28 July 2026, before the expansion search was run
and before any candidate paper was viewed, and is held in the `Search Protocol` sheet of the
tracker.

The database was PubMed and MEDLINE. The publication window ran from 1 January 2018 to 28 July
2026, the lower bound set by the earliest paper already held. The search was executed on 28 July
2026. Three full search strings, one per domain, are recorded in PubMed syntax in the protocol.

**Disclosure.** Embase and Web of Science were declared in the protocol as secondary sources to be
used if PubMed returned fewer eligible records than a domain quota required. That condition was met
in the retinal domain and the secondary databases were not run. The shortfall was instead handled
by revising the target downward, logged as deviation D1. Searching a single database is a
limitation of this study.

**Disclosure.** The protocol was frozen after ten of the fifteen appraised papers had already been
scored. Those ten were not selected under it. The protocol governed the expansion from ten to
fifteen and governs any future addition.

---

## Selection

Where eligible candidates exceeded a domain quota, selection ran in descending order of
publication date. Recency was chosen because it is independent of the checklist result. Ranking by
citation count would bias toward positive and widely promoted trials and ranking by sample size
would bias toward industry funded ones.

Every record assessed at full text was recorded with an include or exclude decision, the criterion
invoked and a reason, whether or not it entered the final set. Eighteen records are logged in the
`Screening Log` sheet. Records that were eligible but fell outside a quota are retained as
supporting evidence rather than discarded.

**Verification.** Before entry to the manifest, the downloaded file was opened and page one read,
and the first author, journal, publication year and study design confirmed against the intended
record. A file failing any of the four does not enter the manifest and is filed separately with
the mismatch logged. This step exists because two of the original twelve files, seventeen percent,
contained a different paper from the one the manifest named. On its first application to eight new
downloads the step rejected two further files.

---

## Analysis sets

**Primary set.** Eleven papers, four retinal and seven colonoscopy. Every headline figure
describes this set.

**Secondary set.** Four electrocardiography papers, reported separately and never pooled into a
headline figure. A twelve lead electrocardiogram is a time series rather than an image, so these
papers cannot sit within an appraisal of imaging. They are retained because they supply the only
tier four primary endpoint in the collection and the clearest single demonstration that process
measures and patient outcomes can move in opposite directions within one trial. The narrowing
follows peer feedback on the proposal and is logged as deviation D7.

**Reference case.** One further paper, the CLOT trial, scored on the same thirteen items under the
same conventions and held on a separate sheet excluded from every summary and export. It is the
trial to which the instrument was applied in its original non imaging domain and it anchors the
second clause of the hypothesis. Because the original application is a single trial, that clause is
reported as an illustrated contrast against one comparator and explicitly not as a statistical
comparison.

**Supporting papers.** Five further papers are documented but not scored, each with the exclusion
criterion that placed them there.

The domain comparison stated as an aim in the proposal is withdrawn. It cannot be supported at this
sample size and the interval analysis demonstrates rather than asserts this. It is reported as a
demonstrated negative result.

---

## Scoring procedure

Every verdict was assigned by reading the full paper. No verdict was assigned by keyword search.

Verdicts were assigned by a single human appraiser working with the assistance of a large language
model. For each paper the model was given the full text and the instrument and proposed all
thirteen verdicts with written reasoning. The appraiser reviewed each proposal against the paper
and confirmed, amended or rejected it before anything was written to the record. The appraiser is
accountable for every verdict and no verdict entered the record without explicit sign off.

This is disclosed for two reasons. A reader assessing the appraisal is entitled to know how the
verdicts were produced. And it constrains the choice of second rater, because a model drawn from
the same family as the one that assisted here would share its training and its characteristic
errors, so agreement between the two would measure very little. Any model used in the reliability
assessment therefore comes from a different developer, and that requirement is recorded in
deviation D12.

Papers were scored one at a time. For each paper all thirteen verdicts were proposed with written
reasoning and confirmed before any cell was written to the record. No batch scoring was performed
and no verdict was entered without sign off.

Each paper carries a written justification note recording the evidence for every verdict, with
section or page locators and quoted wording where the wording is the point. Notes run between
roughly two and a half thousand and five thousand characters per paper. Where a verdict was
amended after initial scoring, the amendment is appended with its date, its prior value and its
reason, and the superseded reasoning is retained for audit rather than deleted.

A software notebook extracts candidate evidence from each PDF by regular expression and reports
where the relevant language appears, with a page reference and a snippet. **It does not assign
verdicts.** An earlier version offered automatic suggestions for two items. The intention to treat
suggestion was checked against five papers and was wrong in five of five, by four distinct
mechanisms, and both suggestion columns were withdrawn.

---

## Reliability

A second rater independently scores a subset. The procedure was fixed in advance of any second
rating and is held in `Drafts/second_rater_protocol.md`.

A fallback was specified in advance as well, before any fallback rating was run and before any
fallback result was seen. It is held in `Drafts/fallback_rater_protocol.md` and recorded as
deviation D12. It fixes the order of preference among possible raters, which runs from an
independent human with relevant background, to an independent human from another analytical field,
to a frontier language model from a developer other than the one whose assistant supported the
first rater. It also fixes what each may be called. The two human options support inter rater
agreement in the ordinary sense. The model option supports a reproducibility check on the
instrument and is not reported as inter rater reliability anywhere. If a human rating arrives at
any point before submission it becomes the primary result automatically, whichever of the two
produces the higher agreement.

Five of the fifteen papers were selected by seeded random draw stratified by domain, seed
20260729, giving sixty five cells. The draw was random rather than purposive, because selecting
the papers that appeared hardest would depress agreement by construction.

The draw preceded the narrowing of scope described above, so four of the five selected papers fall
in the primary imaging set and one falls in the secondary set. The sample was not redrawn, because
the first rater's verdicts on all fifteen papers were already known when the narrowing was made,
and a redraw at that point would have been a selection informed by the data. The primary agreement
figure is therefore computed across all sixty five cells and covers four of the eleven primary
papers and one of the four secondary papers. A figure restricted to the four imaging papers may be
reported additionally as a descriptive, and that option was declared in advance so that the choice
between the two could not be made after the numbers were seen. This is recorded as deviation D8.

The second rater receives the papers, the full item wordings, the item class rule, the `Unclear`
conventions, the tier definitions and a blank form. The rater does not receive any existing
verdict, any justification note, any summary or export, or any statement of what the study
predicts. The rules are shared deliberately, because a reliability study measures whether two
people applying the same stated rules reach the same verdicts, not whether they independently
invent the same rules.

Agreement is computed on the independent ratings before any discussion between raters, and is not
recomputed after reconciliation. Three coefficients are reported together, because no single one
is trustworthy on data this skewed toward `Yes`. Cohen's kappa on the substantive categories, raw
percent agreement, and a prevalence adjusted statistic. Per item kappa is not computed for items
where one category holds every cell, since it is unstable or undefined there even under perfect
agreement. Concordance on `N/A` placement is reported separately as a test of the item class rule.

Disagreements are logged with both verdicts and both notes and then reconciled by discussion. Any
verdict changed as a result is changed on the record with its prior value and date.

No human rater came forward, and the fallback was executed on 3 August 2026 as run 1 of the three it
specifies, recorded as deviation D14. Because the rater was a model with no memory, there was nobody
to reconcile with, so the disagreements are reported and the first rater's verdicts stand. The
agreement figure was computed once from the independent ratings and is not recomputed. Results
section 3.11 reports it as a reproducibility check on the instrument rather than as inter rater
reliability, in the terms fixed in advance by D12. All three passes specified by that protocol were
completed, and results section 3.12 reports the rater's stability against itself, computed on the
raw verdicts before the quotation gate because that gate protects the comparison against rater 1 and
has no bearing on the model's own variance.

---

## Statistical analysis

Every interval reported in this paper is a two sided 95 percent confidence interval, abbreviated CI
in tables. Several items
sit at or near a boundary, so no normal approximation interval was used anywhere.

Single proportions carry Wilson score confidence intervals, with exact Clopper-Pearson intervals computed
alongside as a check. The comparison between item 1 and item 9 is paired, because both were scored
on the same papers, and uses the Newcombe interval for paired proportions with an exact McNemar
test on the discordant pairs. The group level contrast uses a sign test over papers.

Pooled group rates count several cells from each paper and those cells are not independent. A
cluster bootstrap resampling whole papers was computed for every group. With so few clusters the
bootstrap proved unreliable at boundaries, collapsing to zero width where a column holds a single
value, so the interval reported for each group follows a rule fixed in advance rather than chosen
once the numbers were visible. Groups built from a single item are unclustered and take Wilson. For
multi item groups the cluster bootstrap is reported unless it is narrower than the naive interval,
in which case the wider naive interval is taken. The rule and the method it selected for each group
are recorded in the exported data.

Two contrasts are tested, both stated in the proposal before the appraisal began. All other figures
are estimation rather than testing, so no correction for multiple comparisons is applied.

---

## Reproducibility

The complete record is a spreadsheet workbook containing the item definitions, the paper manifest,
every verdict with its justification, the search protocol, the screening log and the deviations
log. All analysis runs in Python notebooks under version control of their outputs, with package
versions pinned. Python 3.13.14 was used throughout.

The appraisal record contains no live formulas. All derived values are written as static values by
a refresh notebook that also regenerates the exported data, so that every reported figure can be
traced to the verdicts it came from and regenerated from them.

---

## Deviations

Thirteen deviations from the protocol are logged with dates and rationale in the `Search Protocol`
sheet, covering the revised target, two records that could not be obtained, an authorship
concentration in one domain, two files rejected at verification, two deviations recorded late on
audit, the scope narrowing, the decision not to redraw the reliability sample afterwards, the
unverified checklist provenance and its resolution, the item 8 reversion, the instrument freeze,
the fallback specified in advance for the reliability assessment, and an amendment to the
transcription rule within that fallback.

Papers weakening the hypothesis are reported rather than dropped, and findings that were reported
and later proved wrong are withdrawn in place rather than quietly replaced.
