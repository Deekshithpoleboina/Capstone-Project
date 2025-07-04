# 🚗 Dynamic Pricing for Urban Parking Lots

## 📌 Overview
This project implements an intelligent, real-time pricing engine for 14 urban parking lots based on occupancy, queue length, traffic conditions, special days, and more. The goal is to optimize lot utilization using dynamic pricing strategies.

## 🛠 Tech Stack
- Python (Pandas, Numpy)
- Pathway (Real-time streaming)
- Bokeh (Visualization)
- Google Colab (Notebook environment)
- GitHub (Version control & hosting)

## 🔧 Architecture Diagram

```mermaid
graph TD
    A[CSV Input: dataset.csv] --> B[Data Preprocessing]
    B --> C1[Model 1: Baseline Linear Pricing]
    B --> C2[Model 2: Demand-Based Pricing]
    B --> C3[Model 3: Competitive Pricing (Optional)]
    C1 --> D[Real-Time Price Output via Pathway]
    C2 --> D
    C3 --> D
    D --> E[Bokeh Visual Dashboard]
```
