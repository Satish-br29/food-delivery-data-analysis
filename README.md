# Food Delivery Operations – Data Analytics

**Kagnus Data Analytics Challenge | Four-Week Project**

## Project Overview

This project focuses on analyzing food delivery operations using data analysis techniques. The objective is to understand how delivery duration varies across available operational factors and communicate findings using numerical evidence and visualizations.

## Project Objectives

- Understand and inspect the food delivery dataset.
- Identify missing values, duplicates, inconsistent labels and unusual values.
- Clean and prepare the dataset for analysis.
- Explore delivery-duration patterns across available operational fields.
- Create visualizations and evidence-based observations.
- Communicate findings and recommendations in a final report.

## Dataset Information

- **Dataset:** Food Delivery Dataset
- **Source:** [Kagnus-provided Food Delivery Dataset](https://drive.google.com/file/d/1O9WYS92iJPZoC6skyYlpcdP8Kre7eW6z/view?usp=sharing)
- **Original dataset size:** 45,584 rows and 20 columns
- **Domain:** Food Delivery Operations

The dataset was inspected using its actual column names and values.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab / Jupyter Notebook

## Project Structure

```text
food-delivery-data-analysis/
├── data/
│   ├── raw/
│   │   └── README.md
│   └── processed/
│       └── cleaned_food_delivery.csv
├── notebooks/
│   └── 01_data_understanding_and_cleaning.ipynb
├── docs/
│   └── cleaning_log.csv
├── README.md
└── requirements.txt
```

## Week 1 – Understand and Prepare

### Work Completed

- Inspected dataset dimensions, column names and data types.
- Reviewed sample records and descriptive statistics.
- Created a column overview with descriptions.
- Checked missing values and their percentages.
- Checked duplicate rows and duplicate order IDs.
- Inspected categorical values for inconsistencies.
- Examined numerical ranges and negative values.
- Inspected date and time fields.
- Created a separate cleaned dataset.
- Documented cleaning actions in a cleaning log.
- Exported and verified the cleaned dataset.

### Initial Dataset Observations

- The dataset contains 45,584 records and 20 columns.
- Missing values were found in 9 columns.
- A total of 9,131 missing cells were identified.
- No completely duplicated rows were found.
- No duplicate order IDs were found.
- Negative restaurant coordinates were observed and retained for investigation because negative geographic coordinates can be valid.

### Week 1 Deliverables

- Dataset profile and quality checks.
- Documented cleaning decisions.
- Cleaned dataset in CSV format.
- Cleaning log.
- Data understanding and cleaning notebook.

## Four-Week Roadmap

| Week | Focus |
|---|---|
| Week 1 | Understand and prepare |
| Week 2 | Explore patterns |
| Week 3 | Visualize and interpret |
| Week 4 | Synthesize findings and recommendations |

## How to Run

1. Clone or download this repository.
2. Install dependencies using:

   `pip install -r requirements.txt`

3. Open the notebook in Google Colab or Jupyter Notebook.
4. Download the original dataset from the source link above and upload it to the notebook environment.
5. Ensure the CSV file path matches the path used in the notebook.
6. Run the notebook cells in order.

## Notes and Limitations

- The original dataset is kept separate from the cleaned dataset.
- The raw dataset is not included in this repository; refer to the source link.
- Cleaning decisions and assumptions are documented in the notebook and cleaning log.
- Unverified values are not automatically assumed to be incorrect.
- Associations observed during analysis should not be interpreted as proof of causation.

## Week 2: Exploratory Data Analysis (EDA)

### Objective
Explore the cleaned food delivery dataset to understand the factors associated with delivery duration.

### Analysis Performed
- Calculated delivery duration statistics, including mean, median, percentiles, and standard deviation.
- Analyzed delivery duration across different traffic conditions.
- Compared delivery duration across weather conditions.
- Calculated approximate straight-line distance using the Haversine formula.
- Examined the relationship between distance and delivery duration.
- Compared delivery duration across vehicle types.
- Analyzed the effect of multiple deliveries on delivery duration.
- Explored delivery person ratings and their relationship with delivery duration.

### Key Findings
- Average delivery duration: 26.29 minutes.
- Jam traffic had an average delivery duration of 31.18 minutes.
- Cloudy weather had an average delivery duration of 28.92 minutes.
- Distance and delivery duration had a positive correlation of 0.321.
- Motorcycle deliveries had an average duration of 27.61 minutes.
- Records with 3 multiple deliveries had an average duration of 47.82 minutes.

### Visualization
- Initial Distance vs Delivery Duration: `visualizations/initial_distance_vs_duration.png`

### Data Limitations
- Partner experience information was not available.
- 4,071 records were excluded from distance analysis due to suspicious coordinates.
- Calculated distance represents straight-line distance, not actual road distance.
- 53 records contained an unusual rating value of 6.0 and were retained without modification.

### Tools Used
Python, Pandas, NumPy, Matplotlib, Seaborn.
