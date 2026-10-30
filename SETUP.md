# Setup Guide — AI Research Excellence System (ARES)

## Quick Start (5 minutes to first prompt)

1. **Copy MASTER_PROMPT.md** → paste as your Claude system prompt
2. **State your research area**: "I'm working on [TOPIC]"
3. **Activate your needed skill**: "ACTIVATE: IDEATION"
4. **Follow the structured output** → iterate from there

## Integration with Claude Projects

1. Create a new Claude Project
2. Paste `MASTER_PROMPT.md` as the project system prompt
3. Upload relevant papers as project knowledge
4. Each conversation begins with the ARIA framework active

## Best Practices

**DO:**
- Be specific about your research area, constraints, and target journal
- Provide your actual results/data/text for analysis
- Ask for the adversarial review BEFORE submission
- Use multiple skill activations in sequence for a full paper
- Run the Quality Fortress on every manuscript before submission
- Pre-register your study design (Methodology Architect can generate the pre-registration)
- Use the full five-step cognitive architecture for complex decisions
- Iterate — the best papers are not written in one pass

**DON'T:**
- Skip the IDEATION phase (a weak question produces a weak paper)
- Skip the QUALITY phase (self-review is insufficient)
- Ask for "a complete paper" in one prompt (iterate through phases)
- Ignore the adversarial feedback (it's designed to save your submission)
- Claim novelty without running the Novelty Certificate protocol
- Overclaim in the discussion (the Logician reviewer will catch you)
- Forget to pre-register (reviewers at top journals will ask)
- Submit without running the Ethics & Compliance checklist

## Skill Combination Matrix

| Task | Skills to Activate |
|------|-------------------|
| Starting from scratch | IDEATION → LITERATURE → METHODOLOGY |
| Have data, need to write | DATA → WRITING → QUALITY |
| Almost ready to submit | QUALITY → JOURNAL → CITATION |
| Just got reviewer comments | QUALITY (revision mode) → JOURNAL |
| Post-acceptance | IMPACT |
| Full paper from idea | All 10 in sequence |
| Rapid publication needed | IDEATION → LITERATURE → METHODOLOGY → DATA → WRITING → QUALITY (compressed timeline) |
| Interdisciplinary project | IDEATION (with adjacency scan focus) → LITERATURE → METHODOLOGY (cross-domain design) |
| Replication study | IDEATION → LITERATURE → METHODOLOGY (with pre-registration emphasis) → ETHICS |

## Workflow Timelines

### Standard Timeline (28 weeks)
```
WEEK 1-2:    IDEATION     → Research question + novelty validation
WEEK 3-6:    LITERATURE   → Systematic review + related work draft
WEEK 7-10:   METHODOLOGY  → Study design + pre-registration
WEEK 11-20:  DATA         → Collection + analysis + figures
WEEK 21-24:  WRITING      → Full draft (Introduction → Discussion)
WEEK 25-26:  QUALITY      → Adversarial peer review simulation
WEEK 27:     STRATEGY     → Journal selection + cover letter
WEEK 28:     SUBMISSION   → Final check + submit
```

### Rapid Publication Timeline (30 days)
See `workflows/RAPID_PUBLICATION.md` for the compressed protocol.

## Journal Quick Reference

| Journal/Venue | Impact Factor (2025 JCR) | Accept Rate (latest cycle) | Turnaround | Best For |
|---------------|--------------------------|----------------------------|------------|----------|
| Nature | 56.1 | ~7% | 6-8 mo | Any breakthrough science |
| Science | 45.8 (2024 JCR) | ~7% | 6-8 mo | Any breakthrough science |
| NEJM | 84.5 | ~5% | 3-4 mo | Clinical medicine |
| Cell | 45.1 | ~7% | 4-6 mo | Life sciences |
| NeurIPS | Premier ML conference | 24.5% (2025) | ~6 mo | ML, Deep Learning |
| ICML | Premier ML conference | 26.9% (2025) | ~6 mo | ML, Theory |
| ICLR | Premier ML conference | 32% (2025) | ~6 mo | Representation learning |
| PNAS | 9.5 | ~13% (direct submissions) | 4-6 mo | Multidisciplinary |
| Nature Machine Intelligence | 29.8 | ~10% | 4-6 mo | AI |
| JMLR | Premier ML journal | selective | 3-6 mo | ML theory/methods |
| ACM CCS | Premier security conference | ~18% | 4-6 mo | Computer security |
| CHI | Premier HCI conference | ~25% | 4-6 mo | Human-computer interaction |

*Journal impact factors reflect the 2025 Journal Citation Reports release (June 2026), verified against publisher metric pages in October 2026. Science's 2025 JIF was not yet retrievable; its 2024 value is shown. Acceptance rates for journals are approximate editor-reported figures; conference rates are official published statistics for the most recent completed cycle.*

## Troubleshooting

**Problem**: The IDEATION phase is producing incremental questions.
**Solution**: Focus on the Contrarian Probe and Adjacency Scan sub-phases. Look for assumptions everyone holds and adjacent fields that have solved structurally similar problems.

**Problem**: The LITERATURE phase is producing summaries instead of synthesis.
**Solution**: Explicitly invoke the Anti-Summary Protocol. Demand that every paragraph ends with an implication for YOUR work, not just a description of prior work.

**Problem**: The QUALITY review is too harsh / producing REJECT verdicts.
**Solution**: This is working as designed. Use the Revision Priority Order to address the most critical issues first. Most papers can move from REJECT to MAJOR REVISION with focused effort on the top 2-3 issues.

**Problem**: I'm not sure which journal to target.
**Solution**: Run the Journal Strategy venue selection matrix. Score 5-7 candidate journals on all 5 dimensions (Scope Fit, Audience Fit, Impact Match, Method Affinity, Strategic Value). The scores will make the right choice clear.

---

*ARES v3.0 — October 2026 — Setup guide for the world's most advanced research paper creation framework.*
