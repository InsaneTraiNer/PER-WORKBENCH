# Project Notebook — Experiment Log

## Experiment Record Template

```markdown
### Experiment ID: EXP-####
- **Date:** YYYY-MM-DD
- **Question:** [What specific technical or architectural question is being tested?]
- **Hypothesis:** [What is the expected behavior or outcome?]
- **Objective:** [What is the practical goal of this experiment?]
- **Inputs:** [List input documents, source files, prompt parameters, or data items]
- **Model(s):** [Models involved and their specific assigned roles]
- **Procedure:** [Step-by-step procedure executed during the experiment]
- **Expected Result:** [Anticipated output or benchmark criteria]
- **Observed Result:** [Actual empirical findings or outputs produced]
- **Failure Modes:** [Observed degradations, hallucinations, errors, or limits]
- **Conclusion:** [Analytical synthesis of the experiment outcome]
- **Next Action:** [Downstream operational or structural action based on results]
- **Status:** [PLANNED | IN_PROGRESS | COMPLETED | FAILED]
```

---

## Active & Historical Experiments

### Experiment ID: EXP-0001
- **Date:** 2026-09-17
- **Question:** Can the V1 PER Workbench repository model execute a complete, bounded end-to-end evidence pipeline (SOURCE → EVIDENCE → REQUIREMENTS → ANALYSIS → PROJECT → PER → QA → REVIEW → OUTPUT) using a single real-world Visalia water source without architectural modification or factual fabrication?
- **Hypothesis:** The V1 structure and schema templates are sufficient to capture provenance, discrete claims, statutory requirements, mathematical derivations, draft PER sections, adversarial QA audits, and review dispositions with unbroken backward traceability.
- **Objective:** Empirically validate the operational viability of the V1 architecture on a minimal vertical slice.
- **Inputs:**
  - Source: Cal Water 2020 Urban Water Management Plan (Visalia District), June 2021 (`SRC-0001`).
  - Target: Visalia Main Public Water System (PWSID CA5410016).
- **Model(s):**
  - Perplexity (Source Discovery & Verification)
  - Claude (Primary Production Drafting & Claim Extraction)
  - Gemini (System Audit & Agentic Implementation Operator)
  - Grok (Adversarial QA Auditing Perspective)
- **Procedure:**
  1. Catalog primary source document into `source_registry.md` (`SRC-0001`).
  2. Extract granular, verified claims into `claims.md` (`CLM-0001`, `CLM-0002`).
  3. Formulate statutory requirements in `requirements.md` (`REQ-0001`).
  4. Perform mathematical engineering calculation in `analysis.md` (`ANL-0001`).
  5. Populate normalized project profile in `project_profile.md`.
  6. Assemble draft section with backward traceability matrix in `sections/section_2_existing_facilities.md`.
  7. Conduct adversarial verification, calculation check, and assumption audit in `qa_log.md` (`QA-0001`).
  8. Record human/governance review disposition in `review_log.md` (`REV-0001`).
  9. Package deliverables and release manifest in `03_OUTPUTS/visalia_city_water/manifest_v1_slice.md`.
- **Expected Result:** Every pipeline stage completes cleanly; identifiers link backward to preceding stages; Stop Rule is not triggered.
- **Observed Result:** All 9 stages completed successfully. 100% backward traceability achieved. Stated assumptions (uniform daily demand) were flagged and documented by QA. AI authority disclaimers preserved.
- **Failure Modes:** None encountered. No architectural deficiencies, template incompatibilities, or schema limitations detected during execution.
- **Conclusion:** The V1 PER Workbench architecture is operationally sound and fully capable of maintaining data integrity, provenance, and governance separation across an end-to-end vertical slice.
- **Next Action:** Ingest secondary source documents (e.g. Mid-Kaweah GSA GSP, CPUC General Rate Case engineering exhibits, and water quality Consumer Confidence Reports) to evaluate multi-source conflict reconciliation.
- **Status:** COMPLETED
