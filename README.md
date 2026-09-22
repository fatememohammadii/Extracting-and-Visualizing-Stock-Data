# Extracting and Visualizing Stock Data

## Project Overview

This repository contains a Python notebook focused on extracting historical stock and revenue data for **Tesla (TSLA)** and **GameStop (GME)**, cleaning and processing the extracted datasets, and visualizing the relationship between stock performance and revenue using custom plotting functions.

The project demonstrates two fundamental methods of data collection in Data Science:

1. **Financial APIs:** Using the `yfinance` library to retrieve historical market stock prices.
2. **Web Scraping:** Utilizing `requests`, `BeautifulSoup`, and `pandas` to extract and sanitize web table revenue data.

---

## Project Structure & Workflow

1. **Data Extraction with `yfinance**`:
* Initialized `Ticker` objects for Tesla (`TSLA`) and GameStop (`GME`).
* Extracted max-period historical market data into Pandas DataFrames.
* Standardized DataFrames by resetting indices.


2. **Web Scraping Financial Tables**:
* Extracted quarterly revenue data from online HTML sources using `requests` and `BeautifulSoup` (or `pd.read_html`).
* Standardized table headers into `Date` and `Revenue`.


3. **Data Cleaning & Preprocessing**:
* Stripped unwanted symbols like commas (`,`) and dollar signs (`$`) from raw revenue strings.
* Dropped `NaN` / null values and filtered out empty string records.


4. **Visualization**:
* Implemented a custom `make_graph` plotting helper leveraging `Matplotlib` to render side-by-side subplots comparing historical share prices against quarterly revenue over time.



---

## Dependencies & Installation

To run this notebook locally, ensure you have Python 3 installed alongside the required packages:

```bash
pip install yfinance bs4 pandas requests matplotlib html5lib

```

---

## Key Modules Used

* **`yfinance`**: Fetching stock prices directly from Yahoo Finance.
* **`requests`**: Fetching remote raw HTML pages.
* **`BeautifulSoup` (`bs4`)**: Parsing and navigating the HTML DOM structure.
* **`pandas`**: Data cleaning, DataFrame operations, and direct table parsing.
* **`matplotlib`**: Plotting static subplots for price and revenue trends.

---

## Usage Instructions

1. Clone this repository to your local machine:
```bash
git clone https://github.com/your-username/your-repo-name.git

```


2. Open the Jupyter Notebook:
```bash
jupyter notebook

```


3. Run all cells sequentially to execute data ingestion, cleaning, and graph generation.
