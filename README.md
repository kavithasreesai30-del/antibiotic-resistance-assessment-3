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

## Business Requirements

The project aims to turn publicly available UKHSA antibiotic resistance surveillance data into clear, understandable insights that can support awareness and further investigation of antibiotic resistance trends in England.

The project requirements are to:

* **Identify resistance patterns:** Compare reported resistance percentages across seven antibiotic categories.
* **Explore changes over time:** Examine monthly resistance trends from July 2021 to July 2026, taking account of the three-month rolling reporting period.
* **Communicate findings clearly:** Use appropriate charts and an interactive Tableau Public dashboard to present the results to both technical and non-technical audiences.
* **Support responsible interpretation:** Explain the dataset’s limitations and avoid unsupported causal claims or individualised clinical advice.
* **Follow ethical data practices:** Acknowledge the UKHSA source, respect applicable reuse conditions, and communicate the findings accurately and transparently.



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

## Project Structure

```text
antibiotic-resistance-assessment-3/
├── data/
│   └── ukhsa-chart-download.csv
├── notebooks/
│   └── ethical_practice_data_analysis.ipynb
├── outputs/
│   └── resistance_summary.csv
├── reports/
│   └── project_summary.md
├── .gitignore
├── README.md
└── requirements.txt
```

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

## Hypothesis and How to Validate Them

The project investigates three hypotheses using the UKHSA antibiotic resistance dataset.

**Hypothesis 1: Co-amoxiclav has a higher resistance percentage than the other antibiotic categories.**

* **Validation:** Compare the mean resistance percentages for all seven antibiotic categories using summary statistics and a bar chart.

**Hypothesis 2: Resistance percentages have increased over the study period for at least some antibiotic categories.**

* **Validation:** Examine the time-series line chart to identify changes and patterns over time. Interpret these patterns cautiously because the published figures use a three-month rolling period.

**Hypothesis 3: Carbapenems and Amikacin have lower resistance percentages than the other antibiotic categories.**

* **Validation:** Compare their mean resistance percentages with those of the other antibiotics using summary statistics and visualisations.

These hypotheses are assessed using descriptive analysis. The results can indicate patterns in the available data but cannot establish the causes of resistance or predict future outcomes.

## Results and Conclusions

The descriptive analysis identified differences in resistance percentages across the seven antibiotic categories.

* **Hypothesis 1 was supported:** Co-amoxiclav had the highest mean resistance percentage at 42.69%.
* **Hypothesis 2 received preliminary support:** Comparing July 2021 with July 2026, six of the seven antibiotic categories showed higher resistance percentages. Increases ranged from 0.70 percentage points for Amikacin to 4.77 percentage points for third-generation cephalosporins. Carbapenems decreased by 0.03 percentage points. This endpoint comparison does not mean resistance increased continuously throughout the study period.
* **Hypothesis 3 was supported:** Carbapenems had the lowest mean resistance percentage at 0.21%, while Amikacin had a mean of 2.76%.

These findings describe the available national surveillance data. They do not establish the causes of antibiotic resistance or predict future trends. The reported monthly values represent three-month rolling measures, and results may be affected by data revisions or changes in testing standards.


## Rationale for Research Methodology

A quantitative, descriptive approach was selected because the UKHSA dataset contains numerical resistance percentages recorded over time for different antibiotic categories.

Python was used to inspect and prepare the dataset, calculate summary statistics, explore patterns and create visualisations. Line charts helped examine changes over time, bar charts supported comparisons between antibiotics, and box plots and a heatmap provided additional views of the distribution and variation in the data.

Tableau Public was used to present the findings in an interactive dashboard, allowing readers to explore the results visually. Using both Python and Tableau supported analysis as well as communication of the findings.

This approach was suitable for identifying patterns and assessing the project hypotheses without making unsupported causal claims. The analysis is limited by the scope and quality of the published dataset, the use of three-month rolling figures and the fact that descriptive analysis alone cannot establish why resistance patterns occur.

## Data Management Throughout Collection, Processing, Analysis and Interpretation

**Data collection:** The dataset was obtained from the official UKHSA antimicrobial resistance dashboard. The source is acknowledged so that readers can locate the published data.

**Data inspection and preparation:** The dataset was loaded into Python and inspected for its structure, data types, missing values, duplicate records and plausible resistance percentage values. The analysis focused on the relevant national surveillance measures.

