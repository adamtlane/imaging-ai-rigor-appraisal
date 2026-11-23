# Session prompts, ready to paste

Operator material. This file is never sent to any rater, human or model.

The prompt is fixed in Appendix A of `Drafts/fallback_rater_protocol.md` and the five blocks below
reproduce it word for word, with only the paper number and the citation differing. They are written
out in full rather than left as a template so that nothing has to be edited by hand fifteen times,
because hand editing is where a session would quietly stop matching the specification.

**Attach three files to every session.** The paper from `Handover/Papers/`, plus
`Handover/RATER_INSTRUCTIONS.md` and `Handover/DEFINITIONS.md`. Every paper listed below is the
copy in `Handover/Papers/`, not the copy in the main `Papers/` tree.

**One paper per session, in a fresh conversation.** Order is 1, 3, 4, 8, 14. Three runs, fifteen
sessions. Save each reply verbatim to `raw/run{R}_paper{PP}.md` and fill the row in `run_log.csv`.

**Do not reply to a session.** No follow up, no clarification, no correction, whatever comes back.
If it stops or returns something unusable, record that in the run log and open the next session.

---

## Session order and files

| Order | Paper | Attach from`Handover/Papers/`       |
| ----- | ----- | ------------------------------------- |
| 1st   | 1     | `zhou_2023_retfound.pdf`            |
| 2nd   | 3     | `abramoff_2018_idx_dr.pdf`          |
| 3rd   | 4     | `eagle_caddie_2025.pdf`             |
| 4th   | 8     | `ladabaum_2023_pragmatic_trial.pdf` |
| 5th   | 14    | `liu_2025_ai_ecg_af.pdf`            |

Note that the file for paper 4 is named 2025 while the paper itself is a 2026 issue. The filename
was never corrected and is left alone so that it continues to match the tracker manifest. The
instructions tell the rater how to read the year, so this does not matter to them.

---

## Paper 1

```
You are acting as an independent second rater in a formal reliability study. Three files are attached. One is a published research paper. The other two are the rating instructions and the operational definitions that govern this exercise.

Read RATER_INSTRUCTIONS.md in full and follow it exactly. Keep DEFINITIONS.md open for item 9. Score the attached paper against all thirteen checklist items.

For each item return four fields. The item number. A verdict, which is one of Yes, No, Unclear or N/A and nothing else. A confidence, which is one of High, Medium or Low. And a note.

For a verdict of Yes or No, the note must contain a locator, meaning the section name or page number, and a verbatim quotation from the attached paper that settles the item. Quote, do not paraphrase. If you cannot find and quote supporting text in the attached paper, return Unclear rather than answering from prior knowledge of this paper or its reputation. This rule is absolute.

For a verdict of Unclear, state which specific fact is missing and where in the paper you looked for it. For a verdict of N/A, state the item class you are invoking and the design feature that triggers it, and note that N/A is available only where the item class table in the instructions permits it.

Where a verdict was close, say so and say what the alternative was.

Before scoring, confirm the first author, the journal, the year and the study design from page one of the attached file. Report what you found. If any of the four disagrees with the citation given below, stop and say so rather than scoring.

Paper number 1. Citation as recorded: Zhou et al. 2023, Nature (RETFound).

Return the thirteen items as a table, followed by any observation the thirteen items have no room for. Do not ask clarifying questions and do not comment on the exercise.
```

---

## Paper 3

```
You are acting as an independent second rater in a formal reliability study. Three files are attached. One is a published research paper. The other two are the rating instructions and the operational definitions that govern this exercise.

Read RATER_INSTRUCTIONS.md in full and follow it exactly. Keep DEFINITIONS.md open for item 9. Score the attached paper against all thirteen checklist items.

For each item return four fields. The item number. A verdict, which is one of Yes, No, Unclear or N/A and nothing else. A confidence, which is one of High, Medium or Low. And a note.

For a verdict of Yes or No, the note must contain a locator, meaning the section name or page number, and a verbatim quotation from the attached paper that settles the item. Quote, do not paraphrase. If you cannot find and quote supporting text in the attached paper, return Unclear rather than answering from prior knowledge of this paper or its reputation. This rule is absolute.

For a verdict of Unclear, state which specific fact is missing and where in the paper you looked for it. For a verdict of N/A, state the item class you are invoking and the design feature that triggers it, and note that N/A is available only where the item class table in the instructions permits it.

Where a verdict was close, say so and say what the alternative was.

Before scoring, confirm the first author, the journal, the year and the study design from page one of the attached file. Report what you found. If any of the four disagrees with the citation given below, stop and say so rather than scoring.

Paper number 3. Citation as recorded: Abramoff et al. 2018, npj Digital Medicine (IDx-DR).

Return the thirteen items as a table, followed by any observation the thirteen items have no room for. Do not ask clarifying questions and do not comment on the exercise.
```

