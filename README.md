# AI Research Excellence System (ARES)

<p align="center">
  <img src="https://img.shields.io/badge/Release-v3.0%20(October%202026)-0052CC?style=for-the-badge&logo=git&logoColor=white" alt="Release Version" />
  <img src="https://img.shields.io/badge/Engine-ARIA%20v3.1-4B0082?style=for-the-badge&logo=openai&logoColor=white" alt="ARIA v3.1" />
  <img src="https://img.shields.io/badge/License-MIT-28A745?style=for-the-badge&logo=open-source-initiative&logoColor=white" alt="MIT License" />
  <img src="https://img.shields.io/badge/Compatibility-Claude%203.5%20%7C%203.7%20%7C%204-D97706?style=for-the-badge&logo=anthropic&logoColor=white" alt="Claude Compatibility" />
  <img src="https://img.shields.io/badge/Provenance-Empirical%20DOIs%20%26%20Real%20Data-10B981?style=for-the-badge&logo=google-scholar&logoColor=white" alt="Empirical Data Provenance" />
  <img src="https://img.shields.io/badge/Evaluators-4%20Quantitative%20Engines-7C3AED?style=for-the-badge&logo=speedtest&logoColor=white" alt="4 Evaluators" />
</p>

> **ARES is a complete AI-powered operating system for research papers** — a set of battle-tested prompts, skills, evaluators, templates, and workflows that take you from a raw idea to a submission-ready manuscript for *Nature*, *Science*, *Cell*, *NEJM*, *NeurIPS*, *ICML*, *ICLR*, *IEEE*, and *ACM*. No plugins. No setup scripts. Just Markdown files that work with any capable LLM.

---

## Table of Contents

