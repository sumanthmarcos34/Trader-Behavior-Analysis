# Trader Behavior vs Market Sentiment Analysis

## Overview

This project analyzes the relationship between **Bitcoin market sentiment (Fear & Greed Index)** and **trader performance** using historical trading data from the Hyperliquid platform. The goal is to uncover patterns in trading behavior and profitability under different market sentiment conditions.

---

## Objective

Market sentiment often influences trader psychology and decision-making.
This project aims to explore:

* How trader profitability changes during **Fear vs Greed markets**
* Differences in **trade size and activity** across sentiment states
* **Buy vs Sell behavior** during different market conditions
* Identification of **top performing traders**

---

## Datasets Used

### 1. Bitcoin Fear & Greed Index

Contains daily sentiment classification for the Bitcoin market.

**Columns**

* Date
* Classification (Fear / Greed)

### 2. Hyperliquid Historical Trader Data

Contains detailed trading activity including execution price, trade size, and realized profit or loss.

**Important Columns**

* Account
* Coin
* Execution Price
* Size USD
* Side (Buy/Sell)
* Timestamp
* Closed PnL

---

## Data Processing

The following preprocessing steps were performed:

1. Loaded both datasets using **Pandas**
2. Cleaned column names and handled missing values
3. Converted timestamps to proper datetime format
4. Extracted trading **date** from timestamps
5. Merged trading data with sentiment data using the **date column**

This produced a unified dataset linking **each trade to the corresponding market sentiment**.

---

## Exploratory Data Analysis

The following analyses were performed:

* Profit distribution across sentiment states
* Trade size comparison between Fear and Greed periods
* Buy vs Sell trading activity
* Profit distribution across trader accounts
* Identification of top profitable traders

Visualizations were created using **Matplotlib and Seaborn**.

---

## Key Insights

* Traders tend to take **larger positions during Greed market sentiment**, indicating higher risk appetite.
* Average profitability increases during **Greed periods**, likely due to bullish market momentum.
* **Fear periods show more cautious trading behavior** with smaller trade sizes.
* A small number of accounts generate **a large portion of total profits**, indicating concentrated trading expertise.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## Project Structure

```
trader-sentiment-analysis
│
├── data
│   ├── historical_data.csv
│   └── fear_greed_index.csv
│
├── trader_sentiment_analysis.ipynb
├── insights.md
└── README.md
```

---

## How to Run

1. Clone the repository
2. Install dependencies
3. Open the Jupyter Notebook
4. Run all cells to reproduce the analysis

```
pip install pandas numpy matplotlib seaborn
```

---

## Conclusion

This project demonstrates how **market sentiment influences trader behavior and profitability in crypto markets**. Integrating sentiment indicators with trading data can help identify behavioral patterns and support better trading strategies.
