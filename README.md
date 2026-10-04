# 🧼 Detergent Sales Growth & Commercial Analytics

A Power BI business intelligence project analysing sales performance, channel profitability, customer behaviour, product contribution, and regional performance for a global detergent business.

The project turns transaction-level data into an executive dashboard and commercial growth recommendations, while also identifying data-quality limitations and opportunities for improving future analytics.

---

## 🎯 Goal

To identify the key drivers of detergent sales growth and profitability and translate them into actionable commercial strategies across sales channels, customers, products, and regions.

### Sub-Questions Explored:

- How is revenue trending over time and across sales channels?
- Which sales channels generate the strongest profit and margins?
- Which products contribute the most to overall profitability?
- Where are the strongest customer retention and reactivation opportunities?
- Which geographic markets contribute the most revenue?
- What data-quality issues could affect management decisions?
- What additional data should the business collect to improve future commercial analysis?

---

## 📂 Files Included

| **File** | **Description** |
| --- | --- |
| `Detergent_PowerBI_Dashboard.pbix` | Interactive Power BI dashboard for sales, customer, product and channel analysis |
| `Detergent_PowerBI_Business_Presentation.pdf` | Executive presentation covering insights, recommendations and data roadmap |
| `transaction data.xlsx` | Original transaction, customer, country and product data |
| `PowerBI_Data_Source.xlsx` | Prepared data source, metric definitions and QA checks used for Power BI |

---

## 🧪 Methodology

### 🔹 Data Preparation

The analysis combines four core datasets:

- **Transaction data** — transaction ID, customer, date, product and units sold
- **Customer Master** — customer details, sales channel and country
- **Country Master** — mapping countries into geographic regions
- **Product Ledger** — product names, standard cost and standard selling price

The datasets were connected through customer, product and geography keys to create a consolidated analytical model.

### 🔹 Key Metrics

The main commercial metrics were defined as:

- **Revenue** = Units Sold × Standard Price
- **Gross Profit** = Revenue − (Units Sold × Standard Cost)
- **Channel Profit** = Gross Profit − Variable Channel Cost − Allocated Fixed Channel Cost
- **Active Customers** = Customers with purchases during the analysed period
- **YoY Growth** = Jan–Sep 2012 compared with Jan–Sep 2011

> Channel profit represents contribution after the case-specific channel costs and should not be interpreted as full operating profit.

---

## 📊 Power BI Dashboard

![Detergent Sales Power BI Dashboard](images/dashboard-overview.png)

The dashboard provides management with one interactive view of commercial performance across **sales channels, regions and product families**.

### Dashboard KPIs

- **$7.71M** Total Revenue
- **$2.58M** Channel Profit
- **6,707** Orders
- **885** Active Customers

Users can filter the dashboard by:

- Sales Channel
- Region
- Product Family

---

## 📈 Exploratory Analysis & Key Findings

### 🔸 Strong Revenue Growth

Revenue reached **$7.71M**, with Jan–Sep revenue increasing **256% compared with the equivalent period in the previous year**.

The monthly trend also shows substantial growth across Direct, Online and Retail channels as the business scaled.

> The business has demonstrated strong growth; the next challenge is determining where additional investment can generate profitable rather than purely top-line growth.

---

### 🔸 Channel Profitability

Channel profit totalled **$2.58M**.

| Channel | Channel Profit |
| --- | ---: |
| Direct | $1.07M |
| Online | $0.88M |
| Retail | $0.63M |

Direct generated the largest absolute contribution, while **Online achieved a 42.3% margin**, making it particularly attractive as a scalable acquisition channel.

### 💡 Insight

Revenue alone should not determine channel investment.

Online presents an opportunity to scale acquisition, while Direct should be protected for high-value customer relationships and Retail managed with stronger promotion and margin guardrails.

---

### 🔸 Customer Value & Reactivation Opportunity

The analysis identified **232 customers who had been inactive for more than 90 days**.

These customers had previously generated approximately **$1.17M in revenue**.

A scenario analysis estimated that reactivating **10% of this segment could generate approximately $65K within 90 days**.

> Existing customers therefore represent a meaningful growth opportunity alongside new customer acquisition.

---

### 🔸 Product Profitability

Profit contribution is concentrated among a relatively small number of products.

Two hero SKUs account for approximately **32% of product profit**:

- **Pure Soft Detergent – 500ml**
- **Super Soft – 1 Litre**

Pure Soft Detergent – 500ml generated approximately **$440K** in channel profit, making it the strongest individual product in the portfolio.

### 💡 Insight

The business should prioritise high-contribution hero SKUs while investigating products with weaker economics.

In particular, the analysis highlighted **Detafast 800ml** as an area where pricing and cost-to-serve should be reviewed.

