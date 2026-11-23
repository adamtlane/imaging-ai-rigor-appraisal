# Operational Definitions

Patient outcome, surrogate, and clinical impact, as used in this appraisal.

---

## Status of this document, stated honestly

Written 29 July 2026, after all fifteen papers were scored. It codifies the rule that was
actually applied on 27 and 28 July. It is not a prospective definition and this document does
not claim to be one.

Reviewer feedback asked that these terms be defined before screening. That is correct practice
and it did not happen here. What can be claimed, and what is checkable by anyone, is that the
rule was applied consistently. Every one of the fifteen item 9 verdicts follows from the
taxonomy below with no exceptions and no discretionary calls. The worked classification near
the end of this document lets a reader verify that in a few minutes, and the second rater will
test it independently.

The honest framing for the manuscript is that the definitions were derived during scoring and
formalised afterwards, that consistency was verified retrospectively, and that a prospective
definition would have been better.

---

## Why a binary definition was not enough

The checklist item asks whether the endpoint is a genuine patient outcome rather than merely a
process or surrogate measure. Applied to fifteen papers, a simple two way split turned out to
hide something. The endpoints that failed the item failed it at four clearly different
distances from the patient, and collapsing them loses the finding.

So the working taxonomy has four tiers. Item 9 scores `Yes` for tier four and `No` for
everything else.

| Tier | Name | What is being measured | Item 9 |
| --- | --- | --- | --- |
| 1 | Model performance metric | A property of the model, measured outside any care pathway | `No` |
| 2 | Process measure | Something the health system or the clinician did | `No` |
| 3 | Surrogate or intermediate clinical finding | Something true of the patient's body, believed to predict outcome | `No` |
| 4 | Patient outcome | Something that happened to the patient | `Yes` |

---

## Tier 4. Patient outcome

**Definition.** An event or state experienced by the patient, which the patient would notice or
which ends or alters their life, measured on the patient over a defined follow up period.

**Includes.** Death from any cause or from a specified cause. Major morbidity such as stroke,
myocardial infarction, cancer incidence, or interval cancer. Hospitalisation. Symptom burden,
function, quality of life, or vision loss measured on the patient.

**Excludes.** Anything the patient would not experience if no one told them about it. This is
the operative test and it settles almost every case. A patient does not experience an adenoma
detection rate, an ejection fraction reading, a referral, or an area under a curve.

**In this set.** One paper of fifteen. Lin and colleagues 2024, all cause mortality at ninety
days.

---

## Tier 3. Surrogate or intermediate clinical finding

**Definition.** A measurement taken from the patient's body, which is not itself experienced by
the patient, and which is used because it is believed to stand in for a tier four outcome.

**The distinguishing test.** A surrogate is located in the patient but its value depends on a
causal claim that the paper usually does not test. Finding more adenomas matters only if
finding them prevents cancer. Diagnosing reduced ejection fraction matters only if the diagnosis
leads to treatment that helps.

**Includes.** Adenoma detection rate, adenomas per colonoscopy, sessile serrated lesion rate.
New diagnosis of a condition within a time window. Laboratory or imaging findings. Any
detection or diagnosis count.

**A ruling worth stating plainly.** Diagnosing a disease is tier three, not tier four.
Diagnosis changes what is known about the patient rather than what happens to them. Two papers
in this set take a new diagnosis of low ejection fraction as their primary endpoint and both
score `No`.

**In this set.** Nine papers of fifteen, seven of them colonoscopy trials with a detection
endpoint.

---

## Tier 2. Process measure

**Definition.** A measurement of what the health system, the clinician, or the patient did,
rather than of the patient's condition or of what happened to them.

**Includes.** Examination completion. Referral uptake or attendance. Prescription rates.
Specialist visits. Procedure time. Adherence and follow through.

**In this set.** Three papers of fifteen.

---

## Tier 1. Model performance metric

**Definition.** A statistical property of the classifier, computed on a dataset rather than
observed in a care pathway. No patient is affected by the study.

**Includes.** Area under the receiver operating characteristic curve, area under the precision
recall curve, sensitivity, specificity, accuracy, calibration.

**A ruling worth stating plainly.** A model performance metric stays tier one even when the
target being predicted is a genuine tier four event. One paper reports discrimination for
ischaemic stroke, heart failure and Parkinson's disease, which are unambiguously patient
outcomes, but reports them as areas under a curve on retrospective data. Nobody's stroke risk
was altered. Predicting an outcome is not measuring one.

**In this set.** Two papers of fifteen.

---

## Clinical impact

**Definition.** Clinical impact is the conjunction of two checklist items rather than a separate
judgment. A paper demonstrates clinical impact when both of the following hold.

Item 2, the tool was evaluated in a pragmatic randomised comparison in which individual
patients were allocated to usual care or to usual care plus the tool.

Item 9, the primary endpoint of that comparison sits at tier four.

**Why both.** Either one alone is insufficient in a way the data shows directly. A trial with
faultless randomisation that measures a detection rate has established that the tool changes
what clinicians find, not that it helps anyone. An observational study reporting mortality has
measured the right thing without establishing that the tool caused it.

