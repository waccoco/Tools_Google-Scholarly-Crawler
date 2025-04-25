# Tools_Google-Scholarly-Crawler
# 📚 Google Scholarly Crawler

This project is a Python-based tool for retrieving academic publication data from **Google Scholar**. It allows users to search by keyword and save the results into a **SQLite database**, **Excel (.xlsx)**, or **CSV** file. Ideal for literature reviews, academic research management, and research trend analysis.

---

## 🚀 Features

- Search academic papers using the [`scholarly`](https://github.com/scholarly-python-package/scholarly) package.
- Store results in:
  - SQLite database
  - Excel (.xlsx) file with active hyperlinks
  - CSV file
- Customizable search options:
  - Limit number of results
  - Filter by publication year range
  - Sort by relevance or date

---

## 🧰 Installation

```bash
pip install scholarly pandas openpyxl

---

##📂 File Overview
Goolge_scholarly_crawler.ipynb: Main Jupyter Notebook containing all functionalities:

-Scholar search
-Data parsing
-Data storage in multiple formats

---

##📝 How to Use
 -  Create a database (optional):
conn = create_database("scholar_data.db")

 - Search publications by keyword:
search_scholar(
    keyword="machine learning in materials science",
    limit=20,
    conn=conn,
    year_low=2018,
    year_high=2024,
    sort_by="relevance"  # or "date"
)

 - Export search results:
save_to_excel(results, "results.xlsx")
save_to_csv(results, "results.csv")


## ⚠️ Notes
 - Google Scholar may block your IP for sending too many requests. It is strongly recommended to add random delays or use proxy services.
 - Proxy configuration examples are included but commented out. For large-scale scraping, use a paid proxy or API service if needed.

## 📄 License
This project is licensed under the MIT License.


