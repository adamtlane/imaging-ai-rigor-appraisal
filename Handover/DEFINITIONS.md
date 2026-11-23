# Operational Definitions

Patient outcome, surrogate, and clinical impact. These are the rules for scoring item 9, and
they are given to you in full so that both raters apply the same ones.

---

## Four tiers, not two

Item 9 asks whether the endpoint is a genuine patient outcome rather than merely a process or
surrogate measure. A simple two way split turns out to hide something, because endpoints fail
the item at four clearly different distances from the patient.

Assign every primary endpoint to one of four tiers. Item 9 scores `Yes` for tier four and `No`
for everything else.

| Tier | Name | What is being measured | Item 9 |
| --- | --- | --- | --- |
| 1 | Model performance metric | A property of the model, measured outside any care pathway | `No` |
| 2 | Process measure | Something the health system or the clinician did | `No` |
| 3 | Surrogate or intermediate clinical finding | Something true of the patient's body, believed to predict outcome | `No` |
| 4 | Patient outcome | Something that happened to the patient | `Yes` |

Record the tier you assigned in the note, alongside the verdict.

---

## Tier 4. Patient outcome

**Definition.** An event or state experienced by the patient, which the patient would notice or
which ends or alters their life, measured on the patient over a defined follow up period.

**Includes.** Death from any cause or from a specified cause. Major morbidity such as stroke,
myocardial infarction, cancer incidence, interval cancer, or a thrombotic event.
Hospitalisation. Symptom burden, function, quality of life, or vision loss measured on the
patient.

**The operative test.** Would the patient experience this if nobody told them about it? That
single question settles almost every case. A patient does not experience a detection rate, a
laboratory value, a referral, or an area under a curve.

---

## Tier 3. Surrogate or intermediate clinical finding

**Definition.** A measurement taken from the patient's body, which is not itself experienced by
the patient, and which is used because it is believed to stand in for a tier four outcome.

**The distinguishing feature.** A surrogate is located in the patient, but its value rests on a
causal claim that the paper usually does not test. Finding more lesions matters only if finding
them prevents disease. Diagnosing a condition matters only if the diagnosis leads to treatment
that helps.

**Includes.** Any detection or diagnosis count. Lesion detection rates and per procedure lesion
counts. A new diagnosis of a condition within a time window. Laboratory or imaging findings.

**A ruling worth stating plainly.** Diagnosing a disease is tier three, not tier four. A
diagnosis changes what is known about the patient rather than what happens to them.

---

## Tier 2. Process measure

**Definition.** A measurement of what the health system, the clinician, or the patient did,
rather than of the patient's condition or of what happened to them.

**Includes.** Examination or procedure completion. Referral uptake or attendance. Prescribing
rates. Specialist visits. Procedure duration. Adherence and follow through.

---

## Tier 1. Model performance metric

**Definition.** A statistical property of the classifier, computed on a dataset rather than
observed in a care pathway. No patient is affected by the study.

**Includes.** Area under the receiver operating characteristic curve, area under the precision
recall curve, sensitivity, specificity, accuracy, calibration.

**A ruling worth stating plainly.** A model performance metric stays tier one even when the
target being predicted is a genuine tier four event. Reporting discrimination for stroke or for
death on retrospective data is still tier one, because nobody's risk was altered. Predicting an
outcome is not measuring one.

---

## Clinical impact

Clinical impact is not scored as a separate item. It is the conjunction of two items, and it is
defined here so you know what the pair is for.

A paper demonstrates clinical impact when both of the following hold. Item 2, the tool was
evaluated in a pragmatic randomised comparison in which individual patients were allocated to
usual care or to usual care plus the tool. Item 9, the primary endpoint of that comparison sits
at tier four.

Either one alone is insufficient. A trial with faultless randomisation that measures a detection
rate has established that the tool changes what clinicians find, not that it helps anyone. An
observational study reporting mortality has measured the right thing without establishing that
the tool caused it.

---

## Decision rules for boundary cases

Apply these rather than improvising, so that both raters resolve the same case the same way.

**The primary endpoint governs.** Item 9 is scored on the primary endpoint alone. Secondary
endpoints, however good, do not change the verdict. A paper reporting a genuine patient outcome
as a secondary endpoint still scores `No` if its primary endpoint is a surrogate.

**Composite endpoints take the lowest tier of their components.** A composite reaches tier four
only if every component is tier four.

**Where a paper declares more than one primary endpoint, the lowest tier governs.** If one of
two co primary endpoints is a surrogate, the paper scores `No`.

**Time to diagnosis is tier three.** Faster diagnosis is not itself an outcome.

**A patient reported measure is tier four.** Symptom burden, function and quality of life are
experienced by the patient and qualify, even though they are not hard events.

**Intent does not count.** A paper that carefully describes its surrogate as a proxy for a
patient outcome still scores `No`. Candour about the limitation belongs in your note and, if the
paper is admirably clear about it, under item 7.

---

## If an endpoint does not fit

Record it as not fitting, in the note, rather than forcing it into the nearest tier. A gap in
this taxonomy is a finding worth having and it will be reported as one.
