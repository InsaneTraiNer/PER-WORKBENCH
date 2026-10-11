# PER Workbench — Discovery and Ingestion Protocol

**Document ID:** MD-004  
**Status:** Authoritative / Operational Protocol  
**Scope:** Automated & Agentic Source Harvesting, Sequential ID Management, and Claim Extraction Governance

---

## 1. Purpose & Authority

This protocol establishes mandatory operating procedures for discovery models and agentic workflows when querying statutory public databases, cataloging primary evidence into the PER Workbench, and transforming raw records into atomic evidence claims.

All procedures herein enforce the foundational tenets of Master Directive `00_MASTER_DIRECTIVE/00_Master_Directive.md`:
1. Repositories own all persistent state.
2. Provenance is strictly preserved.
3. No machine extraction or inference may be represented as established fact without demonstrable source grounding.

---

## 2. Identifier Management

To prevent data collisions, race conditions, and dangling dependencies across multi-model sessions, identifiers must adhere to strict sequential generation rules:

### 2.1 Source Identifiers (`SRC-####`)
- **Format:** `SRC-` followed by exactly four digits, zero-padded (e.g., `SRC-0001`, `SRC-0002`, `SRC-0003`).
- **Sequence:** Strictly ascending numeric order based on formal ingestion into `02_REPOSITORIES/01_SOURCE/source_registry.md`.
- **No Collision:** No two documents, even different editions or appendices of the same master plan, may share an identical `SRC-####` identifier.
- **No Omission / Gap:** Identifiers must increment sequentially ($N+1$). If an entry is retired or replaced, it must be marked `[SUPERSEDED]` or `[ARCHIVED]` rather than deleted or reallocated.

### 2.2 Claim Identifiers (`CLM-####`)
- **Format:** `CLM-` followed by exactly four digits, zero-padded (e.g., `CLM-0001`, `CLM-0002`).
- **Scope:** Claims represent discrete, atomic propositions extracted from a specific `SRC-####` entry.
- **Sequence:** Incrementing sequentially within `02_REPOSITORIES/02_EVIDENCE/claims.md`.

---

## 3. Source Evaluation & Attribution Governance

Every candidate document must undergo structured evaluation prior to registration. An entry in `02_REPOSITORIES/01_SOURCE/source_registry.md` is mandatory and must include:
- **Title:** Complete official document title, including version, amendment, or proceeding docket number.
- **Source Type:** Classification (e.g., Statutory Compliance Filing, Regulatory Monitoring Report, Engineering Master Plan, General Rate Case Exhibit, State Spatial Dataset).
- **Origin:** Publishing agency, lead authoring firm, licensed professional engineer of record, or issuing department.
- **URL / Location:** Permanent canonical web URL, digital object identifier (DOI), or stable archive path.
- **Publication Date:** Date of formal adoption, stamping, or public release.
- **Access Date:** Exact date retrieved by the discovery model.
- **Geographic Scope:** Specific municipal boundary, pressure zone, water district boundary, or groundwater subbasin.
- **Authoritativeness Tier:** Explicit assignment according to the following hierarchy:
  1. *Tier 1 (Statutory / Regulatory Records):* Adopted UWMPs, SWRCB compliance orders, Division of Drinking Water annual compliance letters, certified CEQA filings, SGMA annual reports.
  2. *Tier 2 (Engineering & Infrastructure Studies):* Signed Preliminary Engineering Reports, Master Water Plans, rate case capital expenditure testimonies, facility condition assessments.
  3. *Tier 3 (Operational & Informational Records):* Consumer Confidence Reports (CCRs), public outreach presentations, press releases, meeting minutes.

---

## 4. Claim Extraction Rules

When evidence is parsed from registered sources into `02_REPOSITORIES/02_EVIDENCE/claims.md`, the extraction model must follow these four core standards:

1. **Exact Pinpoint Locator:** Every claim must identify the precise physical location within the source document:
   - Page number (both document page number and PDF page number).
   - Table identifier, figure title, or section number.
   - For GIS datasets: layer name, attribute field, and feature ID.
2. **Verbatim Grounding:** Claims must quote the specific quantitative figure or excerpt the exact sentence establishing the proposition. No paraphrasing that alters engineering precision.
3. **Temporal Validity:** Must specify the operational or measurement timeframe represented by the data (e.g., "Calendar Year 2020", "April 2023 static water level", "10-year rolling average 2010–2020"), separate from the document publication date.
4. **Epistemic Classification Tagging:** Every claim must be tagged with its epistemic category:
   - `[OBSERVED]`: Direct empirical measurement, meter reading, laboratory chemical analysis, or field survey.
   - `[CALCULATED]`: Figure derived from a mathematical operation applied to primary data (must document inputs and arithmetic formula).
   - `[INFERRED]`: Projection, modeling output, demand forecast, or interpolative estimate.
   - `[UNCERTAIN]`: Statement with explicit caveats, disputed measurements, confidence intervals, or known instrumentation limitations.

---

## 5. Standardized Public Query Templates

Discovery models (e.g., Perplexity or automated web harvesters) must use the following standardized query syntaxes when searching statutory portals based on the intake parameters:

### 5.1 CA DWR Urban Water Management Plan (UWMP) Portal
- **Target Endpoint:** DWR WUEdata Portal (`wuedata.water.ca.gov`)
- **Query Template:**  
  `"{System Name}" "{PWSID}" "Urban Water Management Plan" OR "UWMP" site:water.ca.gov OR site:calwater.com filetype:pdf`
- **Objective:** Extract baseline population, active connection counts by sector, five-year historical production, and SB X7-7 water conservation compliance.

### 5.2 SWRCB Division of Drinking Water (DDW) / SDWIS
- **Target Endpoint:** State Water Resources Control Board Drinking Water Watch (`sdwis.waterboards.ca.gov`)
- **Query Template:**  
  `"{PWSID}" "Water Quality" OR "Consumer Confidence Report" OR "MCL Exceedance" site:waterboards.ca.gov OR site:epa.gov`
- **Objective:** Extract chemical analytical records, compliance violations, Maximum Contaminant Level (MCL) exceedances, and public health notifications.

### 5.3 DWR SGMA Portal / Groundwater Sustainability Agency (GSA)
- **Target Endpoint:** DWR SGMA Portal (`sgma.water.ca.gov/portal`)
- **Query Template:**  
  `"{Region / DWR Subbasin ID}" OR "{GSA Name}" "Groundwater Sustainability Plan" OR "Annual Report" "groundwater elevation" site:ca.gov filetype:pdf`
- **Objective:** Extract subbasin overdraft metrics, hydrographs, groundwater sustainability indicators, and monitoring network data.

---

## 6. Gating Check (The Ingestion Air-Lock)

**Strict Prohibition:**  
No agentic, drafting, or analytical tool may generate content in subordinate repositories (`02_REPOSITORIES/03_REQUIREMENTS/`, `02_REPOSITORIES/04_ANALYSIS/`, `02_REPOSITORIES/05_PROJECT/`, or `02_REPOSITORIES/06_PER/`) using data from a source that has not been formally cataloged in `02_REPOSITORIES/01_SOURCE/source_registry.md`.

- Any draft claim lacking a verified `Source ID: SRC-####` is considered an invalid hallucination candidate and must be rejected immediately during QA review (`02_REPOSITORIES/07_QA/qa_log.md`).
- Analysis records (`ANL-####`) must reference verified Claim IDs (`CLM-####`) rather than citing raw external web links directly.
