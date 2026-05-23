# Python Finance ML Analytics

Python/Jupyter finance and machine-learning analysis using `pandas`, `NumPy`, `Matplotlib`, `yfinance`, FRED macroeconomic data, SEC Company Facts, Stooq, `pandas-datareader`, and `scikit-learn` to analyze Microsoft and peer technology stocks, compare valuation metrics, test macroeconomic relationships, and compare predictive models.

## Project Overview

This repository contains a portfolio version of a university data science and machine-learning notebook. The project began as a finance-focused Project 3 analysis and was later extended for Project 4 with machine-learning techniques.

The notebook demonstrates:

- public financial and market data retrieval with `yfinance`
- annual financial-data fallback handling with SEC Company Facts
- historical price-data fallback handling with Stooq
- macroeconomic data retrieval from FRED through `pandas-datareader`
- tabular data preparation and alignment with `pandas`
- numerical work with `NumPy`
- visual analysis with `Matplotlib`
- PE ratio and revenue trend analysis
- peer comparison across technology-sector companies
- COVID-period stock behavior review
- linear regression and multiple linear regression
- polynomial regression
- random forest regression
- train/test split evaluation
- written interpretation of analytical findings

## Repository Contents

- `finance-analysis.ipynb` — public portfolio version of the notebook
- `README.md` — project context, assignment prompt, feedback, tools, and usage notes
- `requirements.txt` — Python package requirements
- `.github/workflows/run-notebook.yml` — GitHub Actions workflow for rerunning the notebook and committing updated outputs

The original class filename included a student identifier. This public version uses a descriptive filename instead.

## Academic Context

This notebook grew out of two related university assignments completed in Spring 2025:

1. **Project 3: Data Science Using Python, Pandas, and MatPlotLib**
2. **Project 4: Machine Learning & Data Science Using Python, Pandas, MatPlotLib, SkiLearn**

Project 3 required a finance-focused data science analysis using Python, pandas, Matplotlib, and `yfinance`. Project 4 required students to extend their Project 3 work with machine-learning techniques.

The Project 3 submission received **105/100**.  
The Project 4 submission received **100/100**.

Instructor feedback for Project 3:

> WOW! Excellent work and I really enjoyed your narrative presentation in your notebook! (+5 for exceeding expectations)
>
> Way to go on this Kyle!
>
> -Scott

## Relevant Assignment Prompt

Only the finance-track portions of the original assignments are reproduced below because those are the portions this project completed.

### Project 3: Data Science Using Python, Pandas, and MatPlotLib

**Purpose:** This project provided students with the opportunity to answer study questions using Python on data retrieved from multiple sources. Students were required to create a Jupyter Notebook containing markdown and code that met the assignment specifications.

**Finance study questions:**

1. Using `yfinance`, create an analysis of Microsoft’s, or another publicly traded company’s, Price-to-Earnings ratio for the past 8 years. The assignment required data from multiple sources to determine PE ratio and required correlation of Microsoft’s PE ratio to earned revenue.

   **Question 1:** Is there a correlation of PE to earned revenue for Microsoft?

   The answer had to include an appropriate visualization and written discussion.

2. Choose five other stocks in the same sector as the stock selected in Step 1. Determine the average PE ratios for the five selected stocks over the past 8 years.

   **Question 2:** How does the PE to earned revenue of the stock in Step 1 compare to the average PE to earned revenue for the five stocks selected in this step?

   Required visualizations included:

   - a line chart depicting PE ratios for all six stocks
   - a five-number summary visualization of stock prices for all six stocks over the last 90 days

   **Question 3:** Was the selected industry affected by COVID in the first and second quarters of 2020? The answer had to be justified using data and visualizations.

   The assignment also required a visualization depicting the relative distribution of revenue for the six stocks by year.

**Project 3 grading rubric:**

1. Did the submission answer the data science questions, and did the analysis support the answers?
2. Were the visualizations complete, visually appealing, and properly labeled?

### Project 4: Machine Learning & Data Science Using Python, Pandas, MatPlotLib, SkiLearn

**Purpose:** This project required students to expand their Project 3 answers using machine-learning techniques. Students were instructed to create a copy of their Project 3 Jupyter Notebook as a starting point and extend the analysis.

**Finance study questions:**

1. Using the stock selected in Project 3, extend the analysis to answer the following:

   **Question 1:** Is there a correlation of inflation to earnings for Microsoft? Earnings and inflation had to be analyzed on a per-month basis for the past 36 months.

   This required a simple linear regression, an appropriate visualization, and written discussion.

   **Question 2:** Using `split_test_train`, double the training sample size and run a new linear regression. Did the predictions change?

