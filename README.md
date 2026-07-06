# Philippine E-Commerce Sales Analysis

**Builder:** Ray Cancino
**Cohort:** 2026-A
**Program:** Data Engineering Pilipinas — Open Track

---

## Problem Statement

Philippine e-commerce has grown significantly over the past few years, but there is limited publicly available analysis on which product categories are driving growth, what the seasonal patterns look like, and how regional differences affect sales volume. This project aims to answer those questions using publicly available sales data.

## Data Source

- **Primary:** [PSA Retail Trade Statistics](https://psa.gov.ph/statistics/retail-trade) — annual retail trade survey data, downloaded as CSV from the PSA OpenSTAT portal
- **Secondary:** Lazada and Shopee product listing data — scraped using Python `requests` + `BeautifulSoup` from public category pages (no login required)

## Project Structure

```
dep-data-engineering-ray/
├── data/
│   ├── raw/            ← raw data from PSA and scraped sources
│   └── processed/      ← cleaned and transformed datasets
├── scripts/
│   ├── ingest.py       ← fetches and stores raw data
│   └── transform.py    ← cleans, joins, and models the data
├── notebooks/          ← exploratory analysis and visualizations
├── output/
│   └── figures/        ← saved charts and visuals
├── dashboard/
│   └── index.html      ← deployed dashboard
└── requirements.txt
```

## How to Run

```bash
# Set up environment
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# Ingest raw data
python scripts/ingest.py

# Transform and clean
python scripts/transform.py
```

## Key Questions

1. Which product categories grew the most between 2022 and 2025?
2. Are there clear seasonal peaks (e.g. 11.11, 12.12 sale events)?
3. How do Metro Manila sales volumes compare to provincial regions?

## Dashboard

Live dashboard (Phase 6): _coming soon_

---

*This project is part of the DEP Data Engineering Open Track 2026-A cohort.*
