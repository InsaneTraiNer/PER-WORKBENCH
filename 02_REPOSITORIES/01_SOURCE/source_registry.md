# Source Repository — Source Registry

## Purpose
The Source Registry is the authoritative catalog of all primary documents, technical reports, regulatory statutes, geospatial datasets, utility billing statements, and reference materials ingested into the PER Workbench. No claim or analysis may enter the Workbench without traceable attribution to an indexed entry in this registry.

---

## Source Record Template

```markdown
### SRC-####
- **Title:** [Document or Dataset Title]
- **Source Type:** [e.g., Regulatory Statute | Master Plan | Engineering Study | Water Quality Report | Billing Record | GIS Dataset | Interview]
- **Origin:** [Issuing Agency, Author, Municipal Department, or Publisher]
- **URL / Location:** [Direct URL, DOI, or local filesystem path]
- **Publication Date:** YYYY-MM-DD
- **Access Date:** YYYY-MM-DD
- **Geographic Scope:** [e.g., Visalia, Tulare County, Central Valley, Regional]
- **Relevant Project:** [e.g., Visalia City Water PER Slice]
- **Description:** [Brief summary of the document contents, scope, and key topics]
- **Reliability / Authority:** [Assessment of authoritativeness, peer review status, or legal standing]
- **Notes:** [Relevant restrictions, versioning details, or caveats]
```

---

## Registered Sources

### SRC-0001
- **Title:** 2020 Urban Water Management Plan: Visalia District
- **Source Type:** Statutory Urban Water Management Plan (pursuant to California Water Code § 10610–10657)
- **Origin:** California Water Service Company (Prepared by EKI Environment & Water, Inc., M.Cubed, and Gary Fiske and Associates; submitted to California Department of Water Resources)
- **URL / Location:** https://www.calwater.com/docs/uwmp2020/VIS_2020_UWMP_FINAL.pdf
- **Publication Date:** 2021-06-24
- **Access Date:** 2026-09-17
- **Geographic Scope:** Visalia District (City of Visalia, Goshen, and unincorporated contiguous areas, Tulare County, CA)
- **Relevant Project:** Visalia City Water PER Slice
- **Description:** Comprehensive five-year urban water management plan containing official regulatory determinations, public water system inventory (PWSID CA5410016), active service connections, historical supply and pumping volumes, groundwater basin characteristics, and water shortage contingency planning.
- **Reliability / Authority:** High. Authoritative compliance filing adopted by utility board of directors, prepared by licensed professional engineers/economic consultants, and filed with state regulatory oversight bodies (DWR and CPUC).
- **Notes:** Primary test input for the initial vertical slice demonstration. Selected to establish verifiable 2020 baseline public water system connections and production volume.
### SRC-0002
- **Title:** 2024 Water Quality Report: Visalia District (Visalia System)
- **Source Type:** Statutory Consumer Confidence Report (pursuant to federal Safe Drinking Water Act and California Health & Safety Code § 116470)
- **Origin:** California Water Service Company (Visalia District, PWSID CA5410016)
- **URL / Location:** https://www.calwater.com/docs/ccr/2024/vis-vis-2024.pdf
- **Publication Date:** 2025-06-01 (reporting CY 2024 compliance monitoring data)
- **Access Date:** 2026-09-18
- **Geographic Scope:** Visalia and Goshen municipal service areas, Tulare County, CA
- **Relevant Project:** Visalia City Water PER Slice
- **Description:** Official annual drinking water quality compliance report for PWSID CA5410016 documenting testing results across 58 active groundwater wells for 196 constituents. Details Primary Drinking Water Standards (including Nitrate as N levels up to 7.3 ppm), Secondary Drinking Water Standards (aluminum and iron detections), and State/Federal monitoring for emerging Per- and Polyfluoroalkyl Substances (PFAS) under California notification levels and EPA National Primary Drinking Water Regulations. Confirms well offline protocols for sources exceeding health advisory levels.
- **Reliability / Authority:** Tier 1 (Statutory Compliance Filing). Certified laboratory analytical data reported under state and federal regulatory oversight (SWRCB Division of Drinking Water and U.S. EPA).
- **Notes:** Selected autonomously as SRC-0002 based on primary health standard deficiency priority, active well counts (58 wells), and recent compliance cycle data (2024). Downstream dependencies: CLM-0003, CLM-0004, CLM-0005, project_profile.md, Section 3 need formulation.
