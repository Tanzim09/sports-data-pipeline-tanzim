
# Sports Data Pipeline & IPL Exploratory Data Analysis

## Overview

This project presents a complete mini pipeline for sports data processing using IPL (Indian Premier League) match and ball-by-ball datasets. The goal was to simulate a real-world data internship task by collecting, cleaning, and analyzing sports data to uncover patterns and insights.

IPL cricket data was used as the data source, and the system was built using Python with Jupyter Notebooks. The pipeline covers raw data extraction using the Kaggle API, data cleaning and preprocessing, and comprehensive Exploratory Data Analysis (EDA).

## Project Structure

```
sports-data-pipeline/
│
├── data/
│   ├── raw/
│   │   └── ipl_data/
│   │       ├── deliveries.csv
│   │       ├── matches.csv
│   │       └── ipl-complete-dataset-20082020.zip
│   └── cleaned/
│       └── ipl_cleaned.csv
│
├── scripts/
│   └── data_collection&data_cleaning.ipynb
│
├── eda/
│   └── eda_report.ipynb
│
└── README.md
```

## Key Components

### 1. Data Collection

- Data was fetched using the Kaggle API from the dataset: [IPL Complete Dataset (2008–2020)](https://www.kaggle.com/datasets/patrickb1912/ipl-complete-dataset-20082020)
- The zip was downloaded to `data/raw/ipl_data/` and extracted programmatically.

### 2. Data Cleaning

- Raw files `matches.csv` and `deliveries.csv` were processed.
- Cleaning steps included:
  - Dropping irrelevant columns.
  - Handling missing values.
  - Unifying team name formats.
  - Removing duplicate rows.
  - Sorting by match and season.
- Final output saved as `data/cleaned/ipl_cleaned.csv`.

### 3. Exploratory Data Analysis (EDA)

Performed in `eda/eda_report.ipynb`. Key insights include:

- **Top Scoring Teams**: RCB, MI, and CSK dominate in run scoring.
- **Leading Batsmen**: Virat Kohli, Suresh Raina, and David Warner top the charts.
- **Common Dismissals**: Caught is the most frequent dismissal method.


Plots and visuals were generated using `matplotlib` and `seaborn`.

### Additional Insights from EDA

- match_id  inning           batting_team                 bowling_team  over  \
- ball       batter   bowler  non_striker  batsman_runs  extra_runs  \
- sns.barplot(x=top_batsmen.values, y=top_batsmen.index, palette='viridis')
- sns.barplot(x=team_runs.index, y=team_runs.values, palette='coolwarm')
- sns.countplot(data=data, x='batsman_runs', palette='pastel')
- Matches with Collapse (3+ wickets in 3 overs):

## How to Run

1. Clone the repository.
2. Install required Python libraries (`pandas`, `matplotlib`, `seaborn`, `jupyter`).
3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
4. Run `scripts/data_collection&data_cleaning.ipynb`.
5. Then explore the `eda/eda_report.ipynb` notebook.

## Requirements

- Python 3.x
- pandas
- matplotlib
- seaborn
- jupyter
- kaggle

## Submission Checklist

- [x] Raw and cleaned data in `data/`
- [x] Notebook for data collection and cleaning
- [x] EDA notebook with plots and insights
- [x] README with explanation and findings
- [ ] Add video demo link here

## Notes

This project addresses an internship challenge requiring end-to-end data pipeline implementation and EDA. The focus was on clarity, structure, and insight generation over completeness.
