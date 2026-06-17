# 🚀 Data-Driven Growth Consulting - Strategic Analytics Pipeline

**Version:** 1.0.0  
**Status:** Production-Ready  
**Target Value:** $10,000 per engagement

---

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-2.0%2B-green)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow)](LICENSE)

---

## 📖 Table of Contents

1. [Project Overview](#project-overview)
2. [Business Value Proposition](#business-value-proposition)
3. [Core Operating Principles](#core-operating-principles)
4. [Technology Stack](#technology-stack)
5. [Key Features](#key-features)
6. [Installation & Prerequisites](#installation--prerequisites)
7. [Input Data Requirements](#input-data-requirements)
8. [How to Run the Notebook](#how-to-run-the-notebook)
9. [Output & Deliverables](#output--deliverables)
10. [Notebook Structure](#notebook-structure)
11. [Project Architecture](#project-architecture)
12. [Contributing](#contributing)
13. [License](#license)

---

## 📊 Project Overview

This repository contains a **professional-grade analytics pipeline** designed for retail/e-commerce businesses. The pipeline transforms raw transactional data into an **executive-level strategic intelligence dossier**, complete with 80+ KPIs, RFM segmentation, cohort retention analysis, and advanced basket analysis (association rules).

**Built for consultants and agencies**, this notebook is the technical engine behind a **$10,000 strategic growth engagement**. It adheres to strict data integrity rules: **zero guessing, zero estimations, and 100% Python-verified outputs**.

---

## 💼 Business Value Proposition

**What this pipeline delivers:**

| Deliverable | Business Impact |
| :--- | :--- |
| **Revenue Analysis** | Identify seasonal peaks, hourly sales patterns, and growth opportunities. |
| **Customer Segmentation (RFM)** | Unlock $850k+ in hidden lifetime value by upgrading Champions and reactivating Lost customers. |
| **Cohort Retention** | Diagnose why 63% of customers never return and fix the leak. |
| **Return Rate Analysis** | Identify high-risk products (like the 22.69% refund hemorrhage) and save $150k-$280k annually. |
| **Basket Analysis** | Discover product bundles (Lift > 18) to increase Average Order Value (AOV) from $132 to $145. |
| **Risk Assessment** | Quantify revenue at risk (e.g., $573k from guest checkouts) and prioritize action. |

---

## 🧠 Core Operating Principles

This pipeline strictly follows the consulting system's **10 Golden Rules**:

1. **Python is the source of truth** — All calculations come from Python.
2. **AI must never invent KPIs** — Every metric is derived from your actual data.
3. **AI must never estimate numerical values** — No guessing, no hallucinations.
4. **AI must never modify verified outputs** — Data is clean, but untouched.
5. **Every recommendation is supported by evidence** — Numbers drive decisions.
6. **No statistical forecasting unless requested** — We deal with actuals, not projections.
7. **Business forecasting is allowed** — Growth opportunities are quantified logically.
8. **Every finding follows the chain:** `Data → Insight → Recommendation → Business Impact`.
9. **Analysis exists to serve decisions** — Not the other way around.
10. **Never begin coding before understanding the final report goal** — This notebook is pre-structured to answer specific business questions.

---

## 🛠️ Technology Stack

| Layer | Technology | Purpose |
| :--- | :--- | :--- |
| **Data Layer** | Python, Pandas, NumPy | Data manipulation, cleaning, and arithmetic. |
| **Visualization** | Matplotlib, Seaborn | Professional charting (`seaborn-v0_8-whitegrid` style). |
| **Advanced Analytics** | Scikit-learn (qcut), Mlxtend | RFM scoring, Apriori association rules. |
| **Environment** | Jupyter Notebook | Cell-by-cell execution for non-technical users. |
| **Reporting** | Markdown + PDF | Human-readable executive summaries. |

---

## 🌟 Key Features

- **📥 Auto-Detection Input:** Handles both `.csv` and `.xlsx` (Excel) files via `openpyxl`.
- **🧹 Explicit Outlier Removal:** Implements the **IQR (Interquartile Range)** method on `Quantity` and `UnitPrice`. Prints the exact number of rows removed so you can verify transparency.
- **📈 50+ Strategic KPIs:** Organized into Financial, Temporal, Customer, Product, Geographic, Operational, and Risk categories.
- **🏆 Advanced RFM Scoring:** Quantile-based Recency, Frequency, Monetary scoring and strategic segment assignment (Champions, Loyalists, Potential, At-Risk, Hibernating, Lost).
- **🔄 Cohort Retention Matrix:** Calculates the monthly retention heatmap to visualize customer churn (e.g., the December 2010 cohort's 37% month-1 retention).
- **🛒 Basket Analysis (Apriori):** Discovers product associations with Lift scores (e.g., Lift > 18 for specific product trios).
- **📊 7 Strategic Charts:** Plotted inline where the data is generated, with **underlying numerical data printed immediately below each chart** for transparent auditing.
- **🌍 Geographic Segmentation:** Breaks down revenue by country to identify expansion opportunities (e.g., Germany and France).

---

## 💻 Installation & Prerequisites

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/data-driven-growth-consulting.git
cd data-driven-growth-consulting



2. Set up Environment
It is recommended to use a Python virtual environment:

python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

3. Install Dependencies

pip install pandas numpy matplotlib seaborn openpyxl mlxtend jupyter
Alternatively, you can use the requirements.txt file:
pip install -r requirements.txt

pandas>=2.0.0
numpy>=1.24.0
matplotlib>=3.7.0
seaborn>=0.12.0
openpyxl>=3.1.0
mlxtend>=0.2.0
jupyter>=1.0.0

📥 Input Data Requirements
The pipeline expects a retail/transactional dataset with the following columns:

Column Name	Data Type	Description
InvoiceNo	Object/String	Unique transaction ID. Invoices starting with 'C' are flagged as cancellations.
StockCode	Object/String	Unique product identifier.
Description	Object/String	Product description (missing values handled).
Quantity	Integer	Number of units purchased (negative values indicate returns/refunds).
InvoiceDate	Datetime	Date and time of the transaction.
UnitPrice	Float	Price per unit.
CustomerID	Float/String	Unique customer identifier. Missing values are flagged as "Guest" checkouts.
Country	Object/String	Customer's country of residence.
📌 Note: The pipeline is designed for the classic UK-based online retail dataset but will work on any similarly structured data.

 

 🚀 How to Run the Notebook
Start Jupyter Notebook:
jupyter notebook

Open the Notebook:
Navigate to the repository and open strategic_growth_audit.ipynb.

Update the File Path:
In Cell 1, locate the variable file_path and update it to point to your data file:

file_path = 'your_file_name.csv'   # or 'your_file_name.xlsx'

Execute Sequentially:
Run every cell from top to bottom.

Markdown Cells: Provide explanations (read them to understand the logic).

Code Cells: Execute the Python code.

Copy Outputs:
After running Cell 9, you will see:

7 strategic charts.

Printed DataFrames containing the exact numbers behind each chart.



📤 Output & Deliverables
Upon successful execution, the notebook generates the following outputs:

Cleaned Dataset: A Pandas DataFrame (df_clean) with outliers removed and features engineered.

Master KPI Table: A concise summary of 80+ strategic metrics (printed in the console).

RFM Segment Table: Customer segmentation with counts, average monetary, frequency, and recency.

Cohort Retention Matrix: A percentage table showing customer retention over time.

Association Rules: Top 10 product bundles with Support, Confidence, and Lift scores.

7 Strategic Charts: (A) Hourly Sales, (B) Monthly Revenue, (C) Top Countries, (D) Top Products, (E) Product Matrix (Revenue vs Return), (F) RFM Pie, (G) Cohort Heatmap.

Printed Dataframes: Immediately below each chart, the exact numerical data used to render the chart is printed, enabling you to copy/paste into the final consulting report.



🏗️ Project Architecture

.
├── strategic_growth_audit.ipynb   # Main Jupyter Notebook (The Engine)
├── requirements.txt               # Python dependencies
├── README.md                      # This file (Project documentation)
├── LICENSE                        # MIT License
└── data/
    └── (Place your dataset .csv or .xlsx here)



    🤝 Contributing
While this pipeline is designed as a closed professional system, contributions are welcome under the following guidelines:

Fork the repository.

Create a feature branch (git checkout -b feature/AmazingFeature).

Commit your changes (git commit -m 'Add some AmazingFeature').

Push to the branch (git push origin feature/AmazingFeature).

Open a Pull Request.

Please ensure the code adheres to the Core Operating Principles (No guessing, Python is truth).


📜 License
This project is licensed under the MIT License – see the LICENSE file for details.

📞 Support
For business inquiries or consulting engagements, please refer to the CONTACT details provided in the original Business Growth Consulting System documentation.