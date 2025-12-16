# Aviation Fleet Acquisition Risk Analysis

## Project Overview

This project provides a data-driven risk assessment for the acquisition of new aircraft for the company's Aviation Division. By analyzing historical accident data from the National Transportation Safety Board (NTSB), the project identifies aircraft models with the lowest fatality rates and provides concrete recommendations to minimize risk and optimize safety performance.

## Business Problem

The objective was to move beyond subjective purchasing decisions by creating a quantifiable metric for aircraft safety. The analysis informs the Head of the Aviation Division on which specific aircraft **models to prioritize for acquisition** and which **high-risk models to immediately exclude** from consideration.

## Methodology

### Data Source
* **Source:** NTSB Aviation Accident Data (Data is assumed to be sourced from the NTSB's publicly available database).
* **Time Frame:** All accidents and incidents recorded from **1990 to Present**.

### Key Steps
1.  **Data Cleaning & Imputation:** Handled missing injury counts by imputing with zero and filtered data for relevance (post-1990 events).
2.  **Feature Engineering:** Calculated the primary risk metric, **Fatality Rate** ($\frac{\text{Total Fatalities}}{\text{Total People Aboard}}$).
3.  **Statistical Filtering:** Limited the analysis to aircraft models with **at least 10 recorded accidents** to ensure statistical reliability, resulting in **971 qualified models**.
4.  **Risk Aggregation:** Aggregated safety metrics (Accident Count, Fatality Rate) by aircraft Make and Model.

## Key Findings & Safety Insight

The analysis produced two crucial risk lists: a "Buy List" and an "Avoid List."

### Insight: The Meaning of 0.0% Fatality Rate (Accidents $\ge$ 10)
The safest category of aircraft are those that meet this criterion. This is **not a contradiction** but a powerful measure of survivability.

* **Interpretation:** The aircraft was involved in at least 10 serious NTSB-reported failure events, yet **every single person involved survived**.
* **Conclusion:** These models demonstrate exceptional structural integrity and survivability features, proving they "fail safely" and should be prioritized.

### Primary Candidates (The Buy List)
These models, despite having a history of accidents (N $\ge$ 10), have a proven **0.00% Fatality Rate** (e.g., Swearingen SA-226T, Cessna 180H).

## Project Deliverables

1.  **Aviation_Risk_Analysis_Final.csv:** The final, cleaned, and aggregated dataset used for all recommendations and Tableau visualizations.
2.  **aviation_analysis.ipynb:** The complete Jupyter Notebook documenting all data cleaning, feature engineering, and analysis steps.
3.  **Aviation_Fleet_Risk_Assessment_Presentation.ppt:** The non-technical presentation for the Aviation Division Head.

## How to Replicate

1.  Clone this repository: `git clone [Your Repository URL]`
2.  Install required libraries (e.g., pandas, numpy, matplotlib, seaborn).
3.  Execute the cells in `aviation_analysis.ipynb` sequentially.
4.  Load the resulting `Aviation_Risk_Analysis_Final.csv` into Tableau to create the final dashboard.