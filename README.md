# Dubai Real Estate Investment ROI Analysis (2026)

> **Quantifying the Yield Gap: Comparative ROI Analysis Between Long-Term Rentals and Short-Term Airbnb Strategies in Dubai**

---

## 🔗 Project Links
| 📊 Live Dashboard | 📓 Data Processing (Colab) |
| :--- | :--- |
| [View Interactive Looker Studio Report](https://lookerstudio.google.com/reporting/6989015c-66b5-4141-89ab-3348f2f83fbf) | [View Python Analysis & Cleaning](Dubai_Real_Estate_ROI_Analysis.ipynb) |

---

## 🖼️ Dashboard Preview
![Dubai Real Estate Dashboard](DubaiRealEstateInvestmentAnalysis2026MarketROIReport.png)

---
## 🔍 Project Overview
This project involves the synthesis and analysis of a high-fidelity Dubai real estate dataset, integrated with secondary market indicators to model realistic ROI scenarios for 2026. 

The analysis goes beyond surface-level pricing to calculate **True Net Yield**. By merging property-level attributes (size, quality, location) with operational cost data (service charges, management fees), the model simulates the financial delta between long-term and short-term rental strategies across 1,891 properties. This data-driven approach provides a robust framework for identifying high-yield opportunities and optimizing investment performance across the Dubai market.

---
## 🛠️ Technical Stack
* **Data Processing:** R, dplyr (Data Cleaning, Feature Engineering, Metric Calculation) used to synthesize multi-source property data, calculate net ROI metrics, and model the Airbnb "Yield Boost" logic.
* **Development Environment:** Google Colab (Using the R Kernel) for end-to-end data transformation and CSV export.
* **Visualization & BI:** Looker Studio (Advanced Heatmaps, Pivot Tables, Geospatial Analysis).
* **Interactivity:** Implemented cross-filtering and drill-down capabilities to analyze investment efficiency by neighborhood and property quality.

---
## 📈 Key Insights & Findings

* **The Airbnb Premium:** Comparative modeling of 1,891 properties reveals an average **2.6% net ROI increase** when transitioning from long-term to short-term rental strategies.
* **High-Efficiency Zones:** Neighborhoods such as **Remraam** (24.05% ROI) and **Jebel Ali** (20.99% ROI) dominate the high-yield segment, specifically within 'Low' to 'Medium' quality tiers.
* **The Scale vs. Yield Inverse:** Scatter plot analysis shows a clear density of high ROI (20%+) in properties under **2,000 Sq. Ft.**, with diminishing returns as property size increases toward the luxury tier.
* **Operational Cost Burden:** Stacked bar analysis of the "Furniture Factor" highlights that while gross revenue is high, **Annual Service Charges** constitute a significant portion of the expense ratio, particularly for unfurnished assets.
* **Geospatial Price Density:** The heat map identifies that peak **Price per Sq. Ft. (4,800+ dh)** is concentrated in central hubs, identifying a high barrier to entry despite lower percentage yields compared to emerging outskirts.

---
## 🖥️ Dashboard Features

### **Strategic Investment KPIs**
* **Total Properties Analyzed:** High-level summary providing the sample size (1,891 units) used to calculate market averages.
* **Airbnb Yield Boost:** A real-time performance indicator quantifying the average ROI percentage gain when transitioning from long-term to short-term rental models.
* **Avg. Market Price (PSF):** A baseline cost tracker (1,327 dh) used to anchor ROI expectations against current entry prices.

### **Analytical Visuals**
* **Strategy Comparison (Bar Chart):** A neighborhood-level view comparing Long-Term vs. Airbnb Yields to identify the specific ROI delta for each area.
* **ROI Efficiency Grid:** A heatmap-style matrix cross-referencing Neighborhoods against Quality Labels to pinpoint high-performance investment pockets.
* **Portfolio Efficiency Scatter Plot:** Maps property size (Sq. Ft.) against Net ROI, utilizing bedroom-count color coding to identify the "sweet spot" for unit scalability.
* **Operational Expense Decomposition:** A 100% stacked bar analysis visualizing the impact of furniture status on net profit after accounting for service charges and management fees.
* **Market Density Map:** A geospatial heat map identifying high-cost central hubs versus high-yield emerging outskirts based on Price per Sq. Ft.

#### **Chart-to-Chart Cross-Filtering:** Selecting a segment in one visual (such as a specific Neighborhood or Quality Label) dynamically updates all other charts to reflect that specific data subset.

---
## 🛠️ Data Schema & Feature Engineering

To transform raw property listings into a reliable investment model, the following logic was applied using **R (dplyr)**:

* **Market Benchmarking:** Integrated custom datasets for 2026 rental rates, service charges, and Airbnb performance across 29 Dubai neighborhoods.
* **Intelligent Data Filling:** Used property "Quality Labels" to estimate missing financial values, ensuring the final analysis was based on a complete dataset.
* **Net Profit Modeling:** Created formulas to calculate "True Net" income by automatically deducting annual expenses from gross revenue:
    * **Long-Term Strategy:** Deducted service charges and a 5% management fee.
    * **Airbnb Strategy:** Deducted service charges and a 20% management fee to reflect higher operational costs.
* **Data Quality Scrubbing:** Filtered out extreme ROI outliers to ensure the final dashboard presents realistic and achievable investment scenarios.
* **Standardization:** Grouped diverse property types and locations into consistent categories for easier comparison and mapping.
