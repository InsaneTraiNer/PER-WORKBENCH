# Evidence Repository — Claims & Grounded Data

## Purpose
The Evidence Repository functions as the structured claim layer of the PER Workbench. It contains granular, discrete factual claims, physical parameters, water quality data points, and historical system metrics extracted directly from authoritative sources in the Source Registry. This layer decouples raw evidence from downstream narrative drafting and engineering analysis.

---

## Claim Record Template

```markdown
### CLM-####
- **Claim:** [Exact, concise factual statement, metric, or physical parameter]
- **Source ID:** SRC-####
- **Source Location:** [Page number, section, table, or figure reference]
- **Date:** YYYY-MM-DD
- **Geographic Scope:** [Specific spatial boundary, pressure zone, wellfield, or district]
- **Supporting Evidence:** [Verbatim snippet, data excerpt, or figure details]
- **Contradictory Evidence:** [Any conflicting data from other sources, or "None identified"]
- **Confidence:** [HIGH | MEDIUM | LOW]
- **Review Status:** [UNVERIFIED | VERIFIED_BY_QA | HUMAN_VALIDATED]
- **Notes:** [Contextual notes, conversion factors, or dependencies]
```

---

## Registered Claims

### CLM-0001
- **Claim:** In calendar year 2020, Cal Water Visalia District's primary public water system (PWSID CA5410016, Visalia) served 45,325 active municipal connections and supplied 30,034 acre-feet of potable water.
- **Source ID:** SRC-0001
- **Source Location:** Chapter 2 ("Plan Preparation"), Page 18 (PDF Page 20), Table 2-1: "Public Water Systems (DWR Table 2-1)"
- **Date:** 2021-06-24 (Reporting CY 2020 data)
- **Geographic Scope:** Visalia Main Public Water System (CA5410016), City of Visalia service area
- **Supporting Evidence:** Table 2-1 entries: Public Water System Number = CA5410016; Public Water System Name = Visalia; Number of Municipal Connections 2020 = 45,325; Volume of Water Supplied 2020 = 30,034 AF.
- **Contradictory Evidence:** None identified in source. (Note: Satellite systems Tulco [CA5410041: 183 connections, 97 AF] and Mullen [CA5400935: 42 connections, 21 AF] are reported separately and aggregate to 45,550 connections and 30,152 AF total district-wide).
- **Confidence:** HIGH
- **Review Status:** UNVERIFIED (Extracted candidate claim; pending formal PE review)
- **Notes:** Baseline connection count and delivery metric for primary municipal service area. Downstream dependency: ANL-0001, project_profile.md, Section 2.2.

### CLM-0002
- **Claim:** In calendar year 2020, Cal Water Visalia District met 100% of its municipal water supply requirements through groundwater pumping (30,131 AF from the Kaweah Subbasin and 21 AF from the Tule Subbasin), without surface water impoundment or direct surface water deliveries.
- **Source ID:** SRC-0001
- **Source Location:** Chapter 6 ("Water Supply Characterization"), Page 60 (PDF Page 62), Table 6-1: "Groundwater Volume Pumped (DWR Table 6-1)" and Section "Surface Water"
- **Date:** 2021-06-24 (Reporting CY 2020 data)
- **Geographic Scope:** Visalia District service territory (Kaweah and Tule Subbasins, Tulare County, CA)
- **Supporting Evidence:** Table 6-1 entries for 2020: Kaweah Subbasin = 30,131 AF; Tule Subbasin = 21 AF; Total = 30,152 AF. Chapter 6 text affirms: "Cal Water does not impound or divert surface water as a means to meet demands in the Visalia District".
- **Contradictory Evidence:** None identified in source.
- **Confidence:** HIGH
- **Review Status:** UNVERIFIED (Extracted candidate claim; pending formal PE review)
- **Notes:** Confirms complete reliance on groundwater resources, predominantly (>99.9%) from the unadjudicated Kaweah Subbasin. Downstream dependency: project_profile.md, Section 2.2.
### CLM-0003
- **Claim:** The Cal Water Visalia District municipal drinking water system (PWSID CA5410016) supplies retail customers in Visalia and Goshen using groundwater produced from 58 active local production wells.
- **Source ID:** SRC-0002
- **Source Location:** Page 4, Section "YOUR WATER SYSTEM", Paragraph 1
- **Date:** 2025-06-01 (CY 2024 compliance status)
- **Geographic Scope:** Visalia and Goshen municipal service territory (PWSID CA5410016)
- **Supporting Evidence:** Verbatim excerpt: "Cal Water has provided high-quality water utility services in Visalia since 1926. We meet the needs of our valued customers in Visalia and Goshen with groundwater produced by 58 local wells."
- **Contradictory Evidence:** None noted in source. (Note: 2020 UWMP reported 60 active wells in 2020; reduction reflects two wells retired or taken offline prior to 2024).
- **Confidence:** [OBSERVED]
- **Review Status:** PROVISIONAL_INGESTION (Machine extracted; pending professional engineering verification)
- **Notes:** Establishes the physical baseline production asset count for evaluating wellhead treatment, replacement needs, and firm supply capacity. Downstream dependencies: project_profile.md, Section 2.2 / Section 3.

