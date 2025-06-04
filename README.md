
# 🚀 **Project Title: Kuda Full-Funnel Growth Analytics/Intelligence System (KUDA Simulation)**

## 🎯 **Project Objective:**

This project simulates a real-world data analyst role at **Kuda**, a digital-only bank, by building a **full-funnel analytics pipeline**. The system tracks the **entire user journey from marketing to retention, integrates data ingestion, transformation, analysis, and dashboarding ** , calculates key business metrics (e.g., **Churn, CAC, LTV, MoM/YoY Growth**), and simulates **A/B testing** for product/CRM strategies to support the Growth, CRM, and Product teams.

The end goal is to provide a **dashboard and reporting suite** that empowers executive teams to make data-driven decisions—**all while showcasing the real challenges fintechs face in aligning growth with product performance**.

---

## 🎯 Business Goals & Stakeholder Questions

### 👥 **Assumed Stakeholders**

* **Growth Marketing Team** — focused on user acquisition & CAC
* **Product Managers** — tracking activation & retention funnels
* **CRM Team** — driving re-engagement via emails & push
* **Executives (CEO/COO/CFO)** — care about ROI, LTV, and growth

---

### 🧠 **Core Business Objectives & Analytical Questions**

#### 📌 **Retention & Churn**

* What percentage of users return on **Day 1**, **Day 7**, and **Day 30**?
* Where are users **dropping off** in the onboarding funnel?
* What are our **monthly** and **quarterly churn rates**?

#### 📌 **Customer Acquisition Cost vs Lifetime Value (CAC vs LTV)**

* What’s the **CAC per campaign/platform**?
* What’s the **average LTV** by UTM source, signup cohort, or platform?
* Are we **overpaying** to acquire **low-LTV users**?

#### 📌 **Funnel Conversion Rates**

* What percentage of users move from:

  * **Signup → Activation?**
  * **Activation → First Transaction?**
  * **First Transaction → Retention?**

#### 📌 **CRM Campaign ROI**

* What’s the **retention uplift** from email/push campaigns?
* Does **A/B testing** show a statistically significant impact?
* What’s the **ROI** on our CRM automation tools?

#### 📌 **Growth Metrics**

* What’s our **Month-on-Month (MoM)** and **Year-on-Year (YoY)** user growth?
* How are **campaign spend and signups trending** over time?


---

## 🛠️ **Project Stack:**

| **Layer**           | **Tools/Libraries**                                                                 |
| ------------------- | ----------------------------------------------------------------------------------- |
| **Data Simulation** | `Python`, `Faker`, `Numpy`, `Pandas`                                                |
| **Storage**         | `PostgreSQL` / `SQLite`, **Snowflake** *(mocked)*, **Google Sheets** *(CSV sync)*   |
| **CRM + Events**    | Simulated `HubSpot`, `Segment`, `Amplitude` or `Mixpanel` *(CSV or API simulation)* |
| **Analysis**        | `Pandas`, `SQL`, `Scipy`, `Statsmodels`, `Matplotlib`, `Seaborn`, `Plotly`          |
| **Dashboards**      | `Power BI`, `Tableau`, `Dash`, *(+ Streamlit for web dashboards — bonus)*           |
| **Orchestration**   | `Airflow`, `Prefect` *(bonus)*                                                      |
| **Reporting**       | `Jupyter Notebooks`, `Markdown`, `PDF summaries`                                    |


---

## 🔄 **Project Architecture Flow:**

```
Marketing Sources → CRM (HubSpot) → App Events (Amplitude) 
→ SQL Database (Snowflake/PostgreSQL) → Retention & Metrics Analysis (Python, SQL) 
→ A/B Testing → Dashboard Visualization (Tableau/Power BI)
```

---

## 📁 **Project Structure**