**Reporting.** The clinical impact rate in this appraisal is the pooled proportion of `Yes`
verdicts across items 2 and 9 together.

---

## Decision rules for boundary cases

These are the rules that resolved every case that was not obvious. They are stated so a second
rater applies the same ones.

**The primary endpoint governs.** Item 9 is scored on the primary endpoint alone. Secondary
endpoints, however good, do not change the verdict. Two papers in this set report genuine tier
four outcomes as secondary endpoints and both score `No`.

**Composite endpoints take the lowest tier of their components.** A composite scores tier four
only if every component is tier four.

**Where a paper declares more than one primary endpoint, the lowest tier governs.** If one of
two co primary endpoints is a surrogate, the paper scores `No`.

**Time to diagnosis is tier three.** Faster diagnosis is not itself an outcome.

**A patient reported measure is tier four.** Symptom burden, function and quality of life are
experienced by the patient and qualify, even though they are not hard events.

**Intent does not count.** A paper that describes its surrogate as a proxy for a patient
outcome, however carefully, still scores `No`. Several papers in this set are admirably clear
that their endpoint is a surrogate, and that candour is recorded under item 7 rather than
under item 9.

---

## Worked classification of all fifteen primary endpoints

Primary set means the eleven imaging papers. Secondary set means the four electrocardiography
papers, which are reported separately following reviewer feedback on modality.

| # | Paper | Set | Primary endpoint as stated | Tier | Item 9 |
| --- | --- | --- | --- | --- | --- |
| 1 | Zhou 2023 (RETFound) | Primary | AUROC and AUPR for multiple prediction targets | 1 | No |
| 3 | Abramoff 2018 (IDx-DR) | Primary | Sensitivity and specificity | 1 | No |
| 2 | Wolf 2024 (ACCESS) | Primary | Eye examination completion | 2 | No |
| 15 | Mathenge 2022 (RAIDERS) | Primary | Referral uptake within thirty days | 2 | No |
| 4 | Kader 2026 (EAGLE/CADDIE) | Primary | Adenomas per colonoscopy and polyp positive agreement, co primary | 3 | No |
| 5 | Ahmad 2023 (AI-DETECT) | Primary | Adenoma detection rate | 3 | No |
| 6 | Wei 2023 (AI-SEE) | Primary | Adenomas per colonoscopy and adenoma detection rate, co primary | 3 | No |
| 7 | Repici 2020 | Primary | Adenoma detection rate | 3 | No |
| 8 | Ladabaum 2023 | Primary | Adenoma detection rate | 3 | No |
| 9 | Alali 2025 | Primary | Adenoma detection rate | 3 | No |
| 13 | Hsu 2026 | Primary | Adenoma detection rate | 3 | No |
| 11 | Yao 2021 (Mayo EAGLE) | Secondary | New diagnosis of low ejection fraction within ninety days | 3 | No |
| 12 | Tsai 2025 (Taiwan) | Secondary | New diagnosis of low ejection fraction within thirty days | 3 | No |
| 14 | Liu 2025 (CARDIOLOGIST) | Secondary | Anticoagulant prescription, new AF diagnosis, echo arrangement, cardiologist visits | 2 | No |
| 10 | Lin 2024 | Secondary | All cause mortality at ninety days | 4 | Yes |

**Tier distribution.** Two papers at tier one, three at tier two, nine at tier three, one at
tier four.

**In the primary imaging set of eleven**, zero papers reach tier four. Seven of the eleven sit
at tier three and every one of those seven is a colonoscopy detection endpoint.

---

## The case that justifies the whole distinction

Liu and colleagues 2025 is the sharpest available demonstration that the tier boundary is real
rather than pedantic.

Its primary endpoints are process measures and two of the four moved. Anticoagulant prescription
within ninety days rose from 12.0 to 23.3 percent. New atrial fibrillation diagnosis rose from
36.0 to 47.8 percent.

Its secondary endpoints are genuine tier four outcomes and not one of them moved. Ischaemic
stroke, no significant difference. Cardiovascular death, no significant difference. All cause
death, hazard ratio 0.72 with an interval from 0.50 to 1.04.

The same trial therefore reports a clear positive result on what the system did and a null
result on what happened to the patients. A reader who accepts process measures as evidence of
benefit would call this trial positive. That is the entire argument of this capstone in one
study.

---

## Consistency check

Every item 9 verdict in the tracker follows from the tier assignment above. Tier four scores
`Yes`, tiers one through three score `No`, and no paper received a verdict that departs from
the rule. There are no discretionary item 9 calls in the dataset.

This check is reproducible. The tier column above can be compared against the item 9 column of
`Data/Tracker/exports/scoring_long.csv` for all fifteen papers.

---

## Instruction to the second rater

Score item 9 by locating the primary endpoint, assigning it a tier using the definitions above,
and recording the tier in the note alongside the verdict. Do not consult this worked table
before scoring, since it contains the first rater's answers. Its purpose is reconciliation
after independent rating, not guidance during it.

If an endpoint does not fit any tier cleanly, record it as such in the note rather than forcing
it. A gap in the taxonomy is a finding worth having.