### CLM-0004
- **Claim:** In municipal groundwater monitoring across the Visalia system (testing period 2017–2024), Nitrate (as N) concentrations reached a maximum detected level of 7.3 ppm (mg/L), representing 73% of the California Primary Maximum Contaminant Level (MCL = 10 ppm), with a system-wide average concentration of 2.5 ppm.
- **Source ID:** SRC-0002
- **Source Location:** Page 13, Table "PRIMARY DRINKING WATER STANDARDS - Inorganic Chemicals", row "Nitrate as N", and Footnote 3
- **Date:** 2025-06-01 (Reporting data for 2017–2024)
- **Geographic Scope:** Visalia System (PWSID CA5410016) groundwater sources
- **Supporting Evidence:** Table reports Nitrate as N: Range = ND–7.3 ppm; Average = 2.5 ppm; MCL = 10 ppm; PHG = 10 ppm. Footnote 3 states: "The average Nitrate as N level was 2.5 ppm, with a maximum level of 7.3 ppm. We are closely monitoring the nitrate levels. Nitrate in drinking water at levels above 10 ppm is a health risk for infants of less than six months of age..."
- **Contradictory Evidence:** None noted; delivered water remained in compliance below the 10 ppm acute health threshold.
- **Confidence:** [OBSERVED]
- **Review Status:** PROVISIONAL_INGESTION (Machine extracted; pending professional engineering verification)
- **Notes:** Establishes an acute contaminant vulnerability driver; nitrate concentrations above 5 ppm (50% MCL) trigger heightened monitoring and potential future blending or ion-exchange treatment needs under DDW guidelines. Downstream dependencies: project_profile.md, Section 3.1.

### CLM-0005
- **Claim:** Municipal groundwater monitoring in the Visalia system (testing period 2019–2024) detected Perfluorooctanoic acid (PFOA) up to 7.4 ppt (exceeding the State Notification Level of 5.1 ppt and the 2024 EPA Primary MCL of 4.0 ppt) and Perfluorooctanesulfonic acid (PFOS) up to 10 ppt (exceeding the State Notification Level of 6.5 ppt and the 2024 EPA Primary MCL of 4.0 ppt), with Cal Water implementing operational offline protocols that take affected groundwater sources out of active service pending treatment installation.
- **Source ID:** SRC-0002
- **Source Location:** Page 10, Section "PFAS", and Page 15, Table "STATE-REGULATED CONTAMINANTS WITH NOTIFICATION LEVELS"
- **Date:** 2025-06-01 (Reporting data for 2019–2024)
- **Geographic Scope:** Visalia System (PWSID CA5410016) groundwater wells
- **Supporting Evidence:** Page 15 table reports PFOA: Range = ND–7.4 ppt (NL = 5.1 ppt; EPA MCL = 4 ppt); PFOS: Range = ND–10 ppt (NL = 6.5 ppt; EPA MCL = 4 ppt); PFHxS: Range = ND–3.5 ppt (NL = 3 ppt; EPA MCL = 10 ppt). Page 10 affirms: "In any cases across our service areas where detections were above the levels at which state public health experts have recommended water suppliers take action (the previous response level), we took the affected sources out of service until treatment was/could be installed."
- **Contradictory Evidence:** None noted; active distributed water met running annual average response levels.
- **Confidence:** [OBSERVED]
- **Review Status:** PROVISIONAL_INGESTION (Machine extracted; pending professional engineering verification)
- **Notes:** Represents a primary regulatory capital expenditure and engineering deficiency driver under the EPA National Primary Drinking Water Regulation (NPDWR), requiring treatment installation (GAC or ion exchange) or source replacement prior to the 2029 mandatory compliance deadline. Downstream dependencies: project_profile.md, Section 3.1 / Section 4.
