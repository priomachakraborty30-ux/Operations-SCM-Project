# Operations-SCM-Project
Developed an end-to-end Power BI dashboard analyzing profitability across inventory, logistics, and sales operations. Identified profit leakage driven by logistics costs and forecasting inefficiencies using DAX-based financial modeling.

1.	Project Title 
End-to-End Supply Chain Analytics: Inventory, Logistics & Profitability | Power BI

2.	 Purpose
This Power BI dashboard provides a comprehensive, data-driven analysis of Sportswear Brand’s supply chain performance. Built as part of a supply chain transformation case study, the dashboard is designed to help operations managers, and analysts identify inefficiencies and opportunities across different sectors:
•	Inventory Analysis — 
Understand the current state of stock levels, identify overstocked or understocked SKUs across different categories, and evaluate the effect of wrong forecasting upon working capital. It also showcases key matrices of inventory like WAPE, COGS, DOH, ITR and Total Holding Cost (~2%) due to over estimation.
•	Inbound Logistics Analysis (Supplier to Distribution Centers) – 
Track supplier-side shipment performance, analyzing cost and lead times by region and mode of transport, and identify bottlenecks in the inbound supply flow. Performed reconciliation analysis to check if units are subjected to damage theft or pilferage during the transaction process from Supplier to DC to Warehouses by comparing total inbound units and total receipt units.
•	Outbound Logistics — 
Evaluate distribution efficiency from Distribution Centers to warehouses, with a focus on cost-per-shipment and delivery performance. Analyzed total warehouses distribution across distribution centers and if it is aligned properly as per the demand by comparing the inbound units and sales units.
•	Profit & Margin Analysis — 
Connect supply chain costs to financial outcomes, revealing how logistics spend and inventory inefficiencies are eroding margins across regions and product categories. Performed Monthly revenue, cost and profit comparison can be filtered for different categories.

3. Tech Stack
The dashboard was built using the following tools and technologies:
• 📊 Power BI Desktop – Main data visualization platform used for report creation.
• 📂 Power Query – Data transformation and cleaning layer for reshaping and preparing the data.
• 🧠 DAX (Data Analysis Expressions) – Used for calculated measures, dynamic visuals, and conditional logic.
• 📝 Data Modeling – Relationships established among tables (DC Inbound Data, DC Outbound Data, Warehouse Data, Callender, Profit Structure) to enable cross-filtering and aggregation.
• 📁 File Format – .pbix for development and .png for dashboard previews.

4. Data Source
Data on ~300 unique SKU Products, total 15 Warehouses located at different countries, 3 Distribution Centers around the world and total 3 Supplier countries are mentioned in the data models, including details on product wise inventory units, sales data, forecasting data, unit price info are provided. Other information includes inbound logistics cost, outbound logistics cost across different transport mediums are also mentioned.

5. Features / Highlights:
🔴 Business Problem
A €15B global sportswear brand is experiencing declining profit margins despite strong revenue. The root cause lies within the supply chain — poor forecast accuracy is driving simultaneous overstock and stockouts, working capital worth tens of millions is either blocked in excess inventory or lost to missed sales, inbound procurement costs are heavily concentrated in high-cost nodes, and outbound logistics spend is misaligned with actual regional sales demand. Leadership lacks a single integrated view to diagnose these inefficiencies and prioritize corrective action.

🎯 Goal of the Dashboard:
To build a comprehensive, multi-layered Power BI dashboard that gives supply chain leaders and executives a data-driven diagnostic tool across three interconnected problem areas — Inventory & Forecasting, Inbound Logistics & Profitability, and Outbound Logistics — enabling them to pinpoint inefficiencies, quantify financial impact, and drive targeted interventions.

