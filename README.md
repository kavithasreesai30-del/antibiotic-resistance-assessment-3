# Exploring Antibiotic Resistance Trends in *E. coli* Bloodstream Infections in England

## Project Overview

This project explores publicly available surveillance data relating to antibiotic resistance in *Escherichia coli* (*E. coli*) bloodstream infections in England.

The analysis aims to investigate patterns and trends in the selected dataset using data analysis and visualisation. The findings will be communicated through appropriate visualisations and a dashboard.

## Project Objectives

* Explore the selected antibiotic resistance surveillance dataset.
* Investigate resistance patterns across the antibiotic groups represented in the data.
* Examine changes over time, where supported by the available data.
* Communicate findings through clear visualisations and a dashboard.
* Consider data quality, privacy, potential bias, and ethical responsibilities.

## Project Structure

```text
antibiotic-resistance-assessment-3/
├── data/
│   └── ukhsa-chart-download.csv
├── notebooks/
│   └── ethical_practice_data_analysis.ipynb
├── outputs/
├── reports/
├── .gitignore
├── README.md
└── requirements.txt
```

## Data Source

The project uses publicly available surveillance data from the UK Health Security Agency (UKHSA), accessed through its official data dashboard.

* **Dataset:** [Antimicrobial resistance in *E. coli* bacteraemia — UKHSA](https://ukhsa-dashboard.data.gov.uk/antimicrobial-resistance/antimicrobial-resistance-in-ecoli-bacteraemia)
* **Local dataset file:** `data/ukhsa-chart-download.csv`

The downloaded dataset is stored locally in the `data/` directory. The original source is acknowledged to support transparency and reproducibility. The dataset will be used in accordance with the applicable licence and conditions of use.

## Dataset Content

The project uses publicly available surveillance data from the UK Health Security Agency (UKHSA) to explore antibiotic resistance in *E. coli* bloodstream infections in England.

The dataset contains monthly resistance percentages for seven antibiotic categories, covering July 2021 to July 2026. It includes information such as the reporting date, antibiotic category, geographical area, demographic group, and resistance percentage.

The main measure analysed is the percentage of tested *E. coli* bloodstream infection samples reported as resistant to each antibiotic. The published monthly figures use a three-month rolling period, so they should not be interpreted as measurements for a single month alone.

The dataset supports comparisons between antibiotics and exploration of changes in resistance percentages over time. It contains aggregated national surveillance statistics rather than identifiable patient records.

## Business Requirements

The project aims to turn publicly available UKHSA antibiotic resistance surveillance data into clear, understandable insights that can support awareness and further investigation of antibiotic resistance trends in England.

The project requirements are to:

* **Identify resistance patterns:** Compare reported resistance percentages across seven antibiotic categories.
* **Explore changes over time:** Examine monthly resistance trends from July 2021 to July 2026, taking account of the three-month rolling reporting period.
* **Communicate findings clearly:** Use appropriate charts and an interactive Tableau Public dashboard to present the results to both technical and non-technical audiences.
* **Support responsible interpretation:** Explain the dataset’s limitations and avoid unsupported causal claims or individualised clinical advice.
* **Follow ethical data practices:** Acknowledge the UKHSA source, respect applicable reuse conditions, and communicate the findings accurately and transparently.

## Hypothesis and How to Validate Them

The project investigates three hypotheses using the UKHSA antibiotic resistance dataset.

**Hypothesis 1: Co-amoxiclav has a higher resistance percentage than the other antibiotic categories.**

* **Validation:** Compare the mean resistance percentages for all seven antibiotic categories using summary statistics and a bar chart.

**Hypothesis 2: Resistance percentages have increased over the study period for at least some antibiotic categories.**

* **Validation:** Examine the time-series line chart to identify changes and patterns over time. Interpret these patterns cautiously because the published figures use a three-month rolling period.

**Hypothesis 3: Carbapenems and Amikacin have lower resistance percentages than the other antibiotic categories.**

* **Validation:** Compare their mean resistance percentages with those of the other antibiotics using summary statistics and visualisations.

These hypotheses are assessed using descriptive analysis. The results can indicate patterns in the available data but cannot establish the causes of resistance or predict future outcomes.


## Tools and Technologies

* **Python** – Data inspection, cleaning, exploratory data analysis and statistical analysis.
* **Jupyter Notebook** – Documentation and execution of the analysis.
* **Tableau Public** – Data visualisation and interactive dashboard development.
* **Visual Studio Code** – Project development and file management.
* **Git and GitHub** – Version control, project documentation and code hosting.


## Project Status

The project has progressed from initial setup to data analysis, visualisation and dashboard publication.

* **Project setup:** Completed.
* **Dataset inspection and preparation:** Completed.
* **Exploratory data analysis and visualisation:** Completed.
* **Statistical analysis and hypothesis evaluation:** Completed.
* **Ethical considerations and limitations:** Documented.
* **Tableau Public dashboard:** Completed and published.
* **README and final documentation:** In progress.
