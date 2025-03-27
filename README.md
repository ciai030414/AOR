# 🏥 COVID-19 Medical Resource Allocation in Los Angeles County

A two-stage modeling framework integrating infection forecasting and hospital-level ICU/ventilator allocation, built using SIR modeling, optimization, and Python-based simulation. This project aims to minimize resource shortages during pandemic surges by regionally optimizing community-to-hospital assignments.

---

## 📊 Project Overview

- **Goal:** Allocate ICU beds and ventilators efficiently to hospitals in LA County based on predicted COVID-19 infections.
- **Scope:** 276 communities and 100+ hospitals across 7 regions.
- **Methods:** SIR-based infection forecasting + greedy and random assignment algorithms.
- **Outcome:** ICU and ventilator shortages reduced significantly with optimized matching.

---

## ⚙️ Methodology

### 📈 Infection Forecasting
- Compared LSTM vs XGBoost → Selected XGBoost for short-term, then SIR for long-term prediction.
- Final prediction model: **SIR model with interpretable epidemiological parameters**.
- Estimated demand:
  - **3% of predicted infections require ICU beds**
  - **6% require ventilators**

### 🔁 Phase One – Region-Based Random Allocation
- Communities assigned randomly to **one hospital within the same region**.
- Demand was aggregated by hospital.
- Result: Several hospitals were **overloaded**, others **underutilized**.

### 🧠 Phase Two – Capacity-Aware Sorted Allocation
- Within each region:
  - Communities sorted by total predicted demand.
  - Hospitals sorted by total available ICU + ventilators.
  - **Greedy one-to-one assignment** based on ranking.
- Result: Shortage dramatically reduced, all hospitals engaged.


---

## 🧱 Repository Structure

```bash
AOR/
├── Allocation/
│   ├── Phase_1_Allocation.py          # Phase 1: Random regional assignment
│   ├── Phase_2_Allocation.py          # Phase 2: Capacity-aware sorted allocation
│   └── Optimised_Allocation_Table.csv # Community-Hospital-Region mapping
├── Data/
│   ├── lacounty_covid.csv             # Infection data per community
│   ├── cleaned_icus_and_ventilators.xlsx # Hospital capacity data
├── Visualisation/
│   └── LA_County_Map.html             # Leaflet-based interactive map
├── Output/
│   ├── Phase_One_Hospital_Resource_Allocation.csv
│   └── Phase_Two_Hospital_Resource_Allocation.csv
├── Final_Project_OR.pdf               # Full formal project report
└── README.md                          # Project summary and guide
