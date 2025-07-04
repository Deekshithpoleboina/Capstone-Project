
# 🚗 Dynamic Pricing for Urban Parking Lots

## 📌 Overview
This project implements an intelligent, real-time pricing engine for 14 urban parking lots using dynamic strategies based on occupancy levels, queue length, traffic congestion, and special event indicators. The goal is to maximize utilization while ensuring price fairness and system adaptability throughout the day.

## 🛠 Tech Stack
- **Python**: `pandas`, `numpy`
- **Pathway**: Real-time data streaming
- **Bokeh**: Interactive visualizations
- **Google Colab**: Notebook execution environment
- **GitHub**: Version control and hosting

## 🔧 Architecture Diagram

```
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

## 🧠 Project Workflow

1. **Data Collection**  
   The dataset contains time-series data from 14 parking lots, recorded over 73 days and 18 intervals per day (every 30 minutes from 8:00 AM to 4:30 PM).

2. **Feature Engineering**  
   - Combine date and time into a single timestamp  
   - Calculate occupancy rate  
   - Encode traffic congestion as numeric levels  
   - Normalize queue length and special day indicators  

3. **Modeling**
   - **Model 1: Baseline Linear Model**  
     Price increases linearly with occupancy rate  
     `Price[t+1] = Price[t] + α * (Occupancy / Capacity)`

   - **Model 2: Demand-Based Pricing**  
     A composite demand function considers occupancy, traffic, queue, special days, and vehicle type.  
     Adjusted price = `BasePrice * (1 + λ * NormalizedDemand)`

   - **Model 3: Competitive Pricing (Optional)**  
     Takes into account prices of nearby lots (via latitude and longitude)  
     Includes rerouting suggestions for full lots or strategic price reduction

4. **Real-Time Simulation with Pathway**  
   - Simulates streaming data with timestamps  
   - Integrates pricing logic into Pathway’s real-time processing pipeline

5. **Visualization with Bokeh**  
   - Real-time line plots of price per parking lot  
   - Competitor price comparisons  
   - Interactive filtering by time, lot, and vehicle type

## 📂 Repository Structure

```
📦 dynamic-parking-pricing/
├── Capstone_Project_Submission.ipynb     # Main implementation notebook
├── dataset.csv                           # Input dataset
├── README.md                             # Project documentation
├── architecture.md / architecture.png    # Mermaid diagram or PNG
├── pricing_models.py                     # (Optional) Modular model implementation
├── report.pdf                            # (Optional) Written report submission
├── star_repo_pathway.png                 # Required screenshot 1
├── star_repo_llm_app.png                 # Required screenshot 2
```

## 📈 Output Examples

### 🔹 Sample Output from Capstone_Project_Submission.ipynb

- **Occupancy Rate + Price Calculation Preview**  
  ![Occupancy Rate Table](![Screenshot 2025-07-04 155928](https://github.com/user-attachments/assets/c784437a-f36c-4988-b3e0-6b53e1a0b5e2)
)

- **Predicted Prices Over Time**  
  [Price Over Time](![Screenshot 2025-07-04 160451](https://github.com/user-attachments/assets/71d17a7a-2402-4be5-a2df-69895fc1093d)
)

### 🖼️ Starred Repository Proofs

#### ⭐ Starred Pathway Repository  
![Starred Pathway](Screenshot_Pathway_Star.png)

#### ⭐ Starred LLM App Repository  
![Starred LLM App](Screenshot_LLM_App_Star.png)




## 🔗 Useful Resources
- [📘 Pathway Documentation](https://pathway.com/developers)
- [📗 Bokeh Docs](https://docs.bokeh.org/en/latest/)
- [📘 Summer Analytics 2025](https://www.caciitg.com/sa/course25/)