**Data analysis:** Descriptive statistics and visualisations were used to compare resistance percentages across antibiotic categories and examine patterns over time. The published figures were interpreted as three-month rolling measures rather than isolated monthly results.

**Data interpretation and communication:** Findings were presented through the Jupyter Notebook and Tableau Public dashboard. Labels, summaries and explanations were used to make the results understandable to technical and non-technical readers.

**Governance and responsible use:** The analysis uses aggregated national surveillance statistics, not identifiable patient records. The source and applicable reuse conditions should be acknowledged, and the results should not be used to make unsupported claims about individual patients, causes of resistance or clinical treatment decisions.

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


## Ethical Considerations

### Privacy and Data Protection

This project uses publicly available, aggregated UKHSA national surveillance statistics rather than identifiable patient records. The analysis does not attempt to identify individuals. The dataset source is acknowledged, and the data is used for educational and analytical purposes in accordance with applicable reuse conditions.

### Data Governance and Transparency

The dataset's source, reporting period and relevant measurement limitations are documented. The analysis recognises that the published monthly figures represent three-month rolling measures. Surveillance figures may be revised, and changes in antibiotic susceptibility testing standards may affect comparisons over time.

### Bias and Fairness

The dataset provides national-level results and does not represent every patient's individual circumstances. Differences in the populations tested, healthcare settings or testing practices may influence the reported percentages. The findings should therefore not be generalised beyond what the available data supports.

### Responsible Interpretation and Social Impact

Antibiotic resistance is a public health issue, so misleading charts or unsupported claims could cause unnecessary concern or lead to incorrect conclusions. Visualisations use clear labels and percentage values to support accurate interpretation. The analysis describes observed patterns but does not establish their causes, predict individual outcomes or provide treatment recommendations.

### Responsible Use of Generative AI

Generative AI supported aspects of coding, troubleshooting and documentation. Its suggestions were treated as assistance rather than authoritative evidence. Factual claims and conclusions were checked against the dataset and the work performed, recognising that AI can produce inaccurate or misleading information.

## Dashboard Design

The interactive dashboard was developed in Tableau Public to communicate antibiotic resistance patterns in *E. coli* bloodstream infections in England.

### Dashboard Content

The dashboard brings together visualisations that allow readers to:

* Compare resistance percentages across seven antibiotic categories.
* Explore how resistance percentages vary over the reporting period.
* Examine differences in the distribution of reported resistance values.
* Identify patterns across antibiotic categories and dates.

### Communicating Insights to Different Audiences

The dashboard is intended for healthcare professionals, public health practitioners, researchers and interested members of the public. Clear titles, labels, percentage formatting and visual comparisons help readers understand the findings without requiring programming knowledge.

Technical readers can use the dashboard alongside the Jupyter Notebook to understand the analysis in more detail. Non-technical readers can focus on the charts and the main patterns.

### Accessibility and Responsible Presentation

The dashboard uses labelled visualisations and percentage values to support interpretation. The findings should be read alongside the project's documented limitations, particularly the three-month rolling reporting period. The dashboard presents descriptive surveillance information, not individualised clinical advice or evidence of causation.

## User Feedback and Evaluation

The dashboard was reviewed during development to check that its titles, labels, percentage values and visualisations communicate the findings clearly. The presentation was also considered from the perspective of technical and non-technical audiences.

Formal feedback from external users has not yet been collected. Further evaluation could involve asking healthcare professionals, public health practitioners and other intended users to review the dashboard and comment on its clarity, usability and accessibility.

Feedback could then be used to improve the dashboard's layout, explanations and filters. Accessibility and usability testing would also help identify areas that may need improvement.

## Unfixed Bugs and Knowledge Gaps

No specific unresolved technical bugs have been documented at this stage. However, some aspects of the project would benefit from further testing and development.

* **Dashboard usability:** The dashboard would benefit from feedback from intended users to confirm that the charts, labels and filters are easy to understand.
* **Accessibility testing:** Further checks could assess colour contrast, readability and usability for people with different accessibility needs.
* **Data updates:** The project currently uses a downloaded dataset. New UKHSA data would need to be obtained and the analysis rerun manually.
* **Data interpretation:** National aggregated statistics do not explain the causes of resistance or reflect every patient's individual circumstances.
* **Changes in reporting:** Revisions to surveillance figures or changes in testing standards may affect comparisons over time.