1. [What Is ARES?](#what-is-ares)
2. [Why Does ARES Exist?](#why-does-ares-exist)
3. [The System Map (Visual Overview)](#the-system-map-visual-overview)
4. [Beginner's Step-by-Step Guide](#beginners-step-by-step-guide)
5. [Repository Architecture](#repository-architecture)
6. [The 10 Research Skills](#the-10-research-skills)
7. [Quantitative Evaluator Suite (0–100 Rubrics)](#quantitative-evaluator-suite-0100-rubrics)
8. [Conference-Grade Expert Paper Review (Skill 06)](#conference-grade-expert-paper-review-skill-06)
9. [Production Workflows](#production-workflows)
10. [Walkthrough Examples & Real-World Provenance](#walkthrough-examples--real-world-provenance)
11. [How the Real-World Datasets Are Collected & Verified](#how-the-real-world-datasets-are-collected--verified)
12. [Publisher & Venue Templates](#publisher--venue-templates)
13. [Skill Combination & Activation Matrix](#skill-combination--activation-matrix)
14. [ARIA Cognitive Architecture & Quality Floor](#aria-cognitive-architecture--quality-floor)
15. [Claude Desktop & Claude Projects Setup](#claude-desktop--claude-projects-setup)
16. [Version History](#version-history)
17. [Author & Community](#author--community)
18. [Citation](#citation)

---

## What Is ARES?

**ARES = AI Research Excellence System.** It is a repository of **40+ modular Markdown documents** that turn a general-purpose AI assistant (Claude, or any capable LLM) into a disciplined research partner. Each file is a *prompt engine* with a precise job:

| Layer | What it does | Example |
|:---|:---|:---|
| **1 Master Prompt** | Installs the "ARIA" cognitive engine | `MASTER_PROMPT.md` |
| **10 Skills** | Executed one at a time, on command | Ideation, Writing, Quality Fortress… |
| **4 Evaluators** | Score your manuscript 0–100 | Novelty, Rigor, Clarity, Impact |
| **4 Workflows** | End-to-end pipelines with timetables | 28-week full paper, 30-day rapid |
| **7 Templates** | Venue-exact formatting blueprints | Nature, Science, NeurIPS, IEEE… |
| **4 Examples** | Full worked papers with real datasets | CS, biomedical, social science, interdisciplinary |

**In one sentence:** *you paste the master prompt into your AI assistant once, then walk through skills and evaluators like stations on an assembly line until your paper is ready for submission.*

---

## Why Does ARES Exist?

Generic LLM prompt collections produce shallow summaries, hallucinated citations, and boilerplate prose that elite reviewers reject in minutes. ARES takes the opposite approach:

1. **Epistemic Depth Over Summaries** — every skill forces causal depth, hypothesis falsifiability, boundary-condition stress-testing, and a strict anti-summary standard.
2. **Multi-Agent Adversarial Peer Review** — simulates a hostile editorial board (Methodologist, Domain Expert, Logician, Communicator, Impact Assessor) *before* real reviewers see your work.
3. **Rigorous Quantitative Evaluators** — four independent 0–100 engines with numeric go/no-go gates: Novelty (≥70), Rigor (≥75), Clarity (≥80), Impact (≥75).
4. **Empirical Dataset Provenance** — every example and protocol cites **verified real-world datasets, trials, and DOI registries** (see [provenance section](#how-the-real-world-datasets-are-collected--verified)). Fabricated identifiers are treated as critical flaws and removed.
5. **Universal Venue Alignment** — native formatting blueprints for the world's most demanding publishers, checked against their current author guides.

---

## The System Map (Visual Overview)

```text
                                    ┌─────────────────────────────┐
                                    │   YOUR RESEARCH IDEA /       │
   YOU                             │   EXISTING DRAFT             │
                                    └──────────────┬──────────────┘
                                                   │
                                                   ▼
                         ┌───────────────────────────────────────────┐
                         │      MASTER_PROMPT.md  (ARIA v3.1)        │
                         │   Install once — the 5-step cognitive     │
      STEP 1 — INSTALL ─▶ │   engine that runs before every response  │
                         └───────────────────┬───────────────────────┘
                                             │
              ┌──────────────────────────────┼──────────────────────────────┐
              │                              │                              │
              ▼                              ▼                              ▼
   ┌────────────────────┐        ┌────────────────────┐        ┌────────────────────┐
   │   SKILLS (01–10)   │        │    WORKFLOWS (4)    │        │   TEMPLATES (7)    │
   │  Execute on demand │        │ End-to-end pipelines│        │ Venue-exact format │
   │  ACTIVATE: X       │        │ 28-wk / 30-day /    │        │ Nature, Science,   │
   │                    │        │ Interdisc. / Repl. │        │ NeurIPS, IEEE, ACM,│
   │ 01 Ideation        │        │                     │        │ Springer, arXiv    │
   │ 02 Literature      │        │                     │        └────────────────────┘
   │ 03 Methodology     │        │                     │
   │ 04 Data            │        │                     │
   │ 05 Writing         │        │                     │
   │ 06 Quality         │        │                     │
   │ 07 Journal          │        │                     │
   │ 08 Ethics          │        │                     │
   │ 09 Citation        │        │                     │
   │ 10 Impact          │        │                     │
   └─────────┬──────────┘        └─────────┬──────────┘
             │                             │
             ▼                             ▼
   ┌─────────────────────────────────────────────────┐
   │         EVALUATORS (0–100, with gates)          │
   │  Novelty ≥70 · Rigor ≥75 · Clarity ≥80 · Impact ≥75
   └───────────────────────┬─────────────────────────┘
                           ▼
   ┌─────────────────────────────────────────────────┐
   │              SUBMISSION-READY PAPER               │
   │        (+ rebuttals, cover letters, policy       │
   │         briefs, and follow-up agenda)            │
   └─────────────────────────────────────────────────┘
```

---

## Beginner's Step-by-Step Guide

**Never used an AI assistant for research? Follow exactly these five steps.**

### Step 1 — Get the system (2 minutes)

```bash
# Clone the repository to your computer
git clone https://github.com/AdilShamim8/ARES.git
cd ARES
```

*(Or click the green **Code → Download ZIP** button on GitHub if you don't use git.)*

### Step 2 — Install ARIA (2 minutes)

Open [`MASTER_PROMPT.md`](MASTER_PROMPT.md) and copy **everything inside the boxed prompt block**. Then either:

- **Claude Projects (recommended):** Create a new project in Claude → paste the block into **Project Instructions** → add your domain papers to **Project Knowledge**. ARIA stays active in every chat inside the project.
- **Plain chat:** Paste the block as the **very first message** of a new conversation.

### Step 3 — State your topic (1 minute)

Tell the system what you are working on — be specific:

> *"I'm working on sample-efficient graph neural networks for drug-target affinity prediction, targeting Nature Machine Intelligence."*

No topic yet? Just say: *"Help me find a high-novelty research question in [field]."*

### Step 4 — Activate skills like switches

Type one command, get one structured deliverable:

```
ACTIVATE: IDEATION      →  gap analysis + novelty certificate (0–100)
ACTIVATE: LITERATURE    →  systematic review + citation cartography
ACTIVATE: METHODOLOGY   →  experimental design + pre-registration
ACTIVATE: DATA          →  statistical audit + publication figures
ACTIVATE: WRITING       →  section-by-section drafting engine
ACTIVATE: QUALITY       →  5-reviewer adversarial review + meta-review
ACTIVATE: JOURNAL       →  venue decision matrix + cover letter
ACTIVATE: ETHICS       →  integrity, IRB & compliance checklist
ACTIVATE: CITATION      →  balanced, hallucination-free bibliography
ACTIVATE: IMPACT        →  press release, policy brief, social threads
```

### Step 5 — Iterate until the gates are green

Run the evaluators, check the 0–100 scores, fix what the reviewers-in-simulation found, and repeat. A typical full paper follows this loop:

```
IDEATION → LITERATURE → METHODOLOGY → (run your study) → DATA
        → WRITING → QUALITY → JOURNAL → CITATION → submit
```

**That's it.** The rest of this README is a reference map of what each command produces.

---

## Repository Architecture

```
ARES/
├── README.md                              ← You are here — system overview & master index
├── MASTER_PROMPT.md                       ← ARIA master cognitive system prompt (install first)
├── SETUP.md                               ← Installation, best practices & verified journal data
├── ARES_MASTER_REPO.md                    ← Consolidated single-file reference manual
│
├── skills/                                ← 10 core research mastery engines
│   ├── 01_ideation/                       ← Breakthrough question & gap discovery
│   ├── 02_literature_command/             ← Systematic review & citation synthesis
│   ├── 03_methodology_architect/          ← Experimental design & threat modeling
│   ├── 04_data_intelligence/             ← Statistical analysis & visual grammar
│   ├── 05_writing_excellence/             ← Publication-grade scientific prose
│   ├── 06_quality_fortress/               ← Conference-grade review, 11-dim audit & VLM
│   ├── 07_journal_strategy/               ← Venue selection & cover letter strategy
│   ├── 08_ethics_compliance/              ← Research integrity, IRB & compliance
│   ├── 09_citation_mastery/              ← Citation cartography & balance
│   └── 10_impact_amplifier/               ← Post-publication dissemination & policy
│
├── evaluators/                            ← 4 quantitative manuscript assessment engines
│   ├── NOVELTY_SCORE_RUBRIC.md            ← 5-axis 0–100 novelty rubric   (gate: ≥70)
│   ├── RIGOR_RUBRIC.md                    ← 5-axis 0–100 rigor rubric     (gate: ≥75)
│   ├── CLARITY_ANALYZER.md                ← 6-axis 0–100 clarity rubric   (gate: ≥80)
│   └── IMPACT_PREDICTOR.md                ← 5-axis 0–100 impact predictor (gate: ≥75)
│
├── workflows/                             ← End-to-end execution pipelines
│   ├── FULL_PAPER_WORKFLOW.md             ← 28-week A-to-Z manuscript lifecycle
│   ├── RAPID_PUBLICATION.md               ← 30-day fast-track protocol
│   ├── INTERDISCIPLINARY.md               ← Cross-domain translation framework
│   └── REPLICATION_STUDY.md               ← Pre-registered replication protocol
│
├── templates/                             ← Production manuscript templates by venue
│   ├── Nature_Family.md                   ← Nature & Nature Portfolio (2,500–4,300 words, 6–8 pages)
│   ├── Science.md                         ← Science (AAAS) research articles & reports
│   ├── NeurIPS_ICML_ICLR.md               ← Top-tier ML conference formats (9-page NeurIPS 2026)
│   ├── IEEE.md                            ← IEEE Transactions double-column specifications
│   ├── ACM.md                             ← ACM SIGCONF & TOCS format guidelines
│   ├── Springer.md                        ← Springer LNCS & journal standards
│   └── arXiv.md                           ← High-impact open preprint formatting
│
└── examples/                              ← Worked exemplar papers with real datasets
    ├── computer_science.md                ← CS/AI: MENTOR LLM Reasoning (GSM8K, SVAMP, StrategyQA)
    ├── biomedical.md                      ← Biomed: CRISPR HSC Off-Target (NCT03745287, BCL11A)
    ├── social_science.md                  ← SocSci: Social Media Deliberation (N=1,500, DCI, DQI)
    └── interdisciplinary.md               ← Interdisc.: BioPhysiFold AI Drug Design (ChEMBL, PDB)
```

---

## The 10 Research Skills

Each skill directory contains an authoritative `SKILL.md` plus specialized modular prompts and actionable checklists:

| Skill | Module Name | Primary Objective | Activation Command | Key Deliverables |
|:---:|:---|:---|:---|:---|
| **01** | [Ideation Engine](skills/01_ideation/SKILL.md) | Formulate high-novelty, falsifiable research questions | `ACTIVATE: IDEATION` | Gap Analysis Matrix, Hypothesis Forge, Novelty Score |
| **02** | [Literature Command](skills/02_literature_command/SKILL.md) | Synthesize vast corpuses without descriptive summaries | `ACTIVATE: LITERATURE` | Systematic Review Protocol, Citation Cartography |
| **03** | [Methodology Architect](skills/03_methodology_architect/SKILL.md) | Build bulletproof experimental designs & pre-registrations | `ACTIVATE: METHODOLOGY` | Threat-to-Validity Matrix, Statistical Power Plan |
| **04** | [Data Intelligence](skills/04_data_intelligence/SKILL.md) | Extract deep statistical signal & design publication figures | `ACTIVATE: DATA` | Effect Size Architecture, Publication Figure Specs |
| **05** | [Writing Excellence](skills/05_writing_excellence/SKILL.md) | Draft prose that compels reviewers from line one | `ACTIVATE: WRITING` | Abstract Blueprint, Introduction Arc, Discussion Defense |
| **06** | [Quality Fortress](skills/06_quality_fortress/SKILL.md) | Conference-grade peer review, 11-dimension audit, VLM visual review & PeerRead 100-pool benchmark | `ACTIVATE: QUALITY` | 11-Dim Audit, VLM Figure Aesthetics, PeerRead Relative Rank (83.8% Acc), Meta-Review |
| **07** | [Journal Strategy](skills/07_journal_strategy/SKILL.md) | Optimize venue selection, editorial pitch & cover letters | `ACTIVATE: JOURNAL` | Venue Decision Matrix, Editor Cover Letter Blueprint |
| **08** | [Ethics & Compliance](skills/08_ethics_compliance/SKILL.md) | Guarantee integrity, transparency, IRB, and dual-use safety | `ACTIVATE: ETHICS` | Compliance Checklist, Data Management Plan (FAIR) |
| **09** | [Citation Mastery](skills/09_citation_mastery/SKILL.md) | Engineer comprehensive, balanced, and strategic citations | `ACTIVATE: CITATION` | Citation Balance Audit, Recency & Lineage Mapping |
| **10** | [Impact Amplifier](skills/10_impact_amplifier/SKILL.md) | Drive post-publication citations, policy translation & media | `ACTIVATE: IMPACT` | Science Communication Brief, Policy Translation Memo |

---

## Quantitative Evaluator Suite (0–100 Rubrics)

ARES ships a dedicated quantitative evaluation suite in [`evaluators/`](evaluators/) to audit manuscripts before submission. Every evaluator computes a weighted score out of 100 with explicit go/no-go acceptance gates:

```
                  ┌───────────────────────────────┐
                  │    ARES EVALUATION SUITE      │
                  └───────────────┬───────────────┘
                                  │
         ┌────────────────┬───────┴────────┬────────────────┐
         ▼                ▼                ▼                ▼
  NOVELTY SCORE      RIGOR SCORE     CLARITY SCORE    IMPACT PREDICTION
   (Rubric ≥70)    (Rubric ≥75)    (Rubric ≥80)      (Rubric ≥75)
         │                │                │                │
         └────────────────┼────────────────┴────────────────┘
                                  │
                                  ▼
                     [PEER REVIEW SUBMISSION GATE]
```

### 1. [Novelty Score Rubric](evaluators/NOVELTY_SCORE_RUBRIC.md)
- **5 weighted dimensions**: Conceptual Novelty (25%), Methodological Novelty (25%), Empirical Novelty (20%), Translational Utility (15%), Interdisciplinary Synthesis (15%).
- **Gate for top-tier venues**: score **≥ 70/100**.

### 2. [Rigor Rubric](evaluators/RIGOR_RUBRIC.md)
- **5 weighted dimensions**: Internal & External Validity (25%), Statistical Power & Inference (25%), Reproducibility & Open Science (20%), Baseline Fairness (15%), Boundary Conditions (15%).
- **Mandatory submission threshold**: **≥ 75/100**.

### 3. [Clarity Analyzer](evaluators/CLARITY_ANALYZER.md)
- **6 dimensions**: Macro-Structure (20%), Sentence-Level Micro-Clarity (20%), Cognitive Load (15%), Visual Grammar (15%), Terminology Precision (15%), Abstract Calibration (15%).
- **Target standard**: **≥ 80/100**.

### 4. [Impact Predictor](evaluators/IMPACT_PREDICTOR.md)
- **5 dimensions**: Theoretical Influence (25%), Method & Tool Adoption (25%), Cross-Disciplinary Diffusion (20%), Translational & Policy Utility (15%), Field-Shaping Longevity (15%).
- **High-impact trajectory**: **≥ 75/100**.

---

## Conference-Grade Expert Paper Review (Skill 06)

[`skills/06_quality_fortress/`](skills/06_quality_fortress/) evaluates manuscripts at the level of senior area chairs and editorial boards. It accepts **LaTeX (`.tex`), PDF (`.pdf`), Word (`.docx`), and Markdown (`.md`)**, and runs a security scan, an 11-dimension technical audit with VLM figure inspection, and a PeerRead-calibrated competitiveness score:

```
                  ┌───────────────────────────────┐
                  │    MANUSCRIPT SUBMISSION      │
                  │   (.tex, .pdf, .docx, .md)    │
                  └───────────────┬───────────────┘
                                  │
         ┌────────────────────────┼────────────────────────┐
         ▼                        ▼                        ▼
  SECURITY SCAN            11-DIMENSION & VLM       EMPIRICAL DATASET
• Prompt-injection       • Logic & Claims         • PeerRead (14,784 drafts)
• Unicode Cf / zero-width• Cross-table consistency• 100-Pool Benchmark (83.8%)
• Double-blind leaks     • VLM Figure Aesthetics  • AAAI 2026 calibration
• Metadata sanitation    • Math notation clashes  • NeurIPS 21-pt checklist
         │                        │                        │
         └────────────────────────┼────────────────────────┘
                                  ▼
                 ┌─────────────────────────────────┐
                 │  MULTI-AGENT CONSENSUS MATRIX   │
                 │   & RELATIVE RANK SCORE (R_comp)│
                 └─────────────────────────────────┘
```

### The 11-Dimension Audit Framework
**[A]** Logic & Argumentation · **[B]** Empirical Rigor & Cross-Table Consistency · **[C]** Writing Quality & Rhetorical Momentum · **[D]** Citation Cartography (zero hallucinated references) · **[E]** Mathematical & Notational Integrity · **[F]** Double-Blind & Anonymity Compliance · **[G]** Venue Formatting & Standards · **[H]** Academic Tone Purity & Anti-AI Smell · **[I]** Narrative Structure & Hierarchy · **[J]** Reviewer Red Flags & Puffery · **[K]** Visual & Figure Aesthetics (VLM multi-modal: ≥300 DPI, colorblind-safe palettes, 30-second caption rule).

### Multi-Platform Activation Triggers
`ACTIVATE: QUALITY` · `review my paper` · `审稿` · `@ai-review`

Full operational guide with before/after case studies: [`skills/06_quality_fortress/expert_paper_reviewer.md`](skills/06_quality_fortress/expert_paper_reviewer.md)

---

## Production Workflows

Four battle-tested end-to-end pipelines in [`workflows/`](workflows/):

| Workflow | Timeline | Use When |
|:---|:---|:---|
| **[Full Paper Lifecycle](workflows/FULL_PAPER_WORKFLOW.md)** | 28 weeks, 8 phases | You have a topic and want the maximum-quality A-to-Z pipeline |
| **[Rapid Publication](workflows/RAPID_PUBLICATION.md)** | 30 days | A breakthrough result needs a priority claim without sacrificing rigor |
| **[Interdisciplinary Innovation](workflows/INTERDISCIPLINARY.md)** | Stage-gated | Your work bridges two fields and must satisfy reviewers from both |
| **[Replication & Extension](workflows/REPLICATION_STUDY.md)** | Stage-gated | You are replicating prior work and need pre-registration + equivalence testing |

```
FULL PAPER (28 weeks):   Idea ──▶ Review ──▶ Design ──▶ Pre-reg ──▶ Draft ──▶ Audit ──▶ Submit
RAPID (30 days):         Day 1–3 triage ──▶ Day 4–10 core build ──▶ Day 11–20 draft ──▶ Day 21–30 polish
INTERDISCIPLINARY:       Bridge scan ──▶ Dual-audit ──▶ Shared vocabulary ──▶ Joint methods
REPLICATION:             Pre-register ──▶ Power analysis ──▶ Direct run ──▶ Equivalence test ──▶ Publish
```

---

## Walkthrough Examples & Real-World Provenance

Unlike synthetic tutorials that use dummy variables, ARES features complete, end-to-end exemplar manuscripts in [`examples/`](examples/) grounded in **real, verifiable datasets, clinical trials, and literature**:

| Domain | Exemplar | Research Question | Verified Real-World Data | Verified Primary Sources |
|:---|:---|:---|:---|:---|
| **Computer Science** | [`computer_science.md`](examples/computer_science.md) | *MENTOR: Metacognitive Self-Regulation for Enhanced LLM Reasoning* | **GSM8K** (arXiv:2111.03797), **SVAMP** (arXiv:2103.07191), **StrategyQA** (DOI: 10.1162/tacl_a_00370), **ProofWriter** (Findings ACL 2021), **BIG-bench Hard** (arXiv:2210.09261) | Kang et al. PeerRead (arXiv:1804.09635); Flavell (1979) DOI: 10.1037/0003-066X.34.10.906 |
| **Biomedical** | [`biomedical.md`](examples/biomedical.md) | *Disease-State-Dependent CRISPR Editing Landscapes in Sickle Cell HSCs* | **ClinicalTrials.gov NCT03745287** (CTX001 SCD trial), **GUIDE-seq** (DOI: 10.1038/nbt.3117), **BCL11A +58 erythroid enhancer** | Frangoul 2021 (DOI: 10.1056/NEJMoa2031054), Frangoul 2024 (DOI: 10.1056/NEJMoa2309676), Newby 2021 (DOI: 10.1038/s41586-021-03609-w), Cameron 2017 (DOI: 10.1038/nmeth.4284) |
| **Social Science** | [`social_science.md`](examples/social_science.md) | *Unraveling the Mechanisms: How Social Media Degrades Democratic Deliberation* | **1,124-paper PRISMA corpus**, **three-experiment pre-registration (N=1,500)**, **Discourse Quality Index** (Steenbergen et al. 2003) | Bail 2018 (DOI: 10.1073/pnas.1804840115), Vosoughi 2018 (DOI: 10.1126/science.aap9559), Steenbergen 2003 (DOI: 10.1057/palgrave.cep.6110002) |
| **Interdisciplinary** | [`interdisciplinary.md`](examples/interdisciplinary.md) | *BioPhysiFold: Biophysically-Informed Foundation Models for Drug Discovery* | **ChEMBL Release 37** (2.92M compounds, live-verified Oct 2026), **ZINC20** (DOI: 10.1021/acs.jcim.0c00675), **PubChem** (DOI: 10.1093/nar/gkaa971), **PDBbind v2020** (DOI: 10.1021/acs.accounts.6b00491), **MoleculeNet** (DOI: 10.1039/c7sc02664a) | Stokes 2020 (DOI: 10.1016/j.cell.2020.01.021), Satorras 2022 (DOI: 10.1038/s41467-022-29939-5), Walters & Barzilay 2021 (DOI: 10.1021/acs.accounts.0c00699) |

---

## How the Real-World Datasets Are Collected & Verified

Every empirical number in ARES is traceable to a public dataset, registry, or published paper. This is **how each source was collected, and how you can re-verify every one of them today**:

### The review-calibration datasets (Quality Fortress)

| # | Dataset | What it contains | How it was collected | How to verify (last verified 30 Oct 2026) |
|:---:|:---|:---|:---|:---|
| 1 | **PeerRead** (Kang et al., NAACL 2018, arXiv:1804.09635) | 14,784 paper drafts with accept/reject decisions from ICLR 2017, NeurIPS 2013–2017, ACL 2017; 10.7K drafts include full expert textual reviews | Scraped from public conference proceedings and review archives by the Allen Institute for AI | `github.com/allenai/peerread` · `arxiv.org/abs/1804.09635` |
| 2 | **PeerRead 100-Pool Benchmark** (Ai-Review evaluation) | 100 sampled ICLR 2017 pools used to calibrate the relative-rank engine (83.8% pairwise ordering accuracy) | Pools sampled from PeerRead v1; pairwise ranking evaluated accepted vs. rejected | `skills/06_quality_fortress/expert_paper_reviewer.md` § 5 |
| 3 | **AAAI 2026 reviewer calibration** | Reviewer guidelines, score distributions, decision boundaries from the 40th AAAI conference (Singapore, January 20–27, 2026) | Reverse-engineered from published AAAI 2026 review forms and meta-review records | `aaai.org/conference/aaai/aaai-26/` |
| 4 | **OpenReview venue pools** | Public reviews for ICLR/NeurIPS/ICML/CoRL, 2020–2026 | Downloaded via the OpenReview API | `openreview.net` |
| 5 | **NeurIPS Reproducibility Checklist** (Pineau et al., JMLR 2021) | The standardized 21-point reproducibility audit (assumptions, proofs, compute, error bars, splits) | Published JMLR paper from the NeurIPS reproducibility program | Search "Improving Reproducibility in Machine Learning Research, Pineau, JMLR" |
| 6 | **S2ORC & SciCite** (Lo et al., ACL 2020; Cohan et al., NAACL 2019) | 81M+ full-text papers with classified citation intents (background / method / result) | Semantic Scholar corpus release + citation-intent crowdsourcing | `github.com/allenai/s2orc` · `github.com/allenai/scicite` |

### The exemplar-paper datasets (examples/)

| Dataset | Access point | Verified size / fact | Live check |
|:---|:---|:---|:---|
| GSM8K | `github.com/openai/grade-school-math` | 8,500 grade-school math problems | arXiv:2111.03797 |
| StrategyQA | `allenai.org/data/strategyqa` | 2,780 implicit multi-hop questions | DOI: 10.1162/tacl_a_00370 |
| CTX001 trial | `clinicaltrials.gov/study/NCT03745287` | Phase 1/2/3 CRISPR SCD trial (Vertex) — **completed** | ClinicalTrials.gov API |
| ChEMBL | `ebi.ac.uk/chembl` | Release 37 (May 2026): 2,921,148 distinct compounds, 24.5M activities | `ebi.ac.uk/chembl/api/data/status.json` |
| ZINC20 | `zinc20.docking.org` | Ultralarge purchasable chemical database (lead-like tranche MW 250–350) | DOI: 10.1021/acs.jcim.0c00675 |
| PubChem | `pubchem.ncbi.nlm.nih.gov` | 110M+ compounds; bioactive subsets used in the exemplar | DOI: 10.1093/nar/gkaa971 |
| PDBbind | `pdbbind.org.cn` (v2020 free tier) | v2020 = last freely accessible release; refined set of high-quality complexes | `pdbbind-plus.org.cn` |

### Verification policy

- **DOIs** are resolved against `doi.org` and Crossref; unregistered or mismatched DOIs are treated as *critical flaws* and corrected or removed (this release fixed six).
- **Trial IDs** are resolved against the ClinicalTrials.gov API.
- **Database versions and sizes** are confirmed against live vendor APIs (ChEMBL, PDBbind) — never from memory.
- **Journal metrics** are taken from the latest JCR release and publisher metric pages (see [`SETUP.md`](SETUP.md) for the verified table).
- **Illustrative placeholders** (e.g., a demo pre-registration DOI inside an example) are explicitly labeled `ILLUSTRATIVE` so they can never be mistaken for real registrations.

---

## Publisher & Venue Templates

Structural blueprints in [`templates/`](templates/) reflecting the current editorial criteria of global publishers (limits checked against author guides, October 2026):

- [`Nature_Family.md`](templates/Nature_Family.md) — *Nature* Articles: ~2,500 words (6 pages) to ~4,300 words (8 pages), Methods ≤3,000 words, summary paragraph ≤200 words, modular display items.
- [`Science.md`](templates/Science.md) — *Science* (AAAS) Research Articles (~4,500 words) & Reports (~2,500 words), Methods excluded from Science word counts.
- [`NeurIPS_ICML_ICLR.md`](templates/NeurIPS_ICML_ICLR.md) — single-column 9-page main-text limit (NeurIPS 2026), proofs & error bars, Broader Impact / Ethics statements.
- [`IEEE.md`](templates/IEEE.md) — *IEEE Transactions* two-column format, formal math, complexity analysis.
- [`ACM.md`](templates/ACM.md) — ACM SIGCONF/TOCS formats, CCS concepts, artifact badges.
- [`Springer.md`](templates/Springer.md) — LNCS and Springer Nature monograph standards.
- [`arXiv.md`](templates/arXiv.md) — preprint architecture that maximizes citation velocity.

---

## Skill Combination & Activation Matrix

Combine skills sequentially to match your stage in the research lifecycle:

| Research Objective | Recommended Skill Pipeline | Target Outcome |
|:---|:---|:---|
| **Starting from scratch** | `IDEATION` → `LITERATURE` → `METHODOLOGY` | Bulletproof, high-novelty research design |
| **Data collected, ready to write** | `DATA` → `WRITING` → `QUALITY` | Transform raw results into an executive first draft |
| **Pre-submission audit** | `QUALITY` → `JOURNAL` → `CITATION` | 4-reviewer adversarial audit & formatted submission package |
| **Addressing reviewer rejections / R&R** | `QUALITY (Revision Mode)` → `JOURNAL` | Point-by-point rebuttal matrices and revised text |
| **Post-acceptance outreach** | `IMPACT` | Press releases, policy briefs, social threads |
| **Full paper pipeline** | All 10 skills in sequence (01 → 10) | Comprehensive manuscript for top-0.0001% venues |

---

## ARIA Cognitive Architecture & Quality Floor

Every activation runs the **ARIA 5-Step Cognitive Architecture** before producing output:

```
[STEP 1: SUMMIT SCAN]      → Benchmark against the top 3 papers in the domain over the last 5 years.
[STEP 2: GAP ANALYSIS]     → Identify the critical delta between the current state and the benchmark.
[STEP 3: NON-OBVIOUS BRIDGE]→ Formulate non-trivial, cross-domain insights rather than incremental fixes.
[STEP 4: ADVERSARIAL TEST] → Subject every claim to harsh Reviewer-2 stress tests to preempt critiques.
[STEP 5: SYNTHESIS]        → Integrate multi-disciplinary lenses (physics, economics, ML, biology).
```

### The ARES Quality Floor
- **Evidence Integrity**: every empirical assertion cites reproducible data or is explicitly marked as an untested hypothesis.
- **Methodological Determinism**: experimental steps are precise enough for independent third-party replication.
- **Figure Storytelling**: every chart is fully interpretable by a domain specialist in under 30 seconds.
- **Anti-Summary Standard**: literature reviews synthesize conceptual tension — never produce chronological lists.

---

## Claude Desktop & Claude Projects Setup

### Option A: Claude Projects (recommended)
1. In Claude, navigate to **Projects** → create a new project (e.g., *"Research Excellence — [Your Project]"*).
2. Paste [`MASTER_PROMPT.md`](MASTER_PROMPT.md) into **Project Instructions**.
3. Upload your domain papers, preprints, and dataset documentation into **Project Knowledge**.
4. Start every chat with an activation trigger (e.g., `ACTIVATE: IDEATION`).

### Option B: Claude Desktop / Web
1. Start a new conversation.
2. Paste the ARIA master prompt from [`MASTER_PROMPT.md`](MASTER_PROMPT.md) as the first message.
3. Follow with your research objective and skill triggers.

For API deployments, memory optimization, troubleshooting, and the verified journal quick-reference: [`SETUP.md`](SETUP.md).

---

## Version History

| Version | Date | Highlights |
|:---:|:---|:---|
| **v3.0** | **October 30, 2026** | **Repository renamed CRES → ARES** (AI Research Excellence System) to match the new GitHub home. All 40+ files rebranded; empirical provenance re-verified against live registries on the release date — 6 unregistered/mismatched DOIs corrected, clinical trial ID fixed (NCT03745287), ChEMBL updated to Release 37, PeerRead identifier corrected to arXiv:1804.09635, unverifiable "Poldrack" attribution replaced with the verified AgentReview framework (Jin et al., 2024), journal metrics refreshed to the 2025 JCR release, Nature word-limit guidance aligned with the current author guide, and skill cross-references repaired. New beginner-first README with system maps and dataset-verification guide. |
| v2.4 | September 2026 | VLM multimodal figure review, multi-format manuscript intake (LaTeX/PDF/DOCX/MD), PeerRead 100-pool benchmark (83.8%), conference-grade Quality Fortress upgrade. |
| v2.0 | Earlier 2026 | Ten-skill modular architecture, 4 quantitative evaluators, 4 production workflows, 7 venue templates. |

*All facts, datasets, and metrics in this release were re-verified against primary sources on October 30, 2026 — not from cached knowledge.*

---

## Author & Community

<div align="center">

### ✦ Connect With Me

<p>
  <a href="https://www.adilshamim.me">
    <img src="https://img.shields.io/badge/Portfolio-111111?style=for-the-badge&logo=About.me&logoColor=white" />
  </a>
  <a href="https://linkedin.com/in/adilshamim8">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  <a href="https://adilshamim8.medium.com">
    <img src="https://img.shields.io/badge/Medium-000000?style=for-the-badge&logo=medium&logoColor=white" />
  </a>
  <a href="https://adilshamim.substack.com">
    <img src="https://img.shields.io/badge/Substack-FF6719?style=for-the-badge&logo=substack&logoColor=white" />
  </a>
</p>

<p>
  <a href="https://github.com/AdilShamim8">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
  </a>
  <a href="https://www.kaggle.com/adilshamim8">
    <img src="https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white" />
  </a>
  <a href="https://leetcode.com/u/AdilShamim8">
    <img src="https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=111111" />
  </a>
  <a href="https://twitter.com/adil_shamim8">
    <img src="https://img.shields.io/badge/X-111111?style=for-the-badge&logo=x&logoColor=white" />
  </a>
</p>

<sub>Building • Learning • Researching • Sharing</sub>

</div>

---

## Citation

If ARES enhances your research, methodology design, or publication workflow, please cite:

```bibtex
@software{shamim2026ares,
  author       = {Shamim, Adil},
  title        = {AI Research Excellence System (ARES): An Advanced AI Framework for High-Impact Scientific Publishing},
  year         = {2026},
  month        = {October},
  publisher    = {GitHub},
  version      = {3.0},
  url          = {https://github.com/AdilShamim8/ARES}
}
```

---

<div align="center">

⭐ **If this repository helped you, consider giving it a star!** ⭐

<sub>ARES v3.0 • Engineered for researchers who refuse to settle for "good enough." • Current as of October 30, 2026</sub>

</div>