---

## Paper 4

```
You are acting as an independent second rater in a formal reliability study. Three files are attached. One is a published research paper. The other two are the rating instructions and the operational definitions that govern this exercise.

Read RATER_INSTRUCTIONS.md in full and follow it exactly. Keep DEFINITIONS.md open for item 9. Score the attached paper against all thirteen checklist items.

For each item return four fields. The item number. A verdict, which is one of Yes, No, Unclear or N/A and nothing else. A confidence, which is one of High, Medium or Low. And a note.

For a verdict of Yes or No, the note must contain a locator, meaning the section name or page number, and a verbatim quotation from the attached paper that settles the item. Quote, do not paraphrase. If you cannot find and quote supporting text in the attached paper, return Unclear rather than answering from prior knowledge of this paper or its reputation. This rule is absolute.

For a verdict of Unclear, state which specific fact is missing and where in the paper you looked for it. For a verdict of N/A, state the item class you are invoking and the design feature that triggers it, and note that N/A is available only where the item class table in the instructions permits it.

Where a verdict was close, say so and say what the alternative was.

Before scoring, confirm the first author, the journal, the year and the study design from page one of the attached file. Report what you found. If any of the four disagrees with the citation given below, stop and say so rather than scoring.

Paper number 4. Citation as recorded: Kader et al. 2026, npj Digital Medicine 9:84 (EAGLE/CADDIE), doi 10.1038/s41746-025-02270-1.

Return the thirteen items as a table, followed by any observation the thirteen items have no room for. Do not ask clarifying questions and do not comment on the exercise.
```

---

## Paper 8

```
You are acting as an independent second rater in a formal reliability study. Three files are attached. One is a published research paper. The other two are the rating instructions and the operational definitions that govern this exercise.

Read RATER_INSTRUCTIONS.md in full and follow it exactly. Keep DEFINITIONS.md open for item 9. Score the attached paper against all thirteen checklist items.

For each item return four fields. The item number. A verdict, which is one of Yes, No, Unclear or N/A and nothing else. A confidence, which is one of High, Medium or Low. And a note.

For a verdict of Yes or No, the note must contain a locator, meaning the section name or page number, and a verbatim quotation from the attached paper that settles the item. Quote, do not paraphrase. If you cannot find and quote supporting text in the attached paper, return Unclear rather than answering from prior knowledge of this paper or its reputation. This rule is absolute.

For a verdict of Unclear, state which specific fact is missing and where in the paper you looked for it. For a verdict of N/A, state the item class you are invoking and the design feature that triggers it, and note that N/A is available only where the item class table in the instructions permits it.

Where a verdict was close, say so and say what the alternative was.

Before scoring, confirm the first author, the journal, the year and the study design from page one of the attached file. Report what you found. If any of the four disagrees with the citation given below, stop and say so rather than scoring.

Paper number 8. Citation as recorded: Ladabaum et al. 2023, Gastroenterology.

Return the thirteen items as a table, followed by any observation the thirteen items have no room for. Do not ask clarifying questions and do not comment on the exercise.
```

---

## Paper 14

```
You are acting as an independent second rater in a formal reliability study. Three files are attached. One is a published research paper. The other two are the rating instructions and the operational definitions that govern this exercise.

Read RATER_INSTRUCTIONS.md in full and follow it exactly. Keep DEFINITIONS.md open for item 9. Score the attached paper against all thirteen checklist items.

For each item return four fields. The item number. A verdict, which is one of Yes, No, Unclear or N/A and nothing else. A confidence, which is one of High, Medium or Low. And a note.

For a verdict of Yes or No, the note must contain a locator, meaning the section name or page number, and a verbatim quotation from the attached paper that settles the item. Quote, do not paraphrase. If you cannot find and quote supporting text in the attached paper, return Unclear rather than answering from prior knowledge of this paper or its reputation. This rule is absolute.

For a verdict of Unclear, state which specific fact is missing and where in the paper you looked for it. For a verdict of N/A, state the item class you are invoking and the design feature that triggers it, and note that N/A is available only where the item class table in the instructions permits it.

Where a verdict was close, say so and say what the alternative was.

Before scoring, confirm the first author, the journal, the year and the study design from page one of the attached file. Report what you found. If any of the four disagrees with the citation given below, stop and say so rather than scoring.

Paper number 14. Citation as recorded: Liu et al. 2025, J Am Heart Assoc (CARDIOLOGIST).

Return the thirteen items as a table, followed by any observation the thirteen items have no room for. Do not ask clarifying questions and do not comment on the exercise.
```
