# Step 6 of 12 — Write the methods

| | |
|:---|:---|
| **Phase** | 2 · Write the paper (Week 3) |
| **Time** | ≈ 2 hours |
| **Deliverable** | A complete Methods draft that passes the five-category audit |
| **Before you start** | [Step 5](step_05_write_the_literature_review.md) complete, and your study design decided |

> **The one idea of this step:** the Methods section is a *reproducibility contract*. The
> test is not "sounds scientific" — the test is: **could a competent stranger rerun this
> study from the text alone?**

## Why this step matters

Ask editors what most often sinks an otherwise sound paper: *"the methods are
under-specified."* Every missing detail is a reviewer question, and every reviewer question is
a round of revision you could have avoided. Writing Methods *early* — before Results and
Introduction — is also the professional's ordering trick: it is the section you already know
in perfect detail, it is mostly past-tense reporting, and finishing it gives you momentum.

## What you will do

Write the section in the order a stranger would need it: materials → procedure → measures →
analysis → ethics. Past tense throughout. Voice (passive vs. "we") follows the venue — match
two recent papers from your target journal (Step 11 refines the choice; approximate now).

## Your work

### Work 6.1 — Draft, category by category (≈60 min)

The five categories of the completeness audit — draft each as its own labeled block:

```text
MATERIALS   What, how much, from where, which version/lot/vendor + availability statement
PROCEDURE   Ordered steps; who did what; randomization/blinding where applicable
PARAMETERS  Every number with units AND the reason for its value (or a sensitivity note)
STATISTICS  Test, effect size, significance threshold, software + version
ETHICS      Approval number, consent procedure, pre-registration ID if any
```

### Work 6.2 — The completeness audit (≈30 min)

Check your draft against the audit — mark each row pass/fail and repair every fail:

| Category | The question | Common beginner fail |
|:---|:---|:---|
| Materials | Versions and sources named? | "statistical software" without name/version |
| Procedure | Steps ordered and complete? | "data were cleaned" — how, exactly? |
| Parameters | Values + justification? | "we used α = 0.05" with no word on why |
| Statistics | Effect size + test assumptions? | p-values with no effect sizes anywhere |
| Ethics | Numbers and IDs present? | "approval was obtained" with no IRB number |

### Work 6.3 — The stranger-rerun test (≈30 min)

Hand the draft to a colleague (or paste it to your AI assistant with the ARES prompt loaded and
run `skills/05_writing_excellence/methods_precision.md`) and ask one question: *"Rerun this
study — what can't you replicate?"* Everything they name goes back into Work 6.1.

## Practice example — one audit fix (hypothetical study)

```text
BEFORE: "Students took weekly quizzes and later a final exam; scores were compared."
AUDIT:  Materials ✓ (quiz platform named) · Procedure ✗ (how many quizzes? when? how long?)
        Parameters ✗ (none given) · Statistics ✗ (compared how?) · Ethics ✓
AFTER:  "Students in the treatment arm completed 10-minute weekly quizzes on the course LMS
        (12 quizzes, weeks 1–12, identical item counts); controls restudied the same material
        for 10 timed minutes. Primary outcome: standardized final exam (100 items). Scores
        compared by ANCOVA adjusting for midterm, α = 0.05, Cohen's d reported; analysis in
        R 4.4. Course approval #EDU-2026-041; consent obtained per syllabus policy."
```

Same study, 4 lines instead of 1 — and zero questions left for a reviewer to ask.

## Exit test

- [ ] All five audit categories pass
- [ ] Stranger-rerun test returns "nothing blocking"
- [ ] Every statistical claim names its effect size and software version

## Going deeper

- Written guide: [`../07_SECTION_GUIDES/06_methods.md`](../07_SECTION_GUIDES/06_methods.md)
- Ref-n-Write video #5 + notes: [`../02_VIDEO_COURSES/video_notes/video_05_materials_methods.md`](../02_VIDEO_COURSES/video_notes/video_05_materials_methods.md)
- Grad Coach's methodology videos (strongest free treatment):
  [`../02_VIDEO_COURSES/03_grad_coach.md`](../02_VIDEO_COURSES/03_grad_coach.md)

**Companion manual:** [Roadmap §3.5 Materials & Methods](../THE_WRITING_ROADMAP.md#35-materials--methods--written-first) — the full treatment with sources.

**Next:** [Step 7 — Write the results →](step_07_write_the_results.md)
