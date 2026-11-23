# Checklist Provenance and Modification Log

Answers the reviewer's request to justify any modifications to the original checklist.

Written 2 August 2026, after the Module 9 lecture slides were obtained. The source is
`Refs/Lecture 9A Slides.pdf`, and the checklist appears as a table on slide 3, repeated
unchanged on slide 31, under the heading "Feature of the AI Project and Evaluation Approach"
against a second column headed "Our Typical Approach".

---

## The headline answer

**The thirteen items are reproduced from the source. None was added, dropped, reworded in
substance, or reordered.** The lecture's table and this project's Legend list the same thirteen
features in the same sequence.

**One substantive modification was made, to item 8, and it has since been reverted.** It is
documented in full below because it materially affected the results and because it produced a
false finding that was written up and then withdrawn.

**Everything else in the Legend is elaboration rather than modification.** The lecture states
each item as a short feature name and then explains it across the body slides. The Legend states
each item as a scoreable criterion. Where the Legend says more than the slide table, the extra
wording almost always comes from the lecture's own explanatory slides, and those slides are cited
item by item below.

---

## Side by side

| # | Source wording, slide 3 | Wording as applied | Status |
| --- | --- | --- | --- |
| 1 | External validation of the model | The model has been shown to hold up on a separate (external temporal or geographic) dataset, not just internal analysis | Elaborated |
| 2 | Pragmatic patient-level randomized controlled trial of impact | There is a pragmatic, patient-level randomized controlled trial of impact (usual care vs. usual care plus AI), not a provider-selected or before/after comparison | Elaborated, from slide 5 |
| 3 | Prespecified primary endpoint | The primary endpoint was prespecified before the trial began | Equivalent |
| 4 | Prespecified study design | The study design was prespecified before the trial began | Equivalent |
| 5 | Registered with ClinicalTrials.gov | The trial was registered with ClinicalTrials.gov before initiation, with an NCT number stated in the Methods | Elaborated, from slide 10 |
| 6 | Transparent reporting of the model (as opposed to black box/proprietary) | The model's predictors and their relative importance are reported; the model is not a black box (e.g., formula in appendix, explorable app) | Elaborated, from slides 13, 18 and 19 |
| 7 | Honest, rigorous evaluation of the impact published | The evaluation of the model's real-world impact is rigorous and honestly reported, not overstated relative to the results | Elaborated |
| 8 | **Clear of any conflict of interest** | **Reverted to the source wording on 2 August 2026** | **Modified, then reverted. See below** |
| 9 | Focus on improving patient outcomes | The endpoint is a genuine patient outcome (e.g., mortality, major morbidity), not merely a process or surrogate measure (e.g., detection rate) | Elaborated, from slide 22 |
| 10 | Sufficiently large sample size | The sample size is sufficiently large to detect the effect claimed (and not so large that trivial effects appear significant) | Elaborated, from slide 23 |
| 11 | Analysis based on the intention-to-treat principle | The primary analysis follows the intention-to-treat principle | Equivalent |
| 12 | Two study arms are balanced in Table 1 | The two study arms are shown to be comparable/balanced in a Table 1 | Equivalent |
| 13 | Avoided reverse causation/data leakage (outcome used as a predictor) | The model avoids reverse causation or data leakage (an outcome used as a predictor) | Equivalent |

### Where the elaborations come from

Item 2. Slide 5 states that assessing whether AI improves patient outcomes requires patient level
randomisation of usual care against usual care plus AI, that comparisons based on providers
selecting patients are of little value, and that before and after comparisons are of little value.
The Legend's added clause reproduces that.

Item 5. Slide 10 gives the sentence a paper should contain, namely that the trial was registered
before initiation with a ClinicalTrials.gov registration number. The Legend's added clause
reproduces that.

Item 6. Slide 13 lists reporting the predictors, showing their relative importance, making the
model easy for others to use, and providing a site or app to experiment with it. Slide 18 says to
provide the formula in the appendix. Slide 19 describes a Shiny app and states that the model is
explainable and transparent rather than a black box. The Legend's added clause reproduces those.

Item 9. Slide 22 states that many papers report an endpoint that is not an important patient
outcome and that many demonstrate improvements in process measures or intermediate outcomes. Its
worked example is polyp detection rates in colonoscopy. The Legend's added clause reproduces that.

Item 10. Slide 23 carries the note that some studies are too large. The Legend's parenthesis
reproduces it.

Item 1. The lecture states only that external validation is essential (slide 4). The Legend's
"external temporal or geographic" is this project's own gloss and is the one elaboration not
traceable to a slide. It is recorded here rather than left implicit.

---

## The one substantive modification

### What was changed

The source reads **"Clear of any conflict of interest"**. From the first paper scored until
2 August 2026 this project applied **"The study is clear of undisclosed conflicts of interest"**.

That is not a clarification. It is a different question. The source asks whether the study is
independent of commercial interest. The applied version asked only whether interest was hidden.

