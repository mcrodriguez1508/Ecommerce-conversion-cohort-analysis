# E-commerce Conversion Funnel & Cohort Retention Analysis
An end-to-end data analysis project focused on optimizing an e-commerce conversion funnel, tracking weekly user cohort retention, and statistically validating a checkout User Interface (UI) experiment using an A/B testing framework.

## 📊 Project overview
This project addresses real-world business challenges by identifying user drop-off points, measuring long-term user engagement, and using data-driven decisions to boost successful purchases.

Key components include:
1. **Funnel analysis:** Cleaning and re-structuring data to build a strictly descending conversion funnel.
2. **Cohort analysis:** Tracking user behavior week-over-week to evaluate retention dynamics.
3. **A/B Testing:** Statistical evaluation of a new checkout UI variant using a two-sided Z-test for proportions.
4. **Executive dashboard:** An interactive Power BI report visualizing core business KPIs (ROI, CAC, Conversion, and Orders).

## 🛠️ Tech stack & libraries
- **Database connection & eExtraction:** SQL (PostgreSQL), `SQLAlchemy`
- **Data manipulation:** Python, `Pandas`, `NumPy`
- **Statistical analysis:** `Statsmodels` (Z-test)
- **Data visualization:** `Matplotlib`, `Seaborn`
- **Business intelligence:** Power BI Desktop

## 📈 Key Findings & Insights

### 1. Conversion funnel optimization
* **Baseline:** The initial analysis revealed raw event inconsistencies. After applying proper sequentially-dependent logical filtering, a realistic descending funnel was established.
* **The Bottom-Line:** The final conversion rate from the first visit to a completed purchase stands at **49.47%**.
* **The Friction Point:** A critical leakage was identified at the very end of the funnel. Out of all users who successfully input their billing information (`add_payment_info`), **22.35%** abandon the platform before hitting the final purchase confirmation button. 
* **Device Consistency:** Drop-off behavior is almost identical on Desktop (**50.15%** conversion) and Mobile (**48.78%** conversion), ruling out isolated mobile-app responsive layout bugs and pointing towards a general checkout checkout-gate issue or lack of local payment options.

### 2. Cohort retention (Heatmap analysis)
* Using a user activity breakdown, a weekly retention grid was visualized via a Seaborn Heatmap. 
* The data exhibits a progressive decline by Week 3 across all monthly sign-up cohorts, revealing a common digital commerce challenge: maintaining early-stage user engagement after the first 14 days post-registration.

### 3. A/B Testing Evaluation
* A statistical proportion evaluation (Z-Test) was carried out on `experiment_checkout_ui.csv` comparing the Control vs. Treatment layout versions.
* By assessing the resulting `P-value` against a significance level of $\alpha = 0.05$, the final report determines whether the interface upgrade provides an implementation-worthy, statistically significant lift or if observed variances are due to random distribution.

## 📂 Repository Structure
```text
├── S12 Estudiante_Proyecto_Final_Correcciones MCRC.ipynb  # Main Jupyter Notebook with code & visualizations
├── Proyecto12_MARIACAMILA_RODRIGUEZCRUZ.pbix              # Interactive Power BI Dashboard
├── orders_clean.csv                                       # Cleaned dataset exported for BI tools
├── catalog_clean.csv                                      # Product catalog dataset
├── marketing_clean.csv                                    # Marketing campaign performance dataset
└── README.md                                              # Project documentation
