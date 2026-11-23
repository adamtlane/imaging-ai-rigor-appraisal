# Capstone Summary Sheet

**Author.** Adam T. Lane **Prepared.** 8 August 2026

## Target venue

| Field | Detail |
| --- | --- |
| Conference | NeurIPS 2026, the Fortieth Annual Conference on Neural Information Processing Systems |
| Symposium | AI for Meta-Science. Scaling and Organizing Science in the Age of AI Scientists. A NeurIPS 2026 workshop |
| Conference site | https://neurips.cc/Conferences/2026/ |
| Call for papers | Workshop, https://ai4metascience.org/ and conference, https://neurips.cc/Conferences/2026/CallForPapers |
| Author instructions | https://neurips.cc/Conferences/2026/MainTrackHandbook |
| Submission portal | https://openreview.net/group?id=NeurIPS.cc/2026/Workshop/AI4MetaScience |
| Submission deadline | 29 August 2026, Anywhere on Earth |
| Author notification | 29 September 2026 |
| Event dates | 6 to 12 December 2026. Workshop day in December, to be announced |
| Event location | NeurIPS 2026 Paris site. Main conference at the International Convention Centre, Sydney |

**Paper type.** A review of AI applications in a healthcare subdomain, the first of the
types listed in the capstone brief. It appraises the published imaging artificial intelligence
literature against a fixed thirteen item rigor instrument. A second contribution measures how far
that appraisal reproduces under an independent language model reader, which bears on evaluation
methodology rather than on the clinical literature itself. No new data were collected and no
software prototype was built.

**Why this venue.** The workshop is convened around quality control in the scientific record and
whether evaluation can scale to match how fast science is produced. This paper appraises what a
literature establishes, then measures how far that appraisal survives an automated reader, which is
the workshop's own question. Submissions are four or eight pages excluding references with an
unlimited appendix, and this paper is prepared at the eight page length as a substantial
contribution. It is formatted to that venue's author instructions and is ready to submit should a
future round be targeted.

## Final paper title

**Imaging Without Outcomes. A Targeted Rigor Appraisal of Medical Imaging AI and the Limits of
Automating It**

## Abstract

Medical artificial intelligence tools are evaluated almost invariably on how well the model
discriminates. That is a claim about the model rather than a claim about the patient. We appraised
fifteen published imaging artificial intelligence papers against a thirteen item rigor checklist
drawn from standard clinical trial criteria, producing one hundred and ninety five justified
verdicts. Across the eleven paper primary set, external validation was satisfied by ten and a
genuine patient outcome was the primary endpoint of none, a paired difference of 90.9 percentage
points with an exact McNemar p value of 0.0020 and no paper falling the other way. Transparent
reporting was also satisfied by no paper, so the evidentiary chain breaks at both ends rather than
one. We then asked whether the appraisal could be automated. A language model given only the written
rules and the papers reproduced the appraiser with a Cohen's kappa of 0.686, but its disagreements
concentrated in judging whether an item applied rather than in reading what a paper said. Rated
three times from cold it reproduced itself on 93.8 percent of cells where it had agreed with the
appraiser and 58.8 percent where it had not. Machine appraisal is least reliable exactly where it is
asked to do the most work.

## Disclosure of generative AI use

A generative artificial intelligence system was used as a measurement instrument in this study, and
its use is reported in the body of the paper rather than only in this statement.

No independent human second rater could be recruited. A fallback specified in advance, before any
result was seen, required a large language model from a developer unaffiliated with the first rater
to independently score a random sample. It was executed on 3 August 2026 using **Gemini 3.6 Flash**,
which scored five of the fifteen papers against the same thirteen items, producing sixty five
verdicts. It received the papers, the item wordings, the item class rule and a blank form, and
received no existing verdict, no justification note and no statement of what the study predicted.

Every reliability figure in the paper derives from those verdicts, including the Cohen's kappa of
0.686 with 83.0 percent raw agreement, the PABAK and Gwet AC1 values, the per item breakdown, and
the Fleiss' kappa of 0.844 measuring the model against itself across three cold passes. The figure
was computed once, before any inspection of disagreements, and never recomputed. It is reported
throughout as a reproducibility check on the written instrument, never as inter rater reliability,
and the paper states plainly that it does not meet the standard an independent human rater would
set. The paper also records that the first rating was itself model assisted under author sign off,
so neither side of the comparison is free of model involvement.

**Accompanying materials.** Paper source at `Manuscript/Submission/`, full manuscript at
`Manuscript/Draft/`, all 195 verdicts with justifications at `Data/Tracker/`, seven analysis
notebooks at `Notebooks/`, second rating record at `Data/Reliability/`.
