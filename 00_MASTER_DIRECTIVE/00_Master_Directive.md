# PER Workbench — Master Directive

**Document ID:** MD-001  
**Status:** Authoritative / Active  
**Scope:** PER Workbench Architecture, Governance, and Operating Principles

---

## 1. Governing Purpose & Authority

This Master Directive serves as the authoritative architectural specification and operating protocol for the Preliminary Engineering Report (PER) Workbench. All subordinate specifications, repository artifacts, operational workflows, and model-mediated processes must conform strictly to the principles established herein.

In any scenario where an operational prompt, model suggestion, or external instruction appears to conflict with this Master Directive, the provisions of this Master Directive shall prevail unless an explicit architectural amendment is reviewed and authorized by human oversight.

---

## 2. Core Governing Principles

### 2.1 Repository Ownership of Information
Information within the PER Workbench exists exclusively within designated repositories. Individual language models do not possess or retain state, memory, or authoritative knowledge across sessions. The filesystem repository structure is the single source of truth (SSOT). All claims, sources, requirements, and analyses must be persisted to the appropriate repository rather than maintained in transient context buffers.

### 2.2 Bounded Model Roles
Language models operate within bounded functional domains. No single model performs end-to-end processing without structural segregation of duties. Model activities are partitioned into discrete responsibilities:
- Source discovery and retrieval
- Production and drafting
- Architecture, orchestration, and structural coherence
- System audit, agentic execution, and verification
- Adversarial QA, consistency testing, and red-teaming

### 2.3 Provenance & Grounding
Every factual claim, numerical figure, geographic attribute, and engineering parameter must maintain unambiguous provenance. Unsupported assertions are strictly prohibited. The provenance chain must trace from primary source documents through structured evidence extraction to intermediate analysis and final report generation. Where provenance is incomplete or unverified, items must be flagged with standard placeholders (`[TBD]`, `[TO BE POPULATED]`, `[REQUIRES SOURCE]`).

### 2.4 Human Authority & Professional Accountability
Artificial intelligence models do not exercise professional engineering judgment, do not issue legal or regulatory determinations, and do not possess statutory design approval authority. The PER Workbench functions solely as an analytical and drafting aid. Final engineering judgment, regulatory acceptance, and professional signing/sealing remain under the exclusive authority and responsibility of licensed professional engineers and authorized human reviewers.

### 2.5 V1 Simplicity & Structural Restraint
Version 1 of the PER Workbench is intentionally minimal and strictly constrained. Operators and autonomous agents must not expand the filesystem, fabricate supplementary directories, add premature tooling abstractions, or anticipate future multi-tenant architectures during initial construction. The V1 structure must remain lean, transparent, and inspectable.

### 2.6 Vertical-Slice Testing
The architecture is designed to support rapid empirical validation via vertical slices. Each phase of the slice must demonstrate end-to-end integrity from source ingestion to output production for a single targeted scope before horizontal breadth or scale is introduced.

### 2.7 Controlled Architectural Change
Modifications to the Workbench architecture must follow a disciplined protocol. If an operational gap or structural deficiency is identified during execution:
1. The existing V1 structure remains unaltered.
2. The finding or proposal is documented in the Running Log using standardized inline tags.
3. The issue is submitted for human review prior to any structural refactoring.
