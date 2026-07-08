# Inventory-Optimization-ABC-XYZ
An Excel-based inventory segmentation framework analyzing 1,000 SKUs to optimize warehouse capacity and working capital.

# Inventory Optimization & Capital Rationalization Dashboard (ABC-XYZ Analysis)

## 📌 Project Overview & Business Case
This project applies a data-driven supply chain framework to a retail dataset containing 1,000 unique SKUs. By evaluating total annual revenue concentration (ABC Analysis) alongside demand predictability and monthly sales volatility (XYZ Analysis), this framework optimizes warehouse shelf allocation and identifies opportunities to free up locked working capital.

* **Tools Used:** Microsoft Excel (Advanced Statistical Functions, Nested IF Logic, Dynamic Running Totals, Multi-Field Pivot Tables)
* **Dataset Size:** 1,000 items | Total Portfolio Revenue: $1.072 Billion

---

## ⚙️ Methodology & Threshold Rules

### 1. ABC Classification (Value/Revenue Analysis)
Data was sorted in descending order by revenue, utilizing a dynamic cumulative percentage algorithm: `=SUM($R$2:R2) / SUM($R:$R)`.
* **Category A (Top 70%):** High Value / Core Revenue Drivers.
* **Category B (Next 20%):** Medium Value / Standard Inventory.
* **Category C (Bottom 10%):** Low Value / Slow Movers (Long Tail).

### 2. XYZ Classification (Demand Predictability Analysis)
Calculated via the Coefficient of Variation ($CV$), derived by dividing monthly sales standard deviation (`STDEV.S`) by mean monthly demand (`AVERAGE`).
* **Category X (CV ≤ 0.2):** Stable, predictable monthly demand.
* **Category Y (0.2 < CV ≤ 0.5):** Fluctuating demand (seasonal or trend-driven).
* **Category Z (CV > 0.5):** Erratic, highly unpredictable demand spikes.

---

## 📊 Dynamic Portfolio Matrix (Summary Grid)

| Value / Volatility | X (Stable) | Y (Seasonal) | Z (Erratic) | **Total Count** |
| :--- | :--- | :--- | :--- | :--- |
| **A (High Revenue)** | **50 SKUs** ($704.3M) | **6 SKUs** ($45.7M) | **0 SKUs ($0)** | **56 SKUs** |
| **B (Medium Revenue)**| 88 SKUs ($199.0M) | 5 SKUs ($12.6M) | 2 SKUs ($3.0M) | **95 SKUs** |
| **C (Low Revenue)** | 674 SKUs ($88.1M) | 116 SKUs ($14.9M)| 59 SKUs ($4.4M)| **849 SKUs**|
| **Total SKUs** | **812** | **127** | **61** | **1,000 SKUs** |

---

## 💡 Strategic Executive Conclusions

### 1. Risk Mitigation (The "AZ" Void)
The analysis conclusively proves there are **0 active items sitting in the high-risk AZ quadrant**. This represents an ideal supply chain state—our high-value revenue streams are entirely decoupled from random, erratic volatility. Because category A demand is highly stable (AX/AY), the business can safely lower defensive safety stock buffers to aggressively maximize working capital cash flows.

### 2. Operational Automation (The "AX" Revenue Engine)
Just **50 SKUs in the AX quadrant drive an overwhelming 65.7% of total portfolio revenue ($704.3 Million)**. Because these core drivers feature steady, highly predictable demand, the purchasing team should migrate them to an automated, Just-In-Time (JIT) system to eliminate manual processing overhead.

### 3. Structural Cost Reduction (The "CZ" Dead Weight)
The **CZ segment contains 59 SKUs that trigger erratic demand spikes while contributing next to zero financial value ($4.4 Million / 0.4% total revenue)**. These items are dragging down warehouse efficiency and inflating holding costs. 
* **Action:** Transition non-essential CZ SKUs to a strict "Order-on-Demand" model or discontinue them entirely to optimize physical warehouse capacity.

* ## 📂 Project Navigation
* 📁 `abc_xyz_dataset.xlsx`: Open this master spreadsheet to inspect the interactive pivot tables, clean data types, and custom formatting configurations.

---
