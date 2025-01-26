# Stock Market Analysis: Tesla and GameStop

Welcome to the Stock Market Analysis project! This repository showcases a Python-based solution for analysing Tesla and GameStop stock prices and revenue data. Using web scraping with BeautifulSoup and financial data analysis techniques, this project provides insights into historical stock performance and company revenues.

## Project Overview
This project focuses on:

1. Scraping Tesla and GameStop revenue data from financial websites using **BeautifulSoup**.
2. Cleaning and preprocessing financial data (e.g., removing dollar signs and commas).
3. Analysing and visualising stock prices and revenue trends up to June 2021.
4. Integrating stock data and revenue data for an informative graphical representation.

The project highlights:
- Web scraping techniques for extracting structured data from web pages.
- Financial data preprocessing and visualisation using **Pandas** and **Plotly**.
- Combining multiple datasets to gain insights into business performance and market trends.

## Features
- Web scraping revenue data for Tesla and GameStop.
- Data cleaning and preparation for revenue columns.
- Visualisation of:
  - Historical share prices.
  - Annual revenue trends.
- Scalable and reusable functions for future financial data analysis.

## Tools and Technologies
- **Python**: Core programming language.
- **BeautifulSoup**: Web scraping library for extracting HTML data.
- **Pandas**: Data manipulation and analysis.
- **Plotly**: Interactive data visualisation.

## Data Sources
- Stock prices were sourced from financial APIs or pre-downloaded CSV files.
- Revenue data was scraped from publicly available financial websites.

## Installation and Setup
To run this project locally:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Analysing-Historical-Stock-Revenue-Data.git
   cd Analysing-Historical-Stock-Revenue-Data

   ```

2. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the script:
   ```bash
   python main.py
   ```

## Project Structure
```
.
├── notebook/                # Python scripts for data extraction and visualization
├── requirements.txt         # Required Python libraries
├── README.md                # Project documentation
```

## Key Functions
### 1. Web Scraping Revenue Data
```python
from bs4 import BeautifulSoup
import requests

# Example: Scraping Tesla Revenue Data
def scrape_tesla_revenue():
    url = "TESLA_REVENUE_URL"
    response = requests.get(url)
    soup = BeautifulSoup(response.text, "html.parser")
    # Extract and process data here
```

### 2. Data Cleaning
```python
# Cleaning Revenue Data
def clean_revenue_data(df):
    df["Revenue"] = df["Revenue"].str.replace("$", "").str.replace(",", "")
    df["Revenue"] = pd.to_numeric(df["Revenue"], errors="coerce")
```

### 3. Visualisation
```python
# Plotting Tesla Stock Data
def make_graph(stock_data, revenue_data, stock_name):
    fig = make_subplots(rows=2, cols=1, shared_xaxes=True, ...)
    fig.show()
```

## Example Visualisations
### Tesla Stock Prices and Revenue

<img src="example_tesla_graph.png" alt="Tesla Stock Graph" width="600">

### GameStop Stock Prices and Revenue

<img src="example_gme_graph.png" alt="GameStop Stock Graph" width="600">

## Challenges and Learnings
1. **Web Scraping:** Handling dynamic content and multiple table classes.
2. **Data Cleaning:** Dealing with inconsistent data formats in revenue columns.
3. **Visualisation:** Ensuring clear and intuitive representation of data.

## Future Enhancements
- Integrate live data using financial APIs (e.g., Yahoo Finance or Alpha Vantage).
- Automate stock trend analysis for additional companies.
- Deploy the solution as a web app using Flask or Streamlit.


## Contributions
Contributions are welcome! Feel free to open an issue or submit a pull request.



