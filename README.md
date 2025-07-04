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
## 🧠 Project Workflow
- Data Collection: Dataset includes timestamped parking metrics (occupancy, queue, etc.)

- Feature Engineering: Occupancy rate, congestion level encoding, datetime merging

- Pricing Models:

- Model 1: Linear occupancy-based

- Model 2: Demand function with multiple features

- Model 3 (optional): Competitive pricing based on geospatial proximity

- Real-Time Simulation: Implemented using Pathway stream processor

- Visualization: Bokeh plots for price over time and lot comparisons

## 📂 Repository Structure

📦 dynamic-parking-pricing/
├── Capstone_Project_Submission.ipynb
├── dataset.csv
├── README.md
├── architecture.png / mermaid.md
├── pricing_models.py (optional)
└── report.pdf (optional)

## 📈 Output Examples
- Add screenshots or GIFs of your visual dashboard here (optional)

## 🔗 Resources
Pathway Docs

Bokeh Documentation


---

#### 2. **Screenshots**
- Upload and name the starred repo screenshots:  
  `star_repo_pathway.png` and `star_repo_llm_app.png`

---

#### 3. **Public GitHub Repo**
Push all files including:
- Notebook: `Capstone_Project_Submission.ipynb`
- Dataset: `dataset.csv` (or link if too large)
- README.md (from above)
- Architecture Diagram (use Mermaid or export image)
- (Optional) `report.pdf`

Make sure the repository is set to **Public**.

---

#### 4. **Final Submission Form Fields**
- ✅ Name, Email, Mobile
- ✅ GitHub Username
- ✅ 2 starred repo screenshots
- ✅ Public GitHub repo link (copy this after push)
- ✅ Any final feedback if you have

---

If you want, I can generate the `README.md` and `architecture.md` files for you right now. Would you like that?
