# Optimizing Conversion Rates with A/B Testing

## Project Overview
The product team redesigned the website's checkout page (Variant B) to reduce friction and improve the user experience. The objective of this project is to analyze the results of an A/B test to determine if the new design leads to a statistically significant increase in the conversion rate compared to the existing design (Variant A).

## Tech Stack
* **Language:** Python
* **Database:** SQLite
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Statsmodels

## Project Workflow
1. **Database Creation:** Generated synthetic A/B test data for 2,000 users and stored it in a local SQLite database (`product_data.db`).
2. **Data Extraction:** Queried the database using SQL within Python to extract the test results.
3. **Exploratory Data Analysis (EDA):** Grouped the data to calculate the baseline and treatment conversion rates.
4. **Statistical Testing:** Conducted a Two-Proportion Z-Test to evaluate statistical significance ($\alpha = 0.05$).
5. **Data Visualization:** Created a clean, business-ready bar chart using Seaborn to visualize the performance of both variants.

## Key Findings
* **Variant A (Old Design):** 10.0% Conversion Rate
* **Variant B (New Design):** 13.1% Conversion Rate
* **Statistical Significance:** The Z-test returned a **p-value of 0.0301**. Since $p < 0.05$, we reject the null hypothesis. 

![AB Test Bar Chart](https://github.com/pnistha11/A-B-Testing/blob/main/Figure_1.png) *(Note: Upload your bar chart image to GitHub and replace this link)*

## Business Recommendation
The new design (Variant B) resulted in a **31% relative lift** in the conversion rate (from 10.0% to 13.1%). Because these results are statistically significant, I recommend **launching Variant B to 100% of website traffic**. 

Assuming a baseline traffic of 50,000 users per month, this 3.1% absolute improvement translates to roughly **1,550 additional conversions per month** with no additional marketing spend.

## How to Run
1. Clone this repository.
2. Install the required libraries: `pip install pandas numpy matplotlib seaborn statsmodels`
3. Run the python script: `python ab_test.py`
