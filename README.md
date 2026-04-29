# Online Retail Customer Segmentation & Revenue Analysis

## Project Overview
This project is a Descriptive and Exploratory Data Analysis of the UCI Online 
Retail II dataset — 541,910 transactions from a UK-based retailer spanning 
December 2010 to December 2011. The goal was to uncover revenue drivers, 
identify top-performing products, understand geographic distribution, and 
segment customers using RFM analysis to generate actionable business 
recommendations.

**Tool:** Microsoft Excel  
**Dataset:** UCI Online Retail II (Kaggle)  
**Records:** 541,910 transactions | 8 columns  
**Analyst:** Gospel [Your Last Name]

---

## Business Problem
> *"Which customer segments, products, and markets drive the most revenue — 
and what should the business prioritise to grow and retain its customer base?"*

---

## Data Cleaning Summary
The raw dataset contained multiple quality issues addressed before analysis:

| Issue | Count | Action |
|---|---|---|
| Duplicate rows | 5,267 | Removed |
| Cancellation invoices | 9,288 | Separated to own sheet |
| Zero/negative price rows | 2,517 | Removed |
| Blank descriptions | 1,454 | Removed |
| Admin stock codes (POST/DOT/M) | Various | Separated |
| Blank Customer IDs | 135,080 | Flagged — kept for revenue analysis |

---

## Key Findings

### Revenue Analysis
- **Total Revenue:** £3,666,179
- **Total Transactions:** 189,231
- **Average Order Value:** £19.37
- **Highest Single Transaction:** £77,183

### Top 5 Products by Revenue
| Product | Revenue |
|---|---|
| Regency Cakestand 3 Tier | £93,177 |
| Medium Ceramic Top Storage Jar | £77,778 |
| White Hanging Heart T-Light Holder | £54,319 |
| Party Bunting | £39,540 |
| Jumbo Bag Red Retrospot | £34,028 |

### Geographic Distribution
| Country | Revenue | Share |
|---|---|---|
| United Kingdom | £3,120,658 | 85% |
| Netherlands | £101,143 | 2.8% |
| EIRE | £85,453 | 2.3% |
| Germany | £79,555 | 2.2% |
| France | £61,341 | 1.7% |

### RFM Customer Segmentation
1,727 identifiable customers were scored and segmented:

| Segment | Count | % of Customers |
|---|---|---|
| Champion | 38 | 2.2% |
| Loyal | 265 | 15.3% |
| Potential Loyal | 465 | 26.9% |
| At Risk | 251 | 14.5% |
| Lost | 260 | 15.1% |
| Needs Attention | 446 | 25.8% |
| High Value Customer Lost | 3 | 0.2% |

---

## Business Recommendations

1. **Protect Champions** — Introduce a VIP retention programme for the 38 
Champion customers who likely drive disproportionate revenue
2. **Convert Potential Loyals** — Launch targeted re-engagement campaigns 
for the 465 Potential Loyal customers — the highest-leverage segment
3. **Recover At Risk customers** — Deploy personalised win-back campaigns 
for 251 At Risk customers before they become Lost
4. **Investigate Lost customers** — Segment the 260 Lost customers by 
monetary value before writing them off
5. **Reduce UK dependency** — Develop market expansion strategy for 
Netherlands, EIRE, and Germany to reduce 85% UK revenue concentration risk
6. **Protect hero products** — Identify and develop backup hero products 
to reduce dependency on the Regency Cakestand

---

## Limitations
- Time Trend Analysis was attempted but Excel encountered mixed date formats 
across the InvoiceDate column. This would be resolved using Python's pandas 
library with pd.to_datetime() — flagged for future work.
- RFM analysis covers only the 1,727 customers with valid Customer IDs. 
The remaining 56,539 unidentified transactions were excluded from 
customer-level analysis.

---

## Excel Functions Used
`SUMIF` `COUNTIF` `DATEDIF` `IF` `IFERROR` `MAX` `MIN` `AVERAGE` 
`TEXT` `TRIM` `SUBSTITUTE` `CONCAT` `VLOOKUP`

---

## Project Structure
online-retail-customer-segmentation/
│
├── Online_Retail_Dataset.xlsx    # Cleaned dataset with all analysis sheets
├── README.md                     # Project documentation
└── screenshots/                  # Key visuals from the analysis
├── rfm_segments.png
├── top_products.png
└── country_analysis.png

---

## Author
**Gospel Arinze**  
Data Analyst | Product Analyst  
[LinkedIn Profile URL](https://www.linkedin.com/in/gospel-arinze-55590424a/) \n
[GitHub Profile URL](https://github.com/ifeyichukwu)
