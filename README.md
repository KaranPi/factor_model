# Full Run of Factor Model

The notebook, `01_full_run.ipynb`, provides a comprehensive pipeline for setting up and running a multi-factor model. The script walks through the steps for importing libraries, loading data, and applying various analyses essential for evaluating factor models. Below is a detailed summary of the code cells, their operations, and the rationale for each step.

---

## Introduction

Factor models are widely used financial tools to evaluate the effects of systematic risk factors on asset returns. This notebook provides an end-to-end execution logic for creating and analyzing factor models using a blend of stock prices, fundamentals, and factor decompositions for U.S. stock data.

---

## Summary of Code Cells

### 1. **Setting up the Project Root**  
   **Code Cell:** Import libraries, define project root, and include it in Python's `sys.path`.  
   **Purpose:** To ensure that all custom modules located in the `src/` folder (like `fm_config`, `fm_data_prices`, etc.) are accessible for imports.  
   - **Key Output:** Confirms if the project root is correctly added to `sys.path`.

---

### 2. **Import Necessary Modules**  
   **Code Cell:** Load various essential libraries from `numpy`, `pandas`, and all relevant `src` modules.  
   **Purpose:**  
   - To establish a standardized library base for handling data.
   - To integrate functional utilities like data loaders, factor builders, etc., into the workflow.

---

### 3. **Initialize Backtest Variables**  
   **Code Cell:** Load key variables like `US_TICKERS` (list of tickers), `START`, and `END` dates.  
   **Purpose:**  
   - This step prepares the universe of U.S. stock tickers and the backtesting time frame.

---

### 4. **Load Historical Price Data**  
   **Code Cell:** Fetch price data for the tickers (`US_TICKERS`) using `load_us_prices()` function.  
   **Purpose:**  
   - Retrieves and saves daily price data in a structured `.parquet` and `.csv` format for fast access.  
   - Displays tail-end stock price data as a preview.

---

### 5. **Load Financial Fundamental Data**  
   **Code Cell:** Import income statements, balance sheets, and cash flow statements using `load_us_income_ttm`, `load_us_balance_ttm`, and `load_us_cashflow_ttm`.  
   **Purpose:**  
   - To fetch and analyze fundamental datasets essential for constructing factor models.  
   - Highlights metrics like total income, assets, liabilities, etc., to understand company performance.

---

### 6. **Preview Datasets**  
   **Code Cells:** Use `.tail()` commands to display previews for the following:  
   - Income statement (`df_inc`)  
   - Balance sheet (`df_bal`)  
   - Cash flow statement (`df_cf`)  

   **Purpose:**  
   - Verifies that the datasets were properly loaded and highlights key financial metrics.

---

### Next Steps:
In a factor model, additional steps such as factor construction, regression analysis, and portfolio decompositions would follow this data ingestion and preview phase. These steps are typically executed using other related notebooks or Python scripts.


---

## Dependencies

- Python 3.9 or higher
- Required libraries: pandas, numpy, matplotlib, etc.
- Custom modules under the `src/` directory, including:
  - `fm_config`
  - `fm_data_prices`
  - `fm_fundamentals`
  - `fm_returns`
  - `fm_factor_model_us`, etc.

---

## Contact

GitHub: [KaranPi](https://github.com/KaranPi)

--- 

```
