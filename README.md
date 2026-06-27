# 📊 Customer Segmentation, Visualization & Advanced Analysis

Developed during a **Business Analyst Internship at Saiket Systems**, this project applies unsupervised machine learning and interactive Power BI dashboards to help telecommunications companies identify customer segments and predict churn, enabling smarter retention strategies.

## 🎯 About the Project

This toolkit was built to give businesses clear, actionable insights into their customer base. Using clustering algorithms on real telecom data, it automatically groups customers by behavior and flags those most likely to leave — all visualized through interactive dashboards that anyone on the team can use.

## ✨ Features

- **Customer Segmentation** — Automatically groups customers into distinct segments based on behaviors and preferences using K-Means and DBSCAN clustering
- **Churn Analysis** — Identifies at-risk customers likely to leave and provides actionable insights to support retention strategies
- **Interactive Power BI Dashboards** — Dynamic, clickable charts and graphs for real-time exploration of customer trends and key metrics
- **Data Export Options** — Export data and visualizations into multiple formats for business reporting and decision-making

## 🏗️ Architecture & Workflow

```
Raw Data (Telco_Customer_Churn_Dataset.csv)
        │
        ▼
  [1] Data Preprocessing
        │   Clean missing values, encode categorical variables,
        │   normalize numerical features
        ▼
  [2] Exploratory Data Analysis (EDA)
        │   Understand distributions, correlations,
        │   and patterns in customer data
        ▼
  [3] Customer Segmentation (ML)
        │   K-Means   → finds well-defined, compact clusters
        │   DBSCAN    → handles irregular shapes & outliers
        ▼
  [4] Churn Analysis
        │   Flag at-risk customers within each segment,
        │   rank by churn probability
        ▼
  [5] Power BI Visualization
        │   Load results into interactive dashboards,
        │   drill-down charts, and exportable reports
        ▼
  [6] Business Insights & Export
        │   Retention recommendations per segment,
        │   export reports in PDF / Excel formats
```

## 📥 Input & Output

### Input
| Source | Description |
|--------|-------------|
| `Telco_Customer_Churn_Dataset.csv` | Core dataset containing customer records from a telecom company |

The dataset includes customer attributes such as:
- **Demographics** — gender, age range, partner/dependent status
- **Account Information** — tenure, contract type, payment method, monthly charges, total charges
- **Services Subscribed** — phone, internet, streaming, tech support, online security
- **Churn Label** — whether the customer has left the company (`Yes` / `No`)

### Output
| Output | Format | Description |
|--------|--------|-------------|
| Customer Segments | Dashboard / Export | Distinct groups of customers labeled by behavior profile |
| Churn Risk Flags | Dashboard / Export | List of at-risk customers ranked by likelihood to churn |
| Power BI Dashboard | `.pbix` / `.pdf` | Interactive visual report of all findings |
| Segment Insights | Export | Actionable retention recommendations per segment |


## 🤖 Machine Learning & Tech Stack

| Component | Technology |
|-----------|------------|
| Analysis & Modeling | Jupyter Notebook (100% of codebase) |
| Segmentation Algorithms | K-Means Clustering, DBSCAN |
| Visualization | Power BI |
| Dataset | `Telco_Customer_Churn_Dataset.csv` |

### Why K-Means & DBSCAN?

Both are **unsupervised learning** algorithms — meaning they find natural groupings in customer data without needing pre-labeled examples.

- **K-Means** is efficient for finding well-defined, evenly sized clusters. It works by assigning each customer to the nearest cluster center and iteratively refining those centers until the groupings stabilize.
- **DBSCAN** (Density-Based Spatial Clustering of Applications with Noise) handles irregular cluster shapes and automatically identifies outliers — customers who don't fit neatly into any group. This makes it ideal for catching edge-case churners.

Using both together gives a more complete and robust picture of the customer base than either algorithm alone.

## 📊 Power BI Dashboards & Visualizations

The Power BI dashboard (`Customer_Segmentation_Churn_Dashboard.pbix`) is the primary way to explore project results. A static PDF version is also included for quick reference.

### What the Dashboard Shows

| Visual | What It Tells You |
|--------|------------------|
| **Churn Rate Overview** | Overall percentage of customers who have churned vs. retained |
| **Segment Distribution** | How customers are spread across the identified segments |
| **Churn by Segment** | Which customer groups have the highest churn rates |
| **Churn by Contract Type** | Whether month-to-month vs. long-term contracts affect churn |
| **Churn by Services** | How subscribed services (e.g., tech support, streaming) relate to churn |
| **Monthly Charges vs. Churn** | Whether pricing is a driver of customer loss |
| **Tenure Analysis** | How long customers stay before churning |
| **At-Risk Customer List** | Filterable table of flagged customers for targeted action |


## 📁 Repository Structure

```
├── Customer Segmentation Analysis.ipynb        # Main analysis notebook
├── Customer_Segmentation_Churn_Dashboard.pbix  # Interactive Power BI dashboard
├── Customer_Segmentation_Churn_Dashboard.pdf   # Static PDF version of the dashboard
├── Telco_Customer_Churn_Dataset.csv            # Dataset used for analysis
├── requirements.txt                            # Python dependencies
├── images/                                     # Project screenshots and visuals
└── README.md
```
