\# Superstore Retail Margin \& Profitability Diagnostic



\## Executive Summary

This project evaluates retail transaction data across products, fulfillment channels, and regions to diagnose the primary root causes of negative operating margins. The analysis pinpoints the threshold where promotional discounting turns value-destructive and identifies structural margin leakage in specific product categories and shipping modes. Based on these diagnostics, actionable pricing and logistics interventions are proposed to restore category-level profitability.



\---



\## Key Visualizations



\### 1. The 20% Discount Cliff

Operating margins experience a steep cliff once promotional discounts exceed 20%, falling rapidly from healthy positive returns to heavy net losses.



!\[Profit Margin by Discount Tier](reports/figures/discount\_tier\_margin.png)



\### 2. Product Sub-Category Net Profitability

High-volume categories do not always equate to high profit; specific bulky sub-categories drive significant cumulative losses.



!\[Sub-Category Profitability](reports/figures/subcategory\_profit\_margin.png)



\---



\## Core Findings



\* \*\*The 20% Discount Cliff:\*\*

&#x20; \* Transactions with \*\*0% to 20% discounts\*\* maintain healthy, positive net profit margins ranging between \*\*+11.9% and +29.5%\*\*.

&#x20; \* Any discount above \*\*20% destroys margins entirely\*\*, plummeting to \*\*-19.7%\*\* for moderate discounts (21%–50%) and \*\*-119.2%\*\* for deep discounts (>50%).

\* \*\*Product Sub-Category Leakage:\*\*

&#x20; \* \*\*Tables\*\* (-$17,725.48 net profit, -8.6% margin) and \*\*Bookcases\*\* (-$3,472.56 net profit, -3.0% margin) represent the largest absolute loss drivers.

&#x20; \* Both sub-categories suffer from a combination of bulky freight profiles and aggressive promotional discounts exceeding 21%–26%.

\* \*\*Shipping Mode Inefficiency:\*\*

&#x20; \* \*\*Standard Class\*\* handles the largest overall sales volume ($1.35M) but registers a \*\*31.4% loss-making order rate\*\*.

&#x20; \* Economy shipping fails to offset thin transaction margins on heavily discounted, low-order-value items.



\---



\## Business Recommendations



1\. \*\*Enforce Strict Discount Governance:\*\*

&#x20;  \* Cap general sales representative discounts at a hard maximum of \*\*20%\*\*.

&#x20;  \* Require mandatory management override and margin-check workflows for any discount request exceeding 20%.

2\. \*\*Restructure Bulky Furniture Pricing:\*\*

&#x20;  \* Terminate unhedged promotional discounting on high-bulk items like Tables and Bookcases.

&#x20;  \* Introduce a dedicated freight surcharge or pass-through delivery fee for oversized furniture items.

3\. \*\*Establish Minimum Order Thresholds for Free Delivery:\*\*

&#x20;  \* Set a minimum basket size required to qualify for free Standard Class fulfillment to eliminate loss-making single-item orders.



\---



\## Project Structure



```text

superstore-margin-diagnostic/

├── data/

│   ├── raw/

│   └── processed/

│       └── Sample\_Superstore\_Cleaned.csv

├── notebooks/

│   └── superstore\_margin\_diagnostics.ipynb

├── reports/

│   └── figures/

│       ├── discount\_tier\_margin.png

│       └── subcategory\_profit\_margin.png

├── .gitignore

├── requirements.txt

└── README.md

