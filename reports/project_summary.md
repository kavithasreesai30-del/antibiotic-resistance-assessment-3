# Antibiotic Resistance Analysis: Project Summary

## Project Overview

This project explores antibiotic resistance trends in *E. coli* bloodstream infections in England using publicly available surveillance data from the UK Health Security Agency (UKHSA).

The project demonstrates data preparation, exploratory data analysis, statistical summaries, visualisation, ethical interpretation and interactive dashboard development.

## Dataset

The dataset contains 427 records and 13 columns, covering July 2021 to July 2026. It includes monthly resistance percentages for seven antibiotic categories.

The data represents aggregated national surveillance statistics rather than identifiable patient records. Monthly values are based on three-month rolling measures.

## Methodology

The project used Python and Jupyter Notebook to inspect the dataset, assess data quality, explore resistance patterns, calculate descriptive statistics and evaluate the project hypotheses.

Line charts, bar charts, box plots and a heatmap were used to explore differences between antibiotics and changes over time. Tableau Public was used to develop an interactive dashboard.

## Key Findings

* Co-amoxiclav had the highest mean resistance percentage at 42.69%.
* Carbapenems had the lowest mean resistance percentage at 0.21%.
* Amikacin had a mean resistance percentage of 2.76%.
* Resistance patterns varied across antibiotic categories over the study period.

These findings support the hypotheses that resistance differs between antibiotics and that some antibiotics have lower resistance percentages than others. Changes over time require cautious interpretation.

## Ethical Considerations and Limitations

The analysis uses aggregated public surveillance data and does not attempt to identify individuals. Findings are interpreted cautiously and are not used to establish causes or predict future resistance.

The data may be revised, and changes in susceptibility-testing standards may affect comparisons. The analysis is descriptive and is limited to the available dataset.

## Dashboard

The interactive dashboard is published on Tableau Public:

[View Antibiotic Resistance Analysis](https://public.tableau.com/app/profile/kav.kavz/viz/AntibioticResistanceAnalysis/AntibioticResistanceDashboard_1?publish=yes)

## Future Improvements

Future work could incorporate updated surveillance data, investigate additional statistical methods where appropriate, and gather feedback from intended users to assess dashboard clarity, accessibility and usability.