### Why it was made

The reasoning at the time, recorded in the scoring notes, was that a reader of a single published
paper can verify disclosure but cannot verify independence, so disclosure is the only thing the
appraiser can actually check. That reasoning is not unreasonable. It is also wrong as a matter of
fidelity to the instrument, because it substitutes what is easy to measure for what was asked.

### What it did to the results

Under the modified wording the item returned **no negative verdict in sixteen papers**, including
papers whose authors were employees, directors, shareholders, patent holders or paid consultants
of the manufacturer whose product was under test. It became one of four columns holding a single
value across the primary set.

That degeneracy was then written up as a finding about the instrument, namely that the conflict of
interest item detects disclosure rather than independence and therefore cannot discriminate in
this literature. **That finding was an artifact of this project's own rewording and has been
withdrawn.**

### What was done about it

The wording was reverted to the source and all sixteen papers were rescored on 2 August 2026 with
sign off, logged as deviation D10.

| | Under the modified wording | Under the source wording |
| --- | --- | --- |
| Item 8, imaging primary set | 11 of 11, 100 percent | 4 of 11, 36.4 percent |
| Integrity group, primary set | 90.0 percent | 55.0 percent |
| Columns holding a single value | 4 of 13 | 3 of 13 |
| Item 8 rank among the thirteen | joint best | third worst |

The item now discriminates, and what it reveals is substantive. Seven of the eleven papers in the
primary set were evaluated by people with a financial or ownership interest in the tool being
evaluated, or were funded by its maker.

---

## Calibrating the reverted item

Read at maximum strictness, "clear of any conflict of interest" fails the lecture's own exemplar.
An author of the CLOT trial declares personal fees from seven anticoagulant manufacturers, and the
trial's intervention is a recommendation to start anticoagulation. Slide 3 nevertheless marks CLOT
as satisfying all thirteen items.

The source therefore tells us the intended threshold is narrower than the literal reading. The
rule adopted is the strictest one under which the exemplar still passes.

> A conflict exists when an author or the study has a financial or ownership interest in the
> **specific tool under evaluation**, or when the tool's maker funded or sponsored the study.
> Equipment loan alone does not count. Relationships with unrelated products do not count.

Two verdicts under this rule are flagged in their scoring notes as genuinely arguable, with
`Unclear` defensible for either. Zhou, where an author holds equity in a medical AI company while
publishing a retinal AI model that is not that company's product. Ahmad, where the authors' ties
are to direct commercial competitors of the device under test, which is a conflict pointing away
from rather than toward a favourable result.

---

## Additions this project made to the instrument

Two rules were added that the source does not contain. Neither changes any item's meaning. Both
were needed to apply thirteen binary features to a heterogeneous body of papers, and both are
declared.

**The item class rule**, governing when `N/A` is permitted. The source presents the checklist as
thirteen features that a well conducted project satisfies, with a single exemplar that satisfies
all thirteen. It does not address what to do with a paper that has no trial arms. Items are
therefore sorted into four classes by what may excuse them, and for items 2 and 9 `N/A` is never
available, because those two are the quantities the study measures and allowing a design based
exemption would restrict their denominators to the papers that pass. Full statement in the
`Legend` sheet and in `Search Protocol` section I.

**The Unclear conventions.** The source offers `Yes` against a question mark. This project needed
a third and fourth verdict for papers where the answer is genuinely not determinable. Items 3 and
4 take `Unclear` when a trial is unregistered, because self reported prespecification cannot be
checked against anything. Item 5 takes `Unclear` when a trial was registered prospectively outside
ClinicalTrials.gov, because scoring `No` would wrongly equate it with reporting no registration at
all.

---

## Two further observations from the source

**The lecture names this project's central finding as the failure mode to look for.** Slide 22
warns that many papers demonstrate improvements in process measures or intermediate outcomes, and
gives polyp detection rates in colonoscopy as its example. Seven of the eleven primary set papers
are colonoscopy trials with a detection endpoint.

**The original application is three papers, not one.** The reference list names Walker 2021 in
Pediatrics (model derivation), Walker 2022 in Trials (protocol) and Walker 2023 in JAMA Network
Open (the trial). This project scored only the trial. Judged as the three paper package the
original application is stronger than the single paper scoring shows, particularly on item 6,
since the derivation paper supplies the variable list, the classification tree, the appendix
formula and a working app. The reference case verdict of `Yes` on item 6 is therefore conservative
rather than generous.

**One disagreement with the source is recorded rather than resolved.** Slide 3 marks CLOT as
satisfying item 11, intention to treat. This project scored it `No`, because the trial analysed a
modified intention to treat population that excluded 411 of 17,838 randomised patients after
randomisation. The exclusions are small, balanced and prespecified, and many methodologists would
accept them. The convention applied here is strict and was applied identically to every paper, so
the verdict stands, but the disagreement is visible rather than buried.
