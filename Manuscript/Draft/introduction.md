# Introduction

Draft 4 August 2026.

---

A paper announcing a medical artificial intelligence tool almost always reports how well the model
discriminates. Area under the curve, sensitivity, specificity. These are claims about the model.
They are not claims about the patient, and the distance between the two is larger than the
literature's own framing usually admits.

Between a model that discriminates and a patient who is better off lies a chain of evidence with
several links. A model must first perform on data it was not fitted to. It must then hold up on data
from another site or another period, since a model that only works where it was built is a local
curiosity. It must then be placed in front of clinicians in a real care pathway, because a model
that performs in silico may change nothing when a busy person is free to ignore it. And finally the
pathway containing the model must be shown to leave patients better off than the pathway without it.
Each link is a separate empirical claim. Establishing one does not establish the next, and a
literature can accumulate a great deal of evidence for the early links while producing almost none
for the last.

This project asks where in that chain the published imaging artificial intelligence literature
actually stops.

## Why the distinction carries particular weight in this literature

Every field has surrogate endpoints, and their limitations are well understood in general terms. The
imaging artificial intelligence literature has a more specific problem, which is that its dominant
endpoints are properties of the examination rather than properties of the patient.

In colonoscopy the standard endpoints are the adenoma detection rate and the number of adenomas
found per procedure. Both are measures of what the examination found. Neither is a measure of what
happened to the person examined. The link between finding more adenomas and preventing more cancers
is plausible, is supported for detection rates in the historical literature, and is not the same
claim. A tool that finds more small polyps raises the detection rate by construction, and whether it
prevents any cancer is a separate question that a detection endpoint cannot answer.

In retinal screening the equivalent endpoints are referral rates and screening uptake. These measure
what the health system did. Whether anyone kept their sight is again a separate question.

The consequence is that a trial can be well designed, honestly reported, adequately powered and
entirely positive, and still tell a reader nothing about whether patients benefited. That is not a
flaw in any individual study. It is a property of what the field has collectively agreed to measure,
and it is invisible unless someone counts.

## Why imaging

Imaging is where medical artificial intelligence has travelled furthest into practice. Autonomous
diagnostic systems have regulatory clearance, computer aided detection is installed in endoscopy
suites and reimbursed, and screening programmes in several countries now run with algorithmic
assistance. If the evidentiary chain is incomplete anywhere it matters, it matters here, because
these are the tools already in front of patients rather than the tools proposed for them.

Imaging also offers something methodologically useful. Two of its subfields, retinal screening and
colonoscopy, have each produced completed randomised trials of clinical impact rather than
diagnostic accuracy studies alone. That makes it possible to appraise trials that genuinely
attempted the later links in the chain, rather than only observing that most papers never attempt
them.

## The appraisal approach

The question is answered by structured appraisal rather than by argument. A defined set of published
papers was identified through a prespecified search, and each was read in full and scored against a
fixed thirteen item rigor checklist covering external validation, trial design and conduct, honest
reporting, independence from the manufacturer, transparency of the model, and whether the primary
endpoint was a genuine patient outcome.

A narrative review could assert that the field measures surrogates. An appraisal can say how often,
on which items, with what uncertainty, and against a reference point. The unit of analysis is the
paper by item cell, which makes the failures countable and locates them rather than describing them.

The instrument is the appraisal checklist taught in Module 9 of this course. Its worked example is a
randomised trial of a paediatric thromboembolism prognostic model, a study outside imaging that the
source marks as satisfying all thirteen items. That example matters for two reasons. It shows the
items are jointly satisfiable, so a literature failing them is failing something achievable rather
than an unreachable standard. And it supplies an external reference point, since the same instrument
already has an established application in another domain against which imaging can be compared. That
trial is appraised here as a reference case alongside the imaging papers.

## Hypothesis

The hypothesis was fixed in the proposal before any paper was scored. It holds that these papers will
score well on the items asking whether the model works and poorly on the items asking whether it
helps patients, and that the distance between the two will prove wider in imaging than in the domain
where the checklist was first applied.

The prediction is directional and was registered as such. Both the item level contrast and the group
level contrast were named in advance, and no other comparison in this appraisal is tested.

## What this paper contributes

Three things beyond the headline count.

A quantified location for the break in the evidentiary chain, reported as a paired contrast on the
same papers rather than as two independent proportions, with an exact test and an interval.

An operational definition separating patient outcomes from surrogate and process measures, arranged
as four tiers with an explicit test for the boundary that matters, and applied to every primary
endpoint in the collection. The distinction is the one on which the central finding rests, so it is
stated in a form another appraiser can apply rather than left to judgment.

And an account of the instrument itself. Applying a rigor checklist carefully to fifteen papers turns
out to expose as much about the checklist as about the papers, including which items discriminate,
which penalise defensible design choices, and which parts of it a second independent reader cannot
reliably reproduce.
