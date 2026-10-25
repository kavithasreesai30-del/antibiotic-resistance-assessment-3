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

## Project Plan

The project was completed in stages to support a structured and responsible analysis of antibiotic resistance trends.

1. **Project setup:** Create the repository, organise the project folders, and document the project purpose and objectives.
2. **Data sourcing and inspection:** Obtain the public UKHSA dataset, review its structure and source documentation, and identify relevant variables.
3. **Data preparation:** Check data types, missing values, duplicate records and value ranges before analysis.
4. **Exploratory data analysis:** Calculate summary statistics and examine resistance percentages across antibiotic categories and over time.
5. **Visualisation and interpretation:** Create charts in Python and develop an interactive Tableau Public dashboard to communicate the findings.
6. **Ethical review:** Consider privacy, data governance, bias, limitations and the risk of misleading interpretations.
7. **Documentation and evaluation:** Record the methods, findings, limitations and lessons learned in the notebook and README, and review the dashboard for clarity and usability.

### Maintenance and Future Updates

If the project is extended, the dataset should be checked against the latest UKHSA publication before new data is incorporated. Any updates should be documented, the analysis and visualisations rerun, and the results reviewed for consistency and accuracy. Dashboard usability and accessibility should also be evaluated, with improvements made where appropriate.

## Data Management Throughout Collection, Processing, Analysis and Interpretation

**Data collection:** The dataset was obtained from the official UKHSA antimicrobial resistance dashboard. The source is acknowledged so that readers can locate the published data.

**Data inspection and preparation:** The dataset was loaded into Python and inspected for its structure, data types, missing values, duplicate records and plausible resistance percentage values. The analysis focused on the relevant national surveillance measures.

**Data analysis:** Descriptive statistics and visualisations were used to compare resistance percentages across antibiotic categories and examine patterns over time. The published figures were interpreted as three-month rolling measures rather than isolated monthly results.

**Data interpretation and communication:** Findings were presented through the Jupyter Notebook and Tableau Public dashboard. Labels, summaries and explanations were used to make the results understandable to technical and non-technical readers.

**Governance and responsible use:** The analysis uses aggregated national surveillance statistics, not identifiable patient records. The source and applicable reuse conditions should be acknowledged, and the results should not be used to make unsupported claims about individual patients, causes of resistance or clinical treatment decisions.

## Rationale for Research Methodology

A quantitative, descriptive approach was selected because the UKHSA dataset contains numerical resistance percentages recorded over time for different antibiotic categories.

Python was used to inspect and prepare the dataset, calculate summary statistics, explore patterns and create visualisations. Line charts helped examine changes over time, bar charts supported comparisons between antibiotics, and box plots and a heatmap provided additional views of the distribution and variation in the data.

Tableau Public was used to present the findings in an interactive dashboard, allowing readers to explore the results visually. Using both Python and Tableau supported analysis as well as communication of the findings.

This approach was suitable for identifying patterns and assessing the project hypotheses without making unsupported causal claims. The analysis is limited by the scope and quality of the published dataset, the use of three-month rolling figures and the fact that descriptive analysis alone cannot establish why resistance patterns occur.

## Mapping Business Requirements to Data Visualisations

The project uses a combination of Python visualisations and a Tableau Public dashboard to communicate antibiotic resistance patterns.

| Business requirement                          | Visualisation            | Purpose                                                                                         |
| --------------------------------------------- | ------------------------ | ----------------------------------------------------------------------------------------------- |
| Compare resistance across antibiotics         | Bar chart                | Compare average resistance percentages between the seven antibiotic categories.                 |
| Explore changes over time                     | Line chart               | Show how resistance percentages vary across the reporting period.                               |
| Examine the distribution of resistance values | Box plot                 | Show the spread and variation of resistance percentages for each antibiotic category.           |
| Compare patterns across antibiotics and time  | Heatmap                  | Provide an overview of resistance percentages across antibiotic categories and reporting dates. |
| Communicate findings interactively            | Tableau Public dashboard | Bring the visualisations together so readers can explore the results.                           |

Clear titles, labels and percentage formatting help readers interpret the charts. The findings are presented as descriptive surveillance patterns rather than explanations of causation or clinical recommendations.

## Analysis Techniques Used

### Data Analysis Methods

The project used the following techniques to explore the UKHSA antibiotic resistance dataset:


* **Data inspection and quality checks:** Reviewed the dataset structure, data types, missing values, duplicate records and resistance percentage ranges before analysis.
* **Descriptive statistics:** Calculated summary measures, including mean, minimum and maximum resistance percentages, to compare antibiotic categories.
* **Time-series analysis:** Examined monthly reporting patterns using line charts, taking account of the three-month rolling reporting period.
* **Comparative visualisation:** Used bar charts, box plots and a heatmap to compare resistance levels and distributions across antibiotic categories and reporting dates.
* **Hypothesis evaluation:** Used descriptive statistics and visual evidence to assess the three project hypotheses.

### Limitations and Alternative Approaches

Descriptive analysis is appropriate for identifying patterns in surveillance data, but it cannot establish the causes of antibiotic resistance or predict future outcomes. The dataset covers national aggregated statistics, so it does not show individual patient circumstances. Three-month rolling figures can also smooth short-term changes, and revisions to surveillance figures or changes in testing standards may affect comparisons over time.

More advanced statistical methods could be considered in future work if suitable data and assumptions were available. Any additional methods would need to be justified and their limitations explained.

### Use of Generative AI

Generative AI was used as a supporting tool during project development to help clarify concepts, organise documentation, troubleshoot coding issues and improve explanations. The dataset, analysis outputs and project findings were reviewed in the context of the actual work rather than accepted without checking.

AI-generated suggestions can be incomplete or inaccurate, so they require verification. AI was not treated as a source of surveillance evidence, and the project's conclusions are based on the dataset and the analysis performed.


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
