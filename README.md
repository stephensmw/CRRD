# ASAL Resilience Monitor: A Data-Driven Early Warning System
This project creates a **Crisis Resilience and Response Dashboard** (CRRD) that can be modified and used for the specific region and criteria needed. For this project, it has been created to monitor conditions in the northern counties of Kenya. More detailed information about the project can be found on the project wiki: [[https://github.com/stephensmw/CRRD/wiki/]]. 

## Objective
Using "live" data, create a dashboard that displays data aggregation, analytical frameworks, and data visualization. For this specific exercise, I am using publicly available and open source data sources to analyze and visualize a dashboard displaying climate-induced resource conflicts in the Arid and Semi-Arid Lands (ASALS) of Northern Kenya. 

## Methodology
### Data Acquisition 
This project used a multi-source data integration approach to model environmental and human security risks in Kenya's ASALs.
* Environmental indicators: Data regarding draught cycles and vegetation health were sourced from the National Drought Management Authority (NDMA) [https://ndma.go.ke/drought-information/]. These monthly bulletins provide standardized drought phase classifications.
* Conflict Indicators: Conflict event data were sourced from the Armed Conflict Location & Event Data Project (ACLED) [https://acleddata.com/conflict-data/download-data-files/], specifically filtered for Northern Kenya to capture the frequency and intensity of security incidents.

### Data Processing and Feature Engineering
To create the "Stability and Resource Allocation Index," raw data underwent a three-step transformation:
1. Normalization: Since drought data (categorical/ordinal, e.g., "Alarm") and conflict data (integer/frequency, e.g., "Number of events") exist on different scales, both were normalized to a common 0–1 risk scale.
2. Index Calculation: A weighted algorithm calculates the "Stability Index" for each target region. A higher index value reflects higher resource pressure (high drought + high conflict).
Formula:
3. Temporal Aggregation: Data was aggregated into monthly time-series buckets to allow for correlation analysis between climatic shocks and security volatility.

### Visualization & Simulation Design
The dashboard serves as a decision-support tool, employing the following visualization principles:
* Geospatial Mapping: A choropleth map visualizes regional "hotspots" where the index exceeds pre-defined thresholds.
* Time-Series Analysis: Dual-axis charts allow stakeholders to compare the lagged effect of drought onset against conflict escalation.
* Scenario Simulation: The interactive component allows users to adjust weightings to simulate how different organizational priorities (e.g., prioritizing food security vs. prioritizing physical safety) shift the allocation of resources.

### Quality Assurance & Limitations
Data Validation: Cross-referencing against periodic reports from agencies like FEWS NET ensures the simulated trends align with historical ground truths.

Methodological Constraints: As this is a simulation tool, it does not account for all socioeconomic variables; the index serves as a proxy for risk rather than an exhaustive predictive model.



