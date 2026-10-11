# PER Workbench — Architecture

## 1. V1 Pipeline Diagram

```
+-------------------------------------------------------------------+
|                        1. SOURCE DISCOVERY                        |
|   (Public filings, regulatory records, GIS, utility data)         |
|   Model: Perplexity                                               |
+---------------------------------+---------------------------------+
                                  |
                                  v
+---------------------------------+---------------------------------+
|                       2. EVIDENCE EXTRACTION                      |
|   (Source Registry -> Claims & Grounded Statements)               |
|   Model: Perplexity / Claude                                      |
+---------------------------------+---------------------------------+
                                  |
                                  v
+---------------------------------+---------------------------------+
|                3. REQUIREMENTS & CONSTRAINTS                      |
|   (Regulatory mandates, engineering criteria, funding rules)      |
|   Model: Claude / ChatGPT                                         |
+---------------------------------+---------------------------------+
                                  |
                                  v
+---------------------------------+---------------------------------+
|                  4. ANALYSIS & ENGINEERING SYNTHESIS              |
|   (Demand calculations, alternatives evaluation, cost models)     |
|   Model: Claude (Production)                                      |
|   Orchestration & Framework: ChatGPT                              |
+---------------------------------+---------------------------------+
                                  |
                                  v
+---------------------------------+---------------------------------+
|                 5. ADVERSARIAL QA & RED-TEAMING                   |
|   (Contradiction detection, citation audit, math checks)          |
|   Model: Grok (Adversarial QA)                                    |
|   System Audit / Execution Verification: Gemini                   |
+---------------------------------+---------------------------------+
                                  |
                                  v
+---------------------------------+---------------------------------+
|               6. HUMAN / PE REVIEW & FINAL AUTHORITY              |
|   (Human-in-the-loop engineering judgment, formal sign-off)      |
|   Authority: Licensed Professional Engineers / Human Reviewers    |
+---------------------------------+---------------------------------+
                                  |
                                  v
+---------------------------------+---------------------------------+
|                        7. OUTPUT GENERATION                       |
|   (Preliminary Engineering Report Deliverables)                   |
|   Location: 03_OUTPUTS/visalia_city_water/                        |
+-------------------------------------------------------------------+
```

---

## 2. Repository Hierarchy

```
PER-WORKBENCH/
├── 00_MASTER_DIRECTIVE/        # Core governing principles, architecture, rules
│   ├── 00_Master_Directive.md
│   ├── 01_Mission.md
│   ├── 02_Architecture.md
│   └── 03_Authority_and_Review.md
│
├── 01_PROJECT_NOTEBOOK/        # Temporal progress tracking, execution logs, experiments
│   ├── 00_Project_Index.md
│   ├── Running_Log.md
│   └── 01_Experiments/
│       └── Experiment_Log.md
│
├── 02_REPOSITORIES/            # Information layers, evidence, and report modules
│   ├── 01_SOURCE/              # Canonical source catalog (SRC-####)
│   │   └── source_registry.md
│   ├── 02_EVIDENCE/            # Grounded claims extracted from sources (CLM-####)
│   │   └── claims.md
│   ├── 03_REQUIREMENTS/        # Engineering, regulatory, project requirements (REQ-####)
│   │   └── requirements.md
│   ├── 04_ANALYSIS/            # Structured engineering and technical analyses (ANL-####)
│   │   └── analysis.md
│   ├── 05_PROJECT/             # Normalized profile and parameters of the target project
│   │   └── project_profile.md
│   ├── 06_PER/                 # Preliminary Engineering Report structure and sections
│   │   ├── outline.md
│   │   └── sections/           # Report section drafts (empty initially)
│   ├── 07_QA/                  # Adversarial testing, audit findings, verifications (QA-####)
│   │   └── qa_log.md
│   └── 08_REVIEW/              # Human and professional engineering review records (REV-####)
│       └── review_log.md
│
└── 03_OUTPUTS/                 # Final deliverables and compiled report packages
    └── visalia_city_water/     # Target vertical-slice output directory
```

---

## 3. Model Roster

Model assignments are bounded by specific functional capabilities:

- **Perplexity**: Source discovery, external literature search, regulatory lookup, and factual identification.
- **Claude**: Primary production, technical drafting, evidence synthesis, and report section narrative generation.
- **ChatGPT**: Architecture, orchestration, structural framing, and process facilitation.
- **Gemini**: System audit, agentic execution, filesystem operations, and structural verification.
- **Grok**: Adversarial QA, red-teaming, boundary testing, contradiction hunting, and skepticism audit.
