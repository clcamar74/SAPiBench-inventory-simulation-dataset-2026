SAPiBench Inventory Simulation Dataset 2026
A reproducible synthetic dataset and methodology for inventory forecasting and simulation research

Overview
This repository provides a complete, transparent, and fully reproducible dataset for inventory forecasting and simulation studies. It includes:

50 retail items with realistic master data
7 years of daily demand (2019–2025)
Seasonality, weekly patterns, and stochastic noise
Cost parameters for inventory optimization

A single generator script that recreates the entire dataset

The dataset is designed for academic research, thesis work, and benchmarking of forecasting and replenishment algorithms without relying on proprietary ERP systems.

Repository Contents

File	                              Description
material_master.csv	                Master data for 50 items (category, base demand, seasonality, lead time, costs)
synthetic_7year_demand.csv	        Daily demand for each item from 2019–2025
synthetic_generator.py	            Full generator script that produces both CSV files
README.md	                          Documentation of dataset, methodology, and reproducibility

Google Colab Integration

You can run the generator directly in Google Colab using this badge:
Open In Colab (colab.research.google.com in Bing)

Replace <your-username> with your GitHub username.

Colab allows you to:

run the generator without installing Python locally
regenerate the dataset instantly
inspect and modify the code interactively
save outputs directly to Google Drive

This is ideal for committee demonstrations and reproducibility.

Reproducing the Dataset
To regenerate the full dataset, run:

python synthetic_generator.py
This will create:

material_master.csv
synthetic_7year_demand.csv

The generator is self‑contained:
It defines the material catalog internally and uses it to produce the 7‑year synthetic demand.

Dataset Description
Material Master
Each of the 50 items includes:

material ID
category
base daily demand
seasonality type
lead time
unit cost
holding cost rate
ordering cost
stockout penalty

This structure mirrors real ERP master data (e.g., SAP MM).

7‑Year Daily Demand
Demand is generated using:

monthly seasonality
weekly seasonality
category‑specific seasonal effects
random noise (±20%)
non‑negative demand constraints

This produces realistic retail demand suitable for forecasting and simulation.

Methodology
1. Synthetic Data Generation
The generator applies:

deterministic seasonality
stochastic variation
item‑specific base demand
category‑specific seasonal effects

The result is a realistic, reproducible dataset.

2. Forecasting Framework (80/20 Split)
The dataset supports:

80% training window
20% testing window
MAPE, RMSE, MAE evaluation

This aligns with forecasting research standards.

3. Inventory Simulation Engine
The dataset is designed for simulation of:

reorder point behavior
lead time effects
purchase order timing
stockouts
ending inventory
total cost (holding + ordering + stockout)

This mirrors classical inventory control logic used in ERP/MRP systems.

Scenario Design
The dataset supports multiple replenishment scenarios:

Baseline (historical average)
Forecast‑driven
Optimized reorder point
EOQ‑based ordering
Hybrid strategy

Each scenario can be evaluated using:

total cost
service level
stockout days
average inventory
order frequency

This enables comparative analysis for thesis and publication.

Dependencies
Install required libraries:

pip install pandas numpy
These are standard scientific Python packages.

Intended Use
This dataset is designed for:

academic theses
forecasting model evaluation
inventory simulation experiments
supply chain analytics education
benchmarking replenishment policies

It is not intended for production ERP use.

License
This project is licensed under the MIT License.
You may use, modify, and distribute the dataset and code with attribution.

Citation
Camar, C. (2026). SAPiBench Inventory Simulation Dataset 2026.
GitHub Repository: https://github.com/clcamar74/SAPiBench-inventory-simulation-dataset-2026

Camar, C. (2026). SAPiBench Inventory Simulation Dataset 2026.
GitHub Repository: https://github.com/<your-username>/SAPiBench-inventory-simulation-dataset-2026
Replace <your-username> with your GitHub username.
