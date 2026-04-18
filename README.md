# Apartment Data Parser

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.11+-blue?logo=python" alt="Python">
  <img src="https://img.shields.io/badge/BeautifulSoup-scraping-orange" alt="BeautifulSoup">
  <img src="https://img.shields.io/badge/pandas-data%20analysis-blue?logo=pandas" alt="pandas">
  <img src="https://img.shields.io/badge/CSV%2FJSON-export-green" alt="Export">
  <img src="https://img.shields.io/badge/license-MIT-blue" alt="License">
</p>

A **web scraper and data parser for apartment listings**. Extracts price, size, location, and amenity data from listing pages, normalizes it, and exports to CSV/JSON for analysis.

---

## 🏗️ Pipeline

```mermaid
flowchart LR
    URL["🌐 Listing URLs"] --> Scraper["🕷️ Requests +\nBeautifulSoup"]
    Scraper --> Raw["📄 Raw HTML\n(price, size, address)"]
    Raw --> Parser["🔧 Parser\n(extract + normalize)"]
    Parser --> DataFrame["🐼 Pandas\nDataFrame"]
    DataFrame --> CSV["📊 CSV Export"]
    DataFrame --> JSON["📋 JSON Export"]
    DataFrame --> Analysis["📈 Price Analysis\n(by location/size)"]
```

---

## 🚀 Quick Start

```bash
pip install -r requirements.txt
python scraper.py --url "https://..." --pages 5 --output ./data
```

---

## ⚙️ Output Schema

```json
{
  "title": "2BR Modern Apartment",
  "price": 1850,
  "currency": "USD",
  "size_sqft": 750,
  "bedrooms": 2,
  "bathrooms": 1,
  "address": "Brooklyn, NY",
  "amenities": ["gym", "laundry", "pets_ok"],
  "url": "https://...",
  "scraped_at": "2024-01-15T10:30:00Z"
}
```

---

## 📊 Analysis Features

- Price per square foot by neighborhood
- Price distribution histograms
- Amenity frequency analysis
- Correlation: size vs price

---

## 📄 License

MIT