```
📦 Kuda_Analytics_Project/
│
├── 📂 data/
│   ├── crm_data.csv
│   ├── event_logs.csv
│   ├── campaign_spend.csv
│   └── transactions.csv
│
├── 📂 notebooks/
│   ├── 01_data_simulation.ipynb
│   ├── 02_metrics_analysis.ipynb
│   ├── 03_ab_testing.ipynb
│   ├── 04_funnel_retention.ipynb
│   └── 05_dashboard_prep.ipynb
│
├── 📂 dashboards/
│   ├── powerbi_dashboard.pbix
│   └── tableau_dashboard.twb
│
├── 📂 reports/
│   └── Final_Report_Kuda_Analytics.pdf
│
└── README.md
```

---

## 🧠 Phase-by-Phase Breakdown

### **PHASE 1: Simulate and Prepare Data**

Use Python to simulate:

* **CRM Data (HubSpot style)**: user\_id, email, signup\_date, utm\_source, campaign
* **App Events (Amplitude style)**: event\_type, user\_id, timestamp
* **Transaction Records**: transaction\_id, user\_id, amount, date
* **Campaign Spend Data**: campaign\_id, platform, cost, impressions, signups

👉 Tools: `Faker`, `random`, `pandas`

---

### **PHASE 2: Load to SQL & Integrate**

* Load data into **Snowflake** (Kuda stack) or **PostgreSQL** (for simulation)
* Create SQL views and joins: users × events × transactions × campaigns
* Write SQL scripts to:

  * Track **signup → activation → retention**
  * Link **campaign → CRM user → LTV**

👉 Tools: `Snowflake Connector`, `SQLAlchemy`, `psycopg2`

---

### **PHASE 3: Business Metrics Calculation**

Using Pandas and SQL:

* Cohort-based **Retention Tables**
* **Churn rate**, **CAC**, **LTV**
* **MoM Growth**, **YoY Growth**
* **Campaign ROI**

👉 Tools: `pandas`, `numpy`, `matplotlib`, `seaborn`, SQL (Snowflake)

---

### **PHASE 4: Funnel + Retention Analysis**

* Define funnel stages: Visit → Signup → Activate → Retain
* Calculate:

  * Drop-off rates
  * Conversion rates
  * Retention curves

👉 Tools: Python + SQL → `Plotly`, `matplotlib`, `Snowflake` queries

---

### **PHASE 5: A/B Testing**

Simulate:

* Test group gets a retention email
* Control group doesn’t
* Analyze click-through, conversion, and retention over 7 days

👉 Tools: `scipy.stats`, `statsmodels`, `pandas`, SQL

---

### **PHASE 6: Visual Dashboards**

* Build executive-style dashboard with:

  * **Retention curves**
  * CAC vs LTV
  * MoM/YoY growth
  * Campaign ROI
  * Funnel conversion

👉 Tools: Power BI, Tableau, Snowflake connector

---

### **PHASE 7: Reporting & Documentation**

* Executive summary (PDF/Markdown)
* Dashboard walkthrough (screenshots and live link)
* SQL + Python codebase with comments
* Data dictionary + project walkthrough

👉 Tools: Markdown, Google Docs, Canva (for styling)

---

## 📈 Bonus: Advanced Touches (If You Want to Shine Extra Bright)

* Add **email open rates and push notifications** as new event types
* Integrate **Segment** or simulate similar data flows
* Use **Airflow or Prefect** to schedule data ingestion and transformation
* Build a lightweight dashboard with **Streamlit** or **Dash**
* Add an **anomaly detection script** for user drop-off or spend spikes

👉 Tools: Segment (mocked), Streamlit, Airflow, Prophet

---

## ✨ Project Deliverables

* 📊 A beautiful, insight-packed dashboard (Power BI or Tableau)
* 🧠 Jupyter notebooks showing clean, modular, reproducible analytics
* 💡 Insights written for stakeholders (PMs, CMOs, C-Suite)
* 🧪 A/B testing report with actionable recommendations
* 🔐 Compliance notes (GDPR/data minimization simulation)
* ⚙️ SQL views for each major metric pipeline
* 📄 Final PDF report and README for walkthrough


  
