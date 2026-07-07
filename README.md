# Supply-Chain-Capacity-Production-Optimization-Model
# Supply Chain Production & Capacity Optimization Model
## 📌 Project Overview
This project delivers a data-driven optimization solution to a complex capacity planning and production scheduling problem over a dynamic 24-month horizon. The core objective is to programmatically evaluate the financial and operational trade-offs between maintaining a baseline production model versus transitioning to an expanded workforce structure. 
The model factors in critical real-world logistics challenges: permanent labor lock-in constraints, fluctuating market demand, and steep external outsourcing premiums.
Using **Python** and **Pandas**, I developed a simulation engine that tests all 25 possible operational paths to pinpoint the exact global minimum cost strategy.
> **Note on Confidentiality:** To comply with professional standards and non-disclosure practices, all data points, volumes, and timeframes in this repository have been programmatically randomized/anonymized. The structural integrity and logic of the optimization algorithm remain fully identical to real-world deployment.
---
## 🛠️ Problem Statement & Constraints
*   **Demand Volatility:** Monthly demand forecasts show heavy seasonal fluctuations, frequently exceeding internal production caps.
*   **Capacity Tiers:** The plant operates on two capacity levels: **Baseline (3-Shift)** and **Expanded (4-Shift)**.
*   **Labor Constraint (Lock-In):** Upgrading to a 4-shift model unlocks higher capacity but incurs an immediate fixed operational overhead of **$1,000,000/month**. Once activated, legal and labor agreements lock this structure in through the end of the 24-month horizon.
*   **Outsourcing Premium:** Any market demand that cannot be met by internal production must be fulfilled by an external Manufacturing Partner (MP) at a heavy markup (**$4.35/unit** outsourced vs. **$0.85/unit** variable in-house cost).
---
## 🚀 Simulation Logic & Operational Strategy
Instead of relying on manual trial-and-error spreadsheet modeling, the Python script automates the scenario analysis by iterating through every potential transition milestone (including a baseline "Never Switch" benchmark). 
The algorithm evaluates the cumulative cost function for each scenario:
$$\text{Total Cost} = \sum_{t=1}^{24} \left( \text{In-House Production}_t \times 0.85 + \text{Fixed Overhead}_t + \text{Outsourced Units}_t \times 4.35 \right)$$
### 📊 Key Insights Matrix (Top Scenarios)
The simulation successfully identified that executing the 4-shift transition in **Year 2 - January** yields the global minimum cost structure for the supply chain network.

| Strategy / Switch Month | Total Cost ($) | Total Outsourced Volume (Units) | Strategy Status |
| :--- | :--- | :--- | :--- |
| **Year2-Jan** | **$93,457,165.00** | **8,897,960** | **🏆 Optimal Solution** |
| Year2-Feb | $93,538,315.00 | 9,206,860 | Suboptimal (+ $81K) |
| Year2-Mar | $93,602,315.00 | 9,510,860 | Suboptimal (+ $145K) |
| **Never Switch (Baseline)** | **$94,966,465.00** | **12,757,760** | **Cost Leakage (- $1.5M)** |

---
## 📈 Quantifiable Business Impact
*   **$1,509,300.00 Net Savings:** Strategically timing the shift change prevented over-manufacturing and fixed cost bleeding during low-demand periods, while securing high in-house capacity right before major demand spikes.
*   **Risk Mitigation:** Reduced reliance on external manufacturing partners by **3,859,800 units**, significantly shielding the company from external supply chain disruptions and third-party dependency.
*   **Agility & Scalability:** Created a dynamic optimization script capable of re-running and adapting instantly whenever the marketing team updates the demand forecast.
---
## 💻 Tech Stack & Environment
*   **Language:** Python 3.x
*   **Primary Libraries:** Pandas
*   **Concepts Applied:** Cost Accounting, Production Capacity Planning, Scenario Simulation, Linear Constraints.
---
## 🏃 How to Run the Model
1. Clone this repository:
   ```bash
   git clone [https://github.com/yourusername/supply-chain-capacity-optimization.git](https://github.com/yourusername/supply-chain-capacity-optimization.git)