2. From the five peer stocks, answer the following:

   **Question 2:** Is the average stock price of stocks in this sector affected by both inflation and consumer confidence? This required multiple linear regression.

   The answer had to include a visualization and confusion matrix.

   **Question 3:** Choose another variable that may affect this market sector, then perform an appropriate analysis to determine whether that variable is correlated with the market sector. Appropriate graphs, models, and discussion were required.

   **Question 4:** For the single stock selected in Question 1, use the stock’s closing price to compare the following models:

   - actual closing price
   - predicted closing price using Linear Regression
   - predicted closing price using Polynomial Regression
   - predicted closing price using Random Forest

   The assignment also required a forecast of the closing price for June 1, 2025 from each model.

**Project 4 grading rubric:**

1. Did the submission answer the data science questions, and did the analysis and models support the answers?
2. Were the visualizations complete, visually appealing, and properly labeled?

## Analysis Scope

The notebook focuses on Microsoft and technology-sector peer companies.

Project 3 scope:

- Microsoft PE ratio and revenue comparison
- peer-company PE ratio comparison
- stock-price five-number summary over a recent 90-day window
- COVID-period price behavior review for Q1 and Q2 2020
- revenue-distribution visualizations across selected stocks

Project 4 extension:

- Microsoft earnings compared against monthly inflation
- train/test split comparison for regression robustness
- sector valuation analysis against inflation and consumer confidence
- unemployment-rate analysis as an additional macroeconomic hypothesis
- model comparison for Microsoft closing price using Linear Regression, Polynomial Regression, and Random Forest
- forecast comparison for June 1, 2025

## Tools Used

- Python
- Jupyter Notebook
- pandas
- NumPy
- Matplotlib
- yfinance
- SEC Company Facts
- Stooq
- FRED
- pandas-datareader
- scikit-learn
- GitHub Actions

## Risk Analytics Relevance

Although this is an educational finance and machine-learning project rather than a production banking model, it demonstrates skills relevant to risk analytics and investigative data work:

- pulling data from multiple public sources
- aligning inconsistent financial, market, and macroeconomic datasets
- calculating derived metrics
- testing relationships between variables
- comparing peer entities
- building and evaluating regression models
- using train/test splits
- visualizing trends, distributions, and model outputs
- documenting assumptions, limitations, and analytical reasoning
- translating code-based analysis into written findings for a reader

## Important Limitations

This project is educational and portfolio-oriented. It is not financial advice, investment advice, or a production-grade financial risk model.

The financial calculations are simplified and depend on public data availability. A production model would require stronger source controls, audited period-specific financial inputs, consistent share-count methodology, and more rigorous validation.

Because `yfinance`, FRED, SEC Company Facts, and Stooq retrieve live public data, outputs may change over time depending on API availability, restatements, market dates, source updates, and public endpoint rate limits.

This repository includes a GitHub Actions workflow that can rerun the notebook and commit updated outputs. The workflow includes retry handling because unauthenticated public data sources may occasionally rate-limit shared GitHub Actions runners or return temporary malformed responses. If a workflow run fails because of a data-source issue, rerunning the workflow may succeed without code changes.

Some model outputs should be interpreted as demonstrations of analytical technique rather than reliable forecasts. The notebook is intended to show data preparation, model construction, visualization, and reasoning, not to predict actual future stock prices.

## Running the Notebook

Install dependencies:

```bash
pip install -r requirements.txt
```

Open the notebook:

```bash
jupyter notebook finance-analysis.ipynb
```

Run all cells from top to bottom. The notebook requires internet access because it retrieves public financial, market, and macroeconomic data from live data sources.

## GitHub Actions Workflow

The repository includes a workflow that can run the notebook online and commit the executed notebook back to the repository.

The workflow:

- installs the Python dependencies from `requirements.txt`
- clears stale notebook outputs
- executes the notebook
- retries execution if a temporary data-source failure occurs
- commits the updated `finance-analysis.ipynb` file back to the repository

Manual execution path:

```text
GitHub repository → Actions → Run finance notebook → Run workflow
```

## Suggested Portfolio Summary

This project extends a Python finance analytics notebook into a machine-learning analysis using public stock and macroeconomic data. It compares Microsoft with technology-sector peer companies, analyzes PE ratios and revenue trends, tests macroeconomic relationships, and compares regression and random forest models. The work demonstrates practical Python analytics, data preparation, visualization, and written interpretation relevant to risk analytics and investigative data review.