These points are recognised as limitations or opportunities for improvement, rather than confirmed software defects.

## Project Reflection and Challenges

### Challenges Faced

During development, the project involved working with surveillance data, checking data quality, selecting suitable visualisations and presenting the results clearly. Building the analysis in Python and creating an interactive Tableau Public dashboard also required learning and troubleshooting across different tools.

These challenges were addressed by inspecting the dataset, checking the analysis outputs, refining the visualisations and documenting the methods and limitations.

### Skills and Learning

The project provided practical experience in data inspection, data preparation, exploratory data analysis, descriptive statistics, hypothesis evaluation and dashboard development. It also strengthened understanding of data governance, privacy, potential bias and the importance of communicating public health information responsibly.

### What Could Be Improved?

Future work could include obtaining and incorporating updated UKHSA data, exploring additional statistical methods where appropriate, and gathering feedback from intended dashboard users. Further accessibility and usability testing would help assess whether the visualisations are clear to different audiences.

This reflection recognises that analytical work involves both technical development and responsible interpretation. Conclusions must remain within the limits of the available evidence.

## Development Roadmap

Future improvements could extend the analysis and strengthen the project's usability and reproducibility.

* **Update the dataset:** Obtain newer UKHSA surveillance data and rerun the analysis when updates become available.
* **Improve dashboard accessibility:** Review colour contrast, labels and readability, and gather feedback from intended users.
* **Extend the analysis:** Explore suitable additional statistical methods if the available data supports them.
* **Improve reproducibility:** Document the update process and ensure that future changes to the dataset are reflected consistently in the notebook and dashboard.
* **Develop analytical skills:** Continue building skills in Python, statistical analysis and dashboard design to support future healthcare data analytics projects.

## Deployment

The interactive dashboard was created using Tableau Public and published online so that users can explore antibiotic resistance trends in *E. coli* bloodstream infections in England.

**View the published dashboard:** [Antibiotic Resistance Analysis | Tableau Public](https://public.tableau.com/app/profile/kav.kavz/viz/AntibioticResistanceAnalysis/AntibioticResistanceDashboard_1?publish=yes)

The dashboard presents resistance percentages across seven antibiotic categories and allows users to explore patterns and changes over time. Tableau Public makes the visualisation accessible online without requiring users to run the Python analysis locally.

The analysis notebook, dataset and project documentation are available in the [GitHub repository](https://github.com/kavithasreesai30-del/antibiotic-resistance-assessment-3).

## Main Data Analysis Libraries

The project uses the following Python libraries for data analysis and visualisation:

* **pandas:** Loading, inspecting and preparing tabular data.
* **NumPy:** Supporting numerical operations.
* **Matplotlib:** Creating charts and visualisations.
* **Seaborn:** Creating statistical visualisations, including distribution plots and heatmaps.

## Tools and Technologies

* **Python** – Data inspection, cleaning, exploratory data analysis and statistical analysis.
* **Jupyter Notebook** – Documentation and execution of the analysis.
* **Tableau Public** – Data visualisation and interactive dashboard development.
* **Visual Studio Code** – Project development and file management.
* **Git and GitHub** – Version control, project documentation and code hosting.


## Credits

* **Data source:** UK Health Security Agency (UKHSA), for the publicly available *E. coli* bacteraemia antimicrobial resistance surveillance data.
* **Analysis and visualisation:** Python libraries and Tableau Public were used to analyse and present the data.
* **Generative AI assistance:** OpenAI ChatGPT and Anthropic Claude supported the project throughout its development, including clarifying concepts, explaining code, troubleshooting errors, refining documentation and discussing analytical approaches. AI-generated suggestions were reviewed and checked against the project work, and the tools were used as assistants rather than substitutes for the analysis and evaluation.


The original data source is acknowledged, and its applicable reuse conditions should be followed.

## Acknowledgements

Thanks to Code Institute for the learning resources and assessment guidance that supported the development of this project.

## Project Status

The project has progressed from initial setup to data analysis, visualisation, ethical review and dashboard publication.

* **Project setup:** Completed.
* **Dataset inspection and preparation:** Completed.
* **Exploratory data analysis and visualisation:** Completed.
* **Statistical analysis and hypothesis evaluation:** Completed.
* **Ethical considerations and limitations:** Documented.
* **Tableau Public dashboard:** Completed and published.
* **Project summary report and analysis outputs:** Completed.
* **README and final documentation:** Completed.
