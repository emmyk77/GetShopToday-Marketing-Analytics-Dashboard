# GetShopToday Campaign Performance

Influencer campaigns recorded the most paid transactions (60). Pay-per-click campaigns generated the most recorded revenue ($11,842.36) from 54 paid transactions. Across the 1,000 records, each dollar of marketing spend corresponded to $0.70 of recorded revenue.

[Download the corrected campaign summary](GetShopToday-Campaign-Summary.xlsx) · [View source CSV](Datasets/GetShop%20Today%20Customer%20Data.csv)

![Excel campaign summary showing spend, clicks, paid transactions, recorded revenue, ROAS and CPA for each campaign.](Images/dashboard_preview.png.jpeg)

## Dashboard measures

| Measure | All campaigns | Calculation |
| --- | ---: | --- |
| Marketing spend | $84,042.16 | Sum of recorded spend |
| Clicks | 4,831,721 | Sum of valid clicks |
| Paid transactions | 276 | Count of transaction rows with PaidCustomer equal to 1 |
| Recorded revenue | $59,067.11 | Sum of recorded revenue on paid transactions |
| Return on ad spend (ROAS) | 0.70× | Recorded revenue divided by marketing spend |
| Cost per acquisition (CPA) | $304.50 | Marketing spend divided by paid transactions |

The campaign summary calculates channel and overall ROAS and CPA from the corresponding totals. CPA uses a paid transaction as the acquisition event. The 276 paid transactions represent 274 distinct customer IDs. ROAS describes revenue relative to marketing spend. Estimating profit would also require product and operating costs.

## Explore the workbook

1. Download the **corrected campaign summary** and open it in Excel. The workbook has one worksheet with six campaign rows and their totals.
2. Compare paid transactions and recorded revenue by campaign. The ROAS and CPA columns contain formulas that recalculate when the aggregate inputs change.
3. For the original dashboard layout and slicers, see the [original interactive Excel workbook](GetShop%20Today%20Customer%20Data%20%20Final%20project.xlsx). Its “Total ROI” and “Total CPA” cards and CPA chart sum row-level measures. Use the corrected campaign summary for acquisition cost and return on ad spend.

The downloadable summary is an aggregate snapshot. Its six input rows contain channel totals and have no underlying transaction-level records or slicers.

## Data preparation and interpretation

The source contains 1,000 transaction rows. The analysis counts a transaction as paid only when its flag equals 1. It treats 477 missing payment flags as unpaid, 180 missing spend values as zero, and 20 invalid click entries as zero. A further 43 paid transactions lack a revenue amount, so the revenue and ROAS figures reflect the amounts on record. The Unknown campaign group retains 120 source rows with that label.

The original workbook’s **Cleaned** sheet stores spend, clicks, impressions and revenue in thousands. The campaign summary restores their original units. The source table retains its legacy ROI field, which measures revenue less marketing spend divided by marketing spend. The corrected summary uses ROAS, which can be calculated directly from the available fields.

**Tools** · Microsoft Excel, PivotTables, PivotCharts, slicers and GETPIVOTDATA.

[Emmanuel Kebodi](https://github.com/emmyk77)
