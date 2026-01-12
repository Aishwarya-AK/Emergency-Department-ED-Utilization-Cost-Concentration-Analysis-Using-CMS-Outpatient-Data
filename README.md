🏥 Emergency Department Utilization & Cost Concentration Analysis
========
📌 Project Overview



Emergency Department (ED) services represent one of the most expensive and highly utilized components of outpatient care. This project analyzes **Emergency Department utilization and cost concentration across U.S. hospitals** using publicly available **CMS Medicare Outpatient Hospital data.**

The analysis focuses on:

- ED service volume

- Estimated ED allowed spending

- Cost concentration among hospitals

- Ownership-level and geographic distribution of ED costs

This project is designed to mirror real-world payer and healthcare analytics workflows, using aggregated claims-style data and business-ready KPIs commonly used in executive reporting and cost analysis.



📊 Data Sources
========

- CMS Medicare Outpatient Hospitals – by Provider and Service (2023)

- CMS Medicare Outpatient Hospitals – by Geography and Service (2023)

- CMS Hospital General Information

**Note:** CMS data is aggregated (hospital- and geography-level only). All cost figures are estimated using CMS-provided averages and service counts.


🛠️ Tools & Technologies
========

-  Power BI Desktop 

-  Power Query (ETL & data modeling)

- DAX (measures and KPIs)

- CMS APC (Ambulatory Payment Classification) mapping

🧠 Methodology
========
**ED Identification**

CMS outpatient data does not explicitly flag Emergency Department services.
To address this, a reusable APC reference table was created:

- APC descriptions were reviewed

- ED-related APCs were manually tagged (ED_Flag = 1)

- This mapping was joined back to provider- and geography-level datasets

This approach ensures consistent, transparent, and defensible ED classification across all analyses.

Cost Estimation Logic
========
Because CMS provides average allowed amounts and service counts, total ED spend was estimated as:

**Estimated ED Allowed Spend = Avg Medicare Allowed Amount × Number of Services**


A weighted average methodology was used for cost KPIs to properly account for service volume and avoid distortion from low-volume services.

📈 Key Metrics
========
- ED Services (utilization proxy)

- ED Beneficiaries

- Estimated ED Allowed Spend

- Weighted Average ED Allowed Amount

- ED Spend Share by Hospital Ownership

- Geographic ED Spend Distribution

📊 Dashboard Pages
========
**1. ED Overview**

- Total ED services

- Total estimated ED allowed spend

- Total ED beneficiaries

- Hospital-level ED service distribution

**2. Cost & Concentration**

- Top 10 hospitals by estimated ED allowed spend

- Weighted average ED allowed amount

- ED spend share by hospital ownership

**3. Geographic Benchmark**

- State-level ED allowed spend comparison

- Geographic variation in ED cost burden

🔍 Key Insights
========
- A small number of large tertiary hospitals account for a disproportionate share of ED spending

- Non-profit hospital systems dominate ED costs, representing the majority of national ED allowed spend

- The weighted average allowed amount per ED service is approximately $4.9K, reflecting higher acuity and service intensity

- ED spending varies significantly by geography, highlighting regional cost concentration

⚠️ Limitations
========
- Data is aggregated (hospital- and geography-level only)

- No patient-level visit dates or clinical outcomes

- ED costs are estimated using CMS averages, not claim-level totals

🎯 Use Cases
========
- Healthcare cost containment analysis

- Payer and provider benchmarking

- Executive reporting and strategy discussions

