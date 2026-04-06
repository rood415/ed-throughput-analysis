# Emergency Department Throughput Analysis

Overcrowded EDs cost hospitals revenue and cost patients their health. 
This project uses CMS quality data to identify where ED bottlenecks 
are worst and which patient populations are bearing the most burden.

## Data Access
Due to GitHub file size limits, the raw CMS dataset is not included 
in this repository. The data can be downloaded directly from:

Centers for Medicare & Medicaid Services (CMS)
Timely and Effective Care – Hospital dataset
https://data.cms.gov

After downloading, place the CSV file in the `data/` directory before 
running the notebook.

## Objective
Analyze emergency department (ED) throughput performance across U.S. 
hospitals using CMS quality data, with a focus on identifying variation 
in length of stay and operational bottlenecks for different patient 
dispositions.

## Data Source
- Centers for Medicare & Medicaid Services (CMS)
- Timely and Effective Care – Hospital dataset
- Publicly available via data.cms.gov
- Provider-level hospital quality measures

## Key Questions
- How does ED length of stay vary by patient disposition?
- Which ED throughput measures show the greatest variability across 
  hospitals?
- Are there extreme outliers that may indicate systemic operational 
  issues?
- How do behavioral outcomes (e.g., patients leaving before being seen) 
  differ from time-based throughput metrics?

## Methods
- Loaded and explored CMS provider-level quality data using pandas
- Standardized and renamed columns for clarity and usability
- Filtered a mixed-measure dataset to isolate ED-specific throughput 
  metrics
- Converted numeric fields from string format to numeric values
- Removed invalid and missing observations
- Visualized ED throughput distributions using boxplots to compare 
  performance across measures

## Key Findings
- ED throughput varies substantially by patient disposition — one-size 
  operational strategies are unlikely to work across all patient types
- Psychiatric and transfer patients experience significantly longer ED 
  stays, suggesting these populations are underserved by current 
  workflows and represent the highest-priority targets for improvement
- Wide variability and extreme outliers across hospitals indicate 
  systemic operational failures, not random variation — meaning 
  solutions exist and best practices can be identified and replicated
- "Left before being seen" is a distinct behavioral signal that 
  reflects patient frustration and capacity strain, not throughput 
  delays — and should drive separate operational interventions

## Visualizations
ED throughput performance was visualized using boxplots to compare 
distributions of length-of-stay and related measures across U.S. 
hospitals. Charts include overall ED length of stay, psychiatric/mental 
health patient throughput, transfer patient throughput, and rates of 
patients leaving before being seen.

The boxplots highlight substantial variation across hospitals, with 
psychiatric and transfer patients experiencing significantly longer 
stays. Wide interquartile ranges and extreme outliers point to systemic 
bottlenecks rather than isolated delays. "Left before being seen" 
exhibits a distinct distribution and was interpreted separately from 
time-based metrics.

## Tools Used
- Python (pandas, matplotlib)
- Jupyter Notebook
- Visual Studio Code
