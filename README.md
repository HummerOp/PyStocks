# AI-Based Sentiment Analysis and Financial Factor Extraction from 10-K Reports

This project uses AI and Python to extract sentiment scores and key financial factors from 10-K filings of companies in the technology sector. The aim is to automate the analysis of financial disclosures and prepare the data for regression modeling in Excel.

---

## 📌 Project Overview

- **Data Source**: 10-K filings from EDGAR (2009–2019)
- **Sectors**: Technology Services or Electronic Technology (based on TradingView components)
- **Items Analyzed**: Item 1, 1A, 1B, 3, and 7A from each 10-K
- **Output**: Sentiment score (0–10), financial ratios, and structured Excel sheet
- **Tools**: Python (PyCharm), AI/NLP model, Tkinter GUI, GitHub for tracking

---

## 🔄 Workflow Summary

1. **Data Collection**
   - Download 10-K reports for each selected company from EDGAR.
   - Filter companies using [TradingView’s Technology Services sector](https://www.tradingview.com/symbols/SP-S5INFT/components/).

2. **Data Processing**
   - Extract specific sections (Item 1, 1A, 1B, 3, 7A).
   - Use AI to assign sentiment scores:
     - `0–4`: Negative  
     - `5`: Neutral  
     - `6–10`: Positive
   - Calculate additional financial ratios from a predefined list of factors.
3. **Calculate the following financial ratios**
     - **Current Ratio** = Current Assets / Current Liabilities
     - **ROA** = (Net Income / Total Assets) × 100
     - **Price to Earnings (P/E)** = Market Price per Share / EPS
     - **Price to Book (P/B)** = Market Price per Share / Book Value per Share
     - **Dividend Yield** = (Annual Dividends / Share Price) × 100
     - **Equity Multiplier** = Total Assets / Shareholders’ Equity
4. **Data Output**
   - Organize per-company data into structured Excel sheets:
     ```
     Company Name
     Year | Sentiment Score | Share Price at 1/1 | Extra Factors...
     ```

5. **Analysis**
   - Perform regression analysis in Excel.
   - Use results for report writing or further modeling.

---

## 💻 Tools & Technologies

- **Python 3.9+**
- **PyCharm** – development IDE
- **Tkinter** – GUI for user inputs or status monitoring
- **Pandas / NumPy / OpenPyXL** – data processing & Excel integration
- **HuggingFace Transformers or SpaCy** – NLP for sentiment analysis
- **GitHub** – version control & project documentation

---

## 📁 Repository Structure

````

📦project-root/
┣ 📂data/                   # Raw and processed reports
┣ 📂notebooks/              # Jupyter notebooks for EDA/testing
┣ 📂scripts/                # Python scripts for downloading, processing
┣ 📂gui/                    # Tkinter GUI interface
┣ 📂models/                 # Trained AI/NLP models
┣ 📂excel\_exports/          # Final Excel files
┣ 📄factors\_reference.pdf   # PDF listing all financial ratios to extract
┣ 📄README.md               # This file
┣ 📄requirements.txt        # Python dependencies

````

---

## 📊 Example Output (Excel)

| Year | Sentiment Score | Share Price (1/1) | Current Ratio | ROA (%) | P/E | P/B | Dividend Yield (%) | Equity Multiplier |
|------|------------------|-------------------|---------------|---------|-----|-----|---------------------|--------------------|
| 2009 | 4.2              | 85.32             | 1.34          | 5.3     | 18.2| 3.2 | 1.25                | 2.1                |
| 2010 | 6.8              | 90.11             | 1.41          | 6.0     | 17.8| 3.4 | 1.40                | 2.0                |

---

## 🧠 Notes

- Only the 10 reports (2009–2019) per company are used — no other filings are retained.
- GitHub history serves as a chronological record for building the final project report.

---

## 🚀 Getting Started

1. Clone the repo:
   ```bash
   git clone https://github.com/HummerOp/PyStocks
   cd PyStocks

2. Create a virtual environment and install dependencies:

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. Launch the Tkinter GUI or run a script:

   ```bash
   python gui/main.py
   ```

---

## ✅ To-Do

* [ ] Finalize list of companies (Technology Services vs. Electronic Technology)
* [ ] Develop sentiment analysis model
* [ ] Integrate Excel export with formatting
* [ ] Regression analysis tooling (Excel formulas or Python)
* [ ] Add full instructions for setting up GUI

---

## 📄 License

This project is licensed under the MIT License. See `LICENSE` for more information.
