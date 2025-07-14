# Advanced Company Profiling and Data Validation

This project presents a complete data engineering solution for profiling, cleansing, deduplicating, validating, and enriching company data using the **Companies House REST API**. It demonstrates practical data engineering skills using Python and Jupyter Notebook, ending with interactive visualizations.

---

## Objective

To develop a system that:
- Profiles and cleans sample company data
- Deduplicates using exact and fuzzy matching
- Validates company names against the Companies House API
- Enriches each record with company metadata (status, address, incorporation date, etc.)
- Generates both static and interactive reports and visualizations

---

## Project Structure

| File | Description |
|------|-------------|
| `Advanced_Company_Profiling.ipynb` | Main Jupyter notebook with all steps and visualizations |
| `CompanyV2 (July 2025).csv` | Sample input dataset containing UK companies |
| `README.md` | You're reading it! Project overview and instructions |

---

## Technologies Used

- Python 3
- Pandas & NumPy
- Seaborn & Matplotlib
- Plotly (for interactive charts)
- Requests (for API calls)
- tqdm (for progress bar during enrichment)
- Regex & string preprocessing

---

## Steps Covered

### 1. Data Collection
- Reads company data from the provided `Company.csv`

### 2. Data Profiling
- Summary statistics, missing values, data types

### 3. Data Cleansing
- Standardizes casing, trims spaces

### 4. Deduplication
- Removes exact duplicates based on name + address
- Performs fuzzy deduplication using normalized names

### 5. Matching
- Calls the Companies House `search/companies` API for each name (sampled to 100 records to stay under rate limits)

### 6. Enrichment
- Adds company status, creation date, CH company number, and registered address

### 7. Reporting & Visualization
- Company status breakdown
- Companies by year of incorporation
- Top cities by company density
- Enrichment error summary
- Word cloud of company names
- Interactive plots via Plotly

---

## 8. API Key Setup

You must get your **LIVE API key** from the [Companies House Developer Portal](https://developer.company-information.service.gov.uk/manage-applications).  
Paste it directly into the notebook:

```python
API_KEY = "your_actual_api_key_here"
