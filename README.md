# Bank-Churn-Analysis
---

### Table of Content
 - [Executive Summary](#executive-summary)
  - [Business objective](#business-objective)
  - [Business questions](#business-questions)
  - [Data and Methodology](#data-and-methodology)
  - [Tool used](#tool-used)
  - [Dashboard Design](#dashboard-design)
  - [Key findings](#key-findings)
  - [Interpretation for the Bank](#interpretation-for-the-bank)
  - [Recommendations](#recommendations)
  - [Limitation](#limitation)
  - [Conclusion](#conclusion)
  - [Appendix](#appendix)
 

### Executive Summary:
---
This analysis examines customer churn in ABC Bank Nig.  using 10,000 customer records. It aims to identify customer groups associated with higher churn, compare the scale of departures across segments, and outline next steps for evidence-led retention planning. The recorded overall churn rate is 20.37%.
Inactive customers have a higher churn rate than active customers. Customers aged 50–59 have the highest age-group churn rate, while customers aged 40–49 account for the largest number of departures. A high rate and a high count answer different business questions. Findings are descriptive signals for investigation, not proof of why customers left.

### Business objective:
---
This project primary objective is to help the bank understand which customer segments warrant further churn investigation and support evidence-led retention planning.

### Business Questions:
---
The following business questions were analyzed.
- What proportion and number of customers are recorded as churned?
- How does churn vary by activity status, age, geography and number of products?
- How do recorded balances compare between churned and retained customers?
- Which balance groups have the highest churn rates, and which contribute the largest number of departures?
- What additional data would help investigate drivers and test retention actions?


### Data and Methodology:
---
The analysis uses customer records containing a churn indicator (Exited), recorded balance, activity status, age, geography, product count and credit-card status. It assumes one row per customer, with Exited = 1 meaning churned and Exited = 0 meaning retained. If the underlying model has multiple rows per customer, counts should instead use a distinct customer identifier.
- Churn rate = churned customers ÷ total customers in the current segment.
- Churned customer count = number of customers with Exited = 1.
- Average recorded balance = mean Balance within each churn-status group.
- Total recorded balance = sum of Balance within each churn-status group.
- Power BI visuals, slicers and tooltips support segment comparisons and contextual interpretation.
  
### Tool Used: 
---
  - Power BI (Pivot Query, DAX,visualization) 
  
### Dashboard Design
---
<img width="948" height="525" alt="Bank churn 1" src="https://github.com/user-attachments/assets/19f2e580-8386-4bcb-a737-ea59da2c5cd5" />

- Executive Overview: customer count, churned customers, churn rate and retention overview.
- Churn Drivers & Customer Behaviour: compare churn rates by age, activity, geography, product count and other available characteristics.
- Customer Risk & Segment Prioritisation: distinguish high-rate segments from high-volume segments.
- Customer Value & Churn Impact: compare total and average recorded balances by churn status; show positive-balance churn measures; compare churn count and rate by balance group.

### Key findings
---
- Overall churn: 2,037 of 10,000 customers were recorded as churned (20.37%).
- Activity status: Inactive customers had a 26.85% churn rate, compared with 14.27% among active customers.
- Geography: Ebonyi had the highest recorded churn rate at 32.44% (814/2,509). Enugu was 16.67% (413/2,477), and Anambra was 16.15% (810/5,014).
- Age: Customers aged 50–59 had the highest age-group churn rate of 56.04% (487/869). Customers aged 40–49 contributed the largest churn count of 806/2,618 (30.79%).
- Products held: Churn rates were 27.71% for one product (1,409/5,084), 7.58% for two products (348/4,590), 82.71% for three products (220/266), and 100% for four products (60/60). Small groups need cautious interpretation.
- Credit card: Churn rates were similar for customers without a credit card (20.81%; 613/2,945) and those with one (20.18%; 1,424/7,055).
- Recorded balances: Average recorded balance was ₦91,000 among churned customers and ₦73,000 among retained customers, a difference of ₦18,000 (about 24.7%). Total recorded balances were ₦185.059m and ₦579.027m respectively.
- Balance groups: The ₦200,001–₦250,900 group had the highest churn rate of 55.88% (19/34). The ₦1–₦50,000 group was 34.67% (26/75). The ₦100,001–₦150,000 group had the largest churn count: 987/3,830 (25.77%). The zero-balance group had the lowest rate: 13.82% (500/3,617).

### Interpretation for the Bank
---
- Use both churn rate and churned customer count when prioritising investigation. Segment churn rate identifies where churn is concentrated; churned customer count shows where the largest number of customers is affected. Combine these with customer value, intervention cost, feasibility and evidence about exit reasons.
- The ₦200,001–₦250,900 balance group has a 55.88% churn rate, based on 19 churned customers out of 34. It is a useful signal but a small group. The ₦100,001–₦150,000 group has 987 churned customers, making it important from a volume perspective.
- The average recorded balance among churned customers is higher than among retained customers. This does not establish that churned customers were more profitable or that their combined balance represents financial loss to the bank.

### Recommendations
---
- Use both rate and volume:
Investigate high-rate segments such as ages 50–59 and the ₦200,001–₦250,900 balance group, while also considering segments with larger churn counts, such as ages 40–49 and the ₦100,001–₦150,000 balance group.
- Investigate inactivity:
Compare transaction recency and frequency, product usage, digital engagement, service contacts and time since last meaningful activity for inactive versus active customers.
- Explore location differences:
Investigate the higher observed churn rate in Ebonyi alongside service coverage, customer mix, complaints and acquisition channels before choosing an intervention.
- Validate product patterns
Review the three- and four-product groups, validate group sizes and definitions, and check product timing before interpreting the high rates.
- Test retention actions
After identifying likely reasons, pilot targeted outreach or service improvements with a comparison group. Track retention, customer experience and intervention cost.
- Improve customer-value measurement
Add customer-level revenue, contribution margin and servicing cost where available. Account balance alone is not revenue, profit or money lost

### Limitation
- The analysis uses a 10,000-row dataset and the recorded churn flag; it does not identify a real bank or claim a commissioned engagement.
- No suitable date field was provided for establishing churn trends over time; no time-based increase or decrease is claimed.
- Associations between age, activity, geography, product count, balance and churn do not prove causation.
- Recorded account balance is not equivalent to revenue, profit, deposits lost, or financial loss caused by churn.
- Balance groups with small populations (34 customers in the highest balance group and 75 in the lowest positive-balance group) can produce volatile rates.
- Further data that could help: transaction recency/frequency, product usage, complaints, service interactions, exit reasons, account closure date, acquisition channel, customer revenue/margin and retention campaign history.

### Conclusion
---
The analysis provides a structured view of customer churn and identifies segments for further investigation. The current data cannot establish why customers leave. The next phase should validate the findings, enrich the dataset with behavioural and service information, and test targeted retention actions with measurable outcomes.

### Appendix
---
#### Balance-group results
|Balance group| Total customers| Churned customers| Churn rate|
|---|---|---|---|
|N200,001-N250,900| 34| 19| 55.88%|
|N1-N50,000| 75| 26| 34.67%|
|N100,001-N150,000| 3,830| 987| 25.77%|
|N150,001-N200,000| 935| 205| 21.93%|
|N50,001-N100,000| 1,509| 300| 19.88%|
|N0(zero balance)| 3,617| 500| 13.82%|

[Click here to view the Dashboard](https://app.powerbi.com/view?r=eyJrIjoiODQ5YjJlNWYtM2E3OS00Y2E0LWJmZjEtNmVjY2FiNmJhZGVjIiwidCI6ImNkYjdmNzc3LTc0ODUtNGQ0Mi1iY2U5LTdkMTc0YzVjMTkyOSIsImMiOjh9)