👁️ Walkthrough of Key Visuals:
Page 1 — Inventory Insights
•	KPI Cards (WAPE, COGS, DOH, ITR, Holding Cost): The headline metrics tell an immediate story — a WAPE of 0.45 signals a poor accuracy in forecasting, it implies on average, forecasts are off by 45 units for every 100 units sold. DOH of 38.57 means inventory sits for over a month on average, and €452.7K in holding costs is a direct cash drain. 
•	Monthly Forecast Bias Chart: Forecast bias oscillates around zero across all three categories throughout the year. While this may suggest no systematic over or under-forecasting, the high volatility — especially for Shoes — reveals that the forecasting process is highly unstable and reactive rather than predictive.
•	DOH by Category (Donut Chart): Shoes carry the heaviest inventory burden at ~28 days, followed by Apparel at ~23 days. Given that Shoes are the highest revenue category, this level of stock build-up is the single largest contributor to working capital blockage.
•	Monthly Effect on WC (Area Chart): It shows effect of Forecasting on working capital, how much working capital is blocked due to over forecasting or how much opportunity is lost due to under forecasting.
•	Net WC Table: Apparel shows negative Net WC, meaning it loses capital through stockouts. Shoes, however, show a positive Net WC of €310K — a classic overstock profile. Whereas Accessories being the only category which has comparatively balanced forecasting resulting in Net WC close to 0. 
•	WC Volatility Scatter Plot: Shoes sit in a high-volatility, high-Net-WC zone — the riskiest quadrant. Accessories and Apparel cluster near zero, indicating smaller but still problematic working capital swings. Shoes being the most demanding product, need proper inventory policy intervention.
________________________________________
Page 2 — Inbound Logistics & Profit Analysis
•	KPI Cards (Revenue, Cost, Profit, Margin, Logistics Cost): With €216M revenue, €150.5M total cost, and a profit of €65.67M at a 30.38% margin, the headline numbers look acceptable — but €49.47M in total logistics cost (nearly 23% of revenue) reveals how much of the margin is being consumed by supply chain spend.
•	IB Logistics across DC (Bar Chart): DC_US dominates inbound logistics at €14.1M — nearly 2.4 times DC Singapore (€5.87M) and almost 4 times DC Europe (€3.68M). Air freight is a notable cost driver at DC_US, pointing to improvement in logistics planning by shifting it to ocean freight.
•	Monthly Supplier Data (Table): All 10 suppliers deliver flat, consistent monthly volumes of around €2.72M regardless of month. This rigidity in suppliers, completely disconnected from seasonality, is one of the main causes of the poor inventory management.
•	Blocked WC vs. Profit by Warehouse (Dual Axis Chart): Several warehouses show high WC Blocked. These warehouses are both capital-intensive and financially underperforming, need operational review.
•	Monthly Revenue, Cost & Profit (Bar + Line Chart): Revenue and costs rise and fall together month-on-month, with the profit line staying relatively flat. This indicates very limited operating leverage.
•	Profit Variation Waterfall: Starting from revenue, the waterfall clearly shows that Holding Cost, Inbound Logistics, and Outbound Logistics are the three sequential profit drains.
•	Profit by Category (Donut): Shoes are dominating the profit (€63.8M), with Apparel at (€23.92M) and Accessories being negligible. This extreme concentration implies that revenue is highly one category dependent.
________________________________________
Page 3 — Outbound Logistics Analysis
•	KPI Cards (Air Share, Non-Air Share, WC Lost, WC Blocked): At €6.77M air and €19.14M non-air, outbound logistics totals ~€25.9M, the outbound network is dealing with both overstock and stockout problems simultaneously — a sign of poor demand-supply synchronization at the warehouse level.
•	Air and Non-Air Share across DC (Bar Chart): DC_US drives the highest outbound cost across both modes — significantly ahead of DC_Singapore and DC_Europe. This, combined with its high inbound cost from Page 2, identifies DC_US as the single most expensive node.
•	WH Count per DC (Donut): While DC_US serves 53.33% of all warehouses (~8 WHs) at the Highest cost, DC Europe serves 26.67% (~4 WHs) at comparatively much lesser cost. This is a stark efficiency gap that points directly to network design and route optimization opportunities.
________________________________________
💡 Overall Business Impact & Insights:
•	Forecasting is the root cause of multiple downstream problems. A WAPE of 0.45 — nearly double the industry benchmark of 0.20–0.30 — cascades into inventory imbalances, emergency air shipments, and both blocked and lost working capital simultaneously. Improving forecast accuracy is the highest-leverage intervention available.
•	The company is not only facing a simple overstock or understock problem — it's facing a segmentation failure, where the wrong products are overstocked while the right ones run out.
•	Shoes carries disproportionate risk. Accounting for 70.6% of profit, the highest inventory days, the most working capital blocked, and the highest forecast error volume — Shoes is simultaneously the most valuable and most vulnerable category in the portfolio.
•	Supplier rigidity is amplifying demand-supply mismatch. Flat monthly supplier volumes regardless of seasonal demand patterns mean warehouses are flooded in low-demand months and potentially short in peak months. Moving to demand-linked procurement cadences is a critical structural fix.
6. Screenshots 


