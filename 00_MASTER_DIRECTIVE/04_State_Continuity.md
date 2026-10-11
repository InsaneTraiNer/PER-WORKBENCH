# PER Workbench — State Continuity & Bootstrap Protocol

## 1. Authority of the Filesystem
- The `PER-WORKBENCH/` filesystem is the single authoritative source of truth (SSOT) and persistent project state.
- Individual AI conversation threads, model context windows, and chat sessions are transient working environments.
- Conversational assumptions, hallucinations, or unpersisted model memory must never override documented project state. Any change to project state requires an explicit, documented update committed to the repository files.

---

## 2. Orientation
When entering the PER Workbench in a new context or session, establish orientation using the foundational governing documents:
- **What the PER Workbench is:** A structured, multi-model agentic workbench for synthesizing, auditing, and authoring defensible Preliminary Engineering Reports (PERs) for civil infrastructure and water systems. (See `00_MASTER_DIRECTIVE/01_Mission.md`)
- **Current V1 Objective:** Execute a minimal, verified vertical slice for an initial infrastructure target without structural bloat or factual fabrication. (See `00_MASTER_DIRECTIVE/01_Mission.md`)
- **V1 Architecture & Pipeline:** Segregated multi-model roles (Perplexity for source discovery, Claude for production drafting, ChatGPT for architecture/orchestration, Gemini for system audit/agentic execution, and Grok for adversarial QA). (See `00_MASTER_DIRECTIVE/02_Architecture.md`)
- **Authority & Review Boundaries:** Strict separation of AI draft work from certified engineering authority. AI models possess zero statutory approval or final engineering design authority. (See `00_MASTER_DIRECTIVE/03_Authority_and_Review.md`)

---

## 3. Current Project State
- **Structural Status:** The V1 filesystem structure has been successfully instantiated.
- **Verification Audit:** Gemini completed the verification audit with zero structural deviations and zero unresolved structural questions.
- **Current Status Code:** `V1 STRUCTURE READY`
- **Next Operational Phase:** Beginning the Visalia City Water vertical slice (primary source ingestion and claim extraction).

---

## 4. State Hierarchy
Information within the Workbench flows strictly according to the following functional hierarchy:
1. `00_MASTER_DIRECTIVE/` → Governing rules, core operating principles, mission, architecture, and authority boundaries.
2. `01_PROJECT_NOTEBOOK/` → Chronological execution tracking, decisions, observations, discoveries, problems, and empirical experiments.
3. `02_REPOSITORIES/` → Authoritative working knowledge layers (sources, evidence claims, requirements, engineering analysis, project profile, PER drafting, QA logs, and human review logs).
4. `03_OUTPUTS/` → Final compiled project deliverables and export artifacts (`visalia_city_water/`).

---

## 5. Fresh-Context Procedure
Any AI session entering the project must execute this sequence before taking action:
1. Read `00_MASTER_DIRECTIVE/00_Master_Directive.md` to review core governing principles.
2. Read `00_MASTER_DIRECTIVE/01_Mission.md` to review project mission and V1 scope.
3. Read `00_MASTER_DIRECTIVE/02_Architecture.md` to review pipeline and model roster.
4. Read `00_MASTER_DIRECTIVE/03_Authority_and_Review.md` to review engineering judgment boundaries.
5. Read this document (`00_MASTER_DIRECTIVE/04_State_Continuity.md`) to re-establish operational bearings.
6. Read `01_PROJECT_NOTEBOOK/00_Project_Index.md` to check active projects and current milestones.
7. Consult `01_PROJECT_NOTEBOOK/Running_Log.md` for recent chronological history, inline tags, and decisions.
8. Inspect relevant repository files under `02_REPOSITORIES/` prior to performing work.
9. Never assume undocumented structure or unrecorded decisions.
10. Never alter or expand the architecture simply because an alternative appears advantageous.

---

## 6. Change Control Protocol
If an AI agent identifies an architectural defect, gap, or improvement:
1. **Identify:** Pinpoint the specific observed operational requirement or failure mode.
2. **Document:** Record the issue in `01_PROJECT_NOTEBOOK/Running_Log.md` using the appropriate inline tag (`[PROBLEM]`, `[OBSERVATION]`, or `[DISCOVERY]`).
3. **Propose:** Detail the proposed structural improvement without modifying existing files.
4. **Decide:** Await human review and formal authorization.
5. **Implement:** Only after explicit human authorization may governing architectural files be amended.
