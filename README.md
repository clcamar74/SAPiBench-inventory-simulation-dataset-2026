# SAPiBench: Inventory Simulation and Forecasting Benchmark Dataset (2026)

SAPiBench is a synthetic, fully reproducible benchmarking framework designed for
evaluating inventory forecasting models, replenishment policies, and economic
valuation in S/4HANA-oriented environments.

This repository provides:

- A 100‑item Walmart‑style synthetic material master  
- Seven years of daily demand (2019–2025)  
- Seasonality, weekly patterns, and stochastic noise  
- Cost parameters for inventory optimization  
- A complete generator script that recreates the entire dataset  
- A Google Colab notebook for end‑to‑end forecasting and simulation  

The dataset is intended for academic research, thesis work, and benchmarking of
forecasting and replenishment algorithms without relying on proprietary ERP
systems.

---

## 📁 Repository Contents

| File | Description |
|------|-------------|
| **material_master.csv** | Master data for 100 items (category, base demand, seasonality, lead time, costs) |
| **synthetic_7year_demand.csv** | Daily demand for each item from 2019–2025 |
| **synthetic_generator.py** | Full generator script that produces both CSV files |
| **SAPiBench.ipynb** | End‑to‑end forecasting, simulation, and valuation notebook |
| **README.md** | Documentation of dataset, methodology, and reproducibility |

---

## 🚀 Google Colab Integration

You can run the notebook or regenerate the dataset directly in Google Colab.

Colab allows you to:

- Run the generator without installing Python locally  
- Regenerate the dataset instantly  
- Inspect and modify the code interactively  
- Save outputs directly to Google Drive  

This is ideal for thesis defenses, committee demonstrations, and reproducibility.

---

## 🔁 Reproducing the Dataset

python synthetic_generator.py


This will create:

- `material_master.csv`  
- `synthetic_7year_demand.csv`  

The generator is **self‑contained** and includes:

- The full 100‑item catalog  
- Seasonality logic  
- Weekly patterns  
- Noise generation  
- Cost parameter assignment  

---

## 📊 Dataset Description

### **1. Material Master**

Each of the 100 items includes:

- Material ID  
- Category  
- Base daily demand  
- Seasonality type  
- Lead time  
- Unit cost  
- Holding cost rate  
- Ordering cost  
- Stockout penalty  

This structure mirrors real ERP master data (e.g., SAP MM).

---

### **2. Seven‑Year Daily Demand (2019–2025)**

Demand is generated using:

- Monthly seasonality  
- Weekly seasonality  
- Category‑specific seasonal effects (Holiday, Summer, School, Rainy)  
- Random noise (±20%)  
- Non‑negative demand constraints  

This produces realistic retail demand suitable for forecasting and simulation.

---

## 🧠 Methodology

### **1. Synthetic Data Generation**

The generator applies:

- Deterministic seasonality  
- Stochastic variation  
- Item‑specific base demand  
- Category‑specific seasonal effects  

The result is a realistic, reproducible dataset.

---

### **2. Forecasting Framework**

The dataset supports:

- 80/20 train‑test split  
- Evaluation using MAPE, RMSE, MAE  
- Classical forecasting models (Naive, Moving Average, Random Forest, Gradient Boosting)  

This aligns with forecasting research standards.

---

### **3. Inventory Simulation Engine**

The dataset is designed for simulation of:

- Reorder point behavior  
- Lead time effects  
- Purchase order timing  
- Stockouts  
- Ending inventory  
- Total cost (holding + ordering + stockout)  

This mirrors classical inventory control logic used in ERP/MRP systems.

---

## 🧪 Scenario Design

The dataset supports multiple replenishment scenarios:

- Baseline (historical average)  
- Forecast‑driven  
- Optimized reorder point  
- EOQ‑based ordering  
- Hybrid strategies  

Each scenario can be evaluated using:

- Total cost  
- Service level  
- Stockout days  
- Average inventory  
- Order frequency  

This enables comparative analysis for thesis and publication.

---

## 📦 Dependencies

Install required libraries:


pip install pandas numpy


These are standard scientific Python packages.

---

## 🎯 Intended Use

This dataset is designed for:

- Academic theses  
- Forecasting model evaluation  
- Inventory simulation experiments  
- Supply chain analytics education  
- Benchmarking replenishment policies  

It is **not** intended for production ERP use.

---

## 🔁 Reproducibility Notes

- All data is synthetic and generated using `synthetic_generator.py`.  
- The notebook loads fixed CSV files from GitHub to ensure consistent results.  
- Randomness is controlled using fixed seeds.  
- The entire workflow is designed to run end‑to‑end with a single click.  

---

## 📄 Citation

If you use SAPiBench in academic work, please cite:

**Camar, C. (2026).  
SAPiBench: A Synthetic Benchmark and Simulation Framework for S/4HANA‑Oriented Inventory Forecasting, Policy Analysis, and Economic Valuation.**

GitHub Repository:  
https://github.com/clcamar74/SAPiBench-inventory-simulation-dataset-2026

---

## 📬 Contact

For questions, clarifications, or reproducibility concerns, please contact:

**clcamar@up.edu.ph**

---

## 📝 License

This project is licensed under the **MIT License**.  
You may use, modify, and distribute the dataset and code with attribution.






To regenerate the full dataset locally:

