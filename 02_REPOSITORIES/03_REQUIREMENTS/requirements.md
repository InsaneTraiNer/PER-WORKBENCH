# Requirements Repository — Requirements

## Purpose
The Requirements Repository stores all project constraints, design criteria, statutory regulations, environmental mandates, and funding program prerequisites governing the Preliminary Engineering Report. All requirements are maintained in a flat structure across standardized categories.

---

## Requirement Record Template

```markdown
### REQ-####
- **Requirement:** [Concise statement of the mandatory condition or design criterion]
- **Category:** [Project | Regulatory | Engineering | Funding | Unresolved]
- **Source:** [Statutory code, agency rule, grant guide, client directive, or SRC-####]
- **Applicability:** [Subsystem, geographic boundary, or phase to which this requirement applies]
- **Status:** [PROPOSED | MANDATORY | WAIVED | UNRESOLVED]
- **Evidence:** [Citation, code reference, or supporting claim ID (CLM-####)]
- **Notes:** [Compliance benchmarks, evaluation criteria, or open questions]
```

---

## Registered Requirements

### REQ-0001
- **Requirement:** Urban retail water suppliers providing water for municipal purposes to 3,000 or more customers or supplying more than 3,000 acre-feet annually must prepare, adopt, and submit an Urban Water Management Plan every five years to the California Department of Water Resources, and maintain demonstrated compliance with statutory water conservation targets (SB X7-7 per CWC § 10608 et seq.) as a prerequisite for state water grant or loan funding eligibility.
- **Category:** Regulatory / Funding
- **Source:** California Water Code § 10617, § 10608.56, and § 10621, as cited and applied in SRC-0001 (Chapter 1, pp. 11-12)
- **Applicability:** Cal Water Visalia District (PWSID CA5410016)
- **Status:** MANDATORY
- **Evidence:** CLM-0001 confirms system scale (45,325 connections, 30,034 AFY), substantially exceeding the statutory threshold of 3,000 connections / 3,000 AFY.
- **Notes:** Governs eligibility for California State Revolving Fund (SRF) and DWR infrastructure grant disbursements. Downstream dependency: ANL-0001, project_profile.md, Section 1.1 / 2.3.
