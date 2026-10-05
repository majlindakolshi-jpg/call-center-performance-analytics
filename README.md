# Call Center Performance & Sales Analytics Dashboard

## Overview
This project delivers a comprehensive, two-page interactive **Power BI** report designed to analyze call center operations, agent performance, customer satisfaction (CSAT), and sales conversion trends. The dataset was extracted, cleaned, and transformed directly from complex Excel source files using Power Query and modeled for deep analytical insights.

---

## Key Features & Multi-Page Dashboard Structure

### 1. Operational Performance & Quality Dashboard (Page 1)
- **Call Volume Trends:** Analysis of total calls received, answered vs. abandoned call rates, and peak hours.
- **Service Level & Efficiency:** Monitoring Average Speed of Answer (ASA), Average Handling Time (AHT), and SLA compliance rates.
- **Customer Satisfaction (CSAT):** Tracking CSAT scores across different agent groups and call categories.

### 2. Sales Analytics & Agent Performance Dashboard (Page 2)
- **Conversion & Revenue:** Analyzing call-to-sales conversion rates and total generated revenue.
- **Agent Leaderboard:** In-depth breakdown of top-performing agents based on sales target achievement and resolution quality.
- **Category Insights:** Performance segmentation by product line, customer demographics, and call reasons.

---

## Key Insights & Business Recommendations
- **Peak Hour Optimization:** Identified specific time windows with high call abandonment rates, leading to operational recommendations for shift rescheduling.
- **Conversion Drivers:** Higher CSAT scores directly correlated with longer handle times during initial customer onboarding calls.
- **Training Opportunities:** Pinpointed performance gaps among specific agent cohorts to target SLA and AHT improvement training.

---

## Tools & Technologies Used
- **Power BI Desktop:** Power Query (ETL), Star Schema Data Modeling, DAX Measures, Multi-page UI/UX Layout.
- **Microsoft Excel:** Source datasets.

---

## Key DAX Measures
```dax
Total Calls = COUNT(Calls[CallID])

Answered Calls = CALCULATE([Total Calls], Calls[Status] = "Answered")

Abandonment Rate = DIVIDE(CALCULATE([Total Calls], Calls[Status] = "Abandoned"), [Total Calls], 0)

CSAT Score = AVERAGE(Calls[CSAT])

Total Revenue = SUM(Sales[RevenueAmount])
