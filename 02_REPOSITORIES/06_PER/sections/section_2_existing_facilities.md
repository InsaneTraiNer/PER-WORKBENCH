# Preliminary Engineering Report (PER) — Draft Section

**Document Module:** PER Section 2.2 — Existing Facilities and System Baseline Demand  
**Target Project:** Visalia City Water PER Slice  
**Working Status:** DRAFT — FOR TESTING AND AUDIT ONLY  
**Professional Disclaimer:** This document is an intermediate machine-generated analytical draft produced by the PER Workbench V1 demonstration pipeline. It does not constitute a completed engineering report, official public works finding, or certified engineering judgment, and has not been approved or sealed by a licensed Professional Engineer.

---

## 2.2 Baseline Planning Area and Water Production Summary (Visalia Main System)

### 2.2.1 System Population and Service Connections
The primary municipal water distribution network serving the City of Visalia is operated by California Water Service Company (Cal Water) under California Public Water System identification number **CA5410016** (`CLM-0001`). In calendar year 2020, this primary system provided retail water service through **45,325 active municipal connections** (`CLM-0001`, `SRC-0001` [Table 2-1]). Because the system exceeds 3,000 active service connections and delivers greater than 3,000 acre-feet per year, it is subject to mandatory five-year Urban Water Management Plan filings and conservation targets under the California Water Code (`REQ-0001`).

### 2.2.2 Source Supply and Groundwater Reliance
The Visalia District relies entirely on local groundwater resources to satisfy potable municipal water requirements (`CLM-0002`). Cal Water neither impounds nor directly diverts surface water to supply the Visalia distribution network (`CLM-0002`, `SRC-0001` [Section 6.3]). 

During calendar year 2020, total groundwater production for the Visalia District reached **30,152 acre-feet (AF)**, of which **30,131 AF (99.93%)** was extracted from the alluvial aquifer of the Kaweah Subbasin, with the remaining **21 AF (0.07%)** drawn from the Tule Subbasin (`CLM-0002`, `SRC-0001` [Table 6-1]).

### 2.2.3 Baseline Volumetric Demand and Delivery Rates
For the primary Visalia municipal system (CA5410016), total water supplied to the distribution network in 2020 totaled **30,034 AF** (`CLM-0001`, `SRC-0001` [Table 2-1]). Engineering synthesis of these primary production records indicates the following baseline operational demand characteristics (`ANL-0001`):

| Metric | Measured / Calculated Value | Units | Provenance / Backward Reference |
| :--- | :--- | :--- | :--- |
| **Public Water System ID** | `CA5410016` | — | `SRC-0001` Table 2-1, `CLM-0001` |
| **Active Service Connections** | `45,325` | Connections | `SRC-0001` Table 2-1, `CLM-0001` |
| **Total Annual Volume Supplied** | `30,034` | Acre-Feet (AF) | `SRC-0001` Table 2-1, `CLM-0001` |
| **Total Annual Volume (Gallons)** | `9,786,608,934` | Gallons | `ANL-0001` (Calculated at 325,851 gal/AF) |
| **Average Daily Demand (ADD)** | `26.74` | Million Gallons/Day (MGD) | `ANL-0001` (366 days in CY 2020) |
| **Average Annual Delivery / Conn.** | `0.663` | AF/Connection/Year | `ANL-0001` (30,034 AF / 45,325 conn) |
| **Average Daily Delivery / Conn.** | `590` | Gallons/Connection/Day | `ANL-0001` (26.74 MGD / 45,325 conn) |
| **Groundwater Supply Proportion** | `100.0%` | Percent | `SRC-0001` Table 6-1, `CLM-0002` |

---

## Traceability and Backward Attribution Matrix

| Draft Element / Sentence | Supporting Evidence ID | Primary Source & Locator | Analytical Step |
| :--- | :--- | :--- | :--- |
| Visalia Main System PWSID CA5410016 | `CLM-0001` | `SRC-0001` p. 18, Table 2-1 | Extraction |
| 45,325 Active Municipal Connections (2020) | `CLM-0001` | `SRC-0001` p. 18, Table 2-1 | Extraction |
| 30,034 AF Total Water Supplied (2020) | `CLM-0001` | `SRC-0001` p. 18, Table 2-1 | Extraction |
| Mandatory CWC Planning Threshold (>3,000 conn) | `REQ-0001` | `SRC-0001` p. 11 (CWC § 10617) | Requirement formulation |
| 100% Groundwater extraction / Zero surface water | `CLM-0002` | `SRC-0001` p. 60, Table 6-1 & Sec 6.3 | Extraction |
| 30,131 AF pumped from Kaweah Subbasin | `CLM-0002` | `SRC-0001` p. 60, Table 6-1 | Extraction |
| Average Daily Demand = 26.74 MGD | `ANL-0001` | Computed from `CLM-0001` inputs | `ANL-0001` Step 2 |
| Unit Consumption = 0.663 AF/conn/yr (590 gpd) | `ANL-0001` | Computed from `CLM-0001` inputs | `ANL-0001` Steps 3 & 4 |