---

### 🔸 Product Sampling

Product sampling showed potentially encouraging behaviour:

- Samples cost approximately **$72.8K**
- **75% of sampled customers purchased within 90 days**

However, the relationship cannot yet be interpreted as causal.

> A control or holdout group should be introduced before increasing sampling investment to determine whether sampling actually creates incremental purchases.

---

## ⚠️ Data Quality Investigation

One of the most important findings was a geography mapping issue.

**352 of 998 customer-master records** contain countries that do not match the supplied Country Master.

Transactions associated with these customers represent:

- **$3.06M revenue**
- **39.7% of total revenue**

Rather than removing these observations, the Power BI dashboard retains them as **"Unmapped"**.

### 💡 Why This Matters

Silently excluding unmatched records would materially distort regional performance.

The country master should therefore be corrected before regional results are used for market target-setting or investment allocation.

---

## 💡 Strategic Recommendations

### 🎯 1. Scale Online Acquisition

**Objective:** Grow customer acquisition without sacrificing profitability.

- Scale Online within a contribution-based CAC ceiling
- Measure acquisition against contribution rather than revenue alone
- Introduce CAC and ROAS monitoring as marketing data becomes available

Online's **42.3% margin** suggests room for controlled growth.

---

### 🤝 2. Protect High-Value Direct Customers

**Objective:** Maximise value from the company's strongest customer relationships.

Direct generates approximately **$4.4K profit per customer**.

Actions could include:

- Deeper account management
- Retention initiatives
- Cross-sell opportunities
- Customer-level profitability monitoring

---

### 🔁 3. Reactivate Lapsed Customers

**Objective:** Recover value from previously active customers.

Create segmented win-back campaigns targeting the **232 customers inactive for more than 90 days**.

Potential tactics include:

- Customer-value-based segmentation
- Personalised reactivation offers
- Product recommendations based on previous purchases
- Triggered CRM campaigns

A 10% reactivation scenario represents approximately **$65K in potential 90-day revenue**.

---

### 📦 4. Prioritise Hero SKUs

**Objective:** Concentrate commercial investment around products with strong contribution.

Prioritise:

- Pure Soft Detergent – 500ml
- Super Soft – 1 Litre

Together they generate approximately **32% of product profit**.

At the same time, investigate lower-performing products for:

- Pricing
- Standard cost
- Cost-to-serve
- Promotion effectiveness

---

### 🧪 5. Test Sampling Incrementality

**Objective:** Determine whether product sampling genuinely drives additional sales.

Instead of scaling the programme based only on observed conversion:

1. Establish test and control groups
2. Compare purchase rates after sampling
3. Measure incremental revenue and profit
4. Calculate sampling ROI

This would move the analysis from correlation toward causal measurement.

---

## 🗺️ Recommended Data Roadmap

The current dataset supports commercial performance analysis, but additional data would enable much stronger decision-making.

### Data to Collect

**Retail sell-out & inventory**
- Consumer demand
- Stock availability
- Sell-through
- Lost-sales risk

**Prices, promotions & discounts**
- Price elasticity
- Promotion effectiveness
- Incremental ROI

**Customer identity & purchase history**
- Customer lifetime value
- Repeat purchase
- Churn
- Win-back targeting

**Marketing exposure & digital behaviour**
- Attribution
- Conversion
- CAC
- Customer journey analysis

**Samples, costs & master data**
- Sampling lift
- Cost-to-serve
- SKU profitability
- Reliable geographic reporting

---

## 🚀 90-Day Analytics Roadmap

### Days 0–30
- Fix country and channel master data
- Standardise metric definitions
- Add campaign, sample and order identifiers

### Days 31–60
- Integrate net sales, returns and fulfilment data
- Add inventory and retail sell-out
- Introduce automated data-quality monitoring

### Days 61–90
- Launch CAC / ROAS reporting
- Build lapsed-customer cohorts
- Introduce sampling holdout tests
- Develop margin experiments

---

## 📊 Key Takeaways

- **Growth is strong, but profitable growth matters more than revenue alone.**
- **Online offers a compelling scaling opportunity** with a 42.3% margin.
- **Direct customers are highly valuable** and should receive stronger retention focus.
- **232 lapsed customers represent a measurable reactivation opportunity.**
- **Product profit is concentrated**, with two hero SKUs contributing approximately 32%.
- **Sampling looks promising but requires experimentation before causal conclusions can be made.**
- **Data quality is a business issue, not just a technical issue** — 39.7% of revenue currently sits within unmapped geography.

---

## 🛠️ Tech Stack

- Power BI
- DAX
- Power Query
- Excel
- Data Modelling
- Data Visualisation
- Commercial Analytics
- Customer & Product Analysis
- Data Quality / QA
