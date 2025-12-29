# NutriBox Supply Chain Optimisation

This project models and solves a realistic supply chain transportation problem using linear programming.

The objective was not just to find the cheapest solution, but to understand how real-world constraints
(time, emissions, capacity, and operational limits) affect feasibility and decision-making.

---

## 📦 Problem Overview

NutriBox needs to ship **600 pallets** from **4 factories** to **5 destinations** using:
- **3 distribution centres**
- Limited direct factory-to-destination routes
- Strict capacity limits on routes and facilities

The model includes:
- Factory supply constraints
- Destination demand constraints
- Distribution centre flow balance
- Arc capacity limits
- Distribution centre inbound and outbound limits
- Minimum rail usage policy
- Operational complexity constraint (limited active routes)

---

## ⚠️ Key Insight

When strict **time** and **CO₂ emission** limits were applied together,  
**no feasible solution existed**.

This reflects a real supply chain challenge:
sometimes the network structure itself makes certain targets impossible.

Instead of forcing a solution, the problem was reframed to explore trade-offs.

---

## 🔍 Scenarios Solved

Four optimisation scenarios were analysed:

1. **Cheapest Solution**
   - Minimises total transportation cost
   - Ignores time and emissions limits
   - Shows the cost of prioritising savings

2. **Fastest Solution**
   - Minimises total delivery time
   - Ignores cost and emissions
   - Highlights service-level trade-offs

3. **Cleanest Solution**
   - Minimises total CO₂ emissions
   - Ignores cost and time
   - Demonstrates sustainability impact

4. **Balanced (Feasible) Solution**
   - Minimises cost
   - Subject to relaxed but achievable time and CO₂ limits
   - Represents a realistic operational compromise

Each scenario satisfies all structural and operational constraints.

---

## 🛠 Tools Used

- **Python**
- **PuLP** (Linear Programming modelling)
- **CBC Solver** (via PuLP)

---

## 📁 Repository Structure

