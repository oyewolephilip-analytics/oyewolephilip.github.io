# Snowflake Financial Risk Analysis

This project demonstrates how Snowflake Data Cloud can be used to perform financial risk monitoring on stock market data.

## Project Overview

The objective of this analysis is to simulate a cloud-based financial analytics workflow using Snowflake SQL.

Using historical stock data, the project calculates:

- Daily stock returns
- Risk classification
- Volatility monitoring

## Project Purpose

This demonstrates how cloud-based data platforms can be used for financial analytics and risk monitoring.

## Tools Used

Snowflake Data Cloud  
SQL  
Financial Market Data  
Data Analytics  

## Key Analysis

Daily returns were calculated using SQL window functions.

Risk categories were created to classify volatility exposure.

## Example Snowflake Query

```sql
SELECT
DATE_VAL,
SYMBOL,
CLOSE_PRICE,
(CLOSE_PRICE - LAG(CLOSE_PRICE)
OVER (PARTITION BY SYMBOL ORDER BY DATE_VAL))
/
LAG(CLOSE_PRICE)
OVER (PARTITION BY SYMBOL ORDER BY DATE_VAL)
AS DAILY_RETURN
FROM RAW_STOCK_DATA;

```markdown
## Sample Output

![Snowflake Risk Analysis](images/snowflake-risk-analysis.png)

## Key Insight

Monitoring daily return flunctuations allows analysts to identify volatility spikes and potential market risk exposure early.

## Author

**Oyewole Philip**
Risk-Focused Data Analyst
Excel • SQL • Python • Power BI • Snowflake
