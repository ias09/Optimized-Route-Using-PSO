# 🚚 Vehicle Routing Problem with Time Windows (VRPTW) - PSO Solution

This project implements a **Particle Swarm Optimization (PSO)** algorithm to solve the **Vehicle Routing Problem with Time Windows (VRPTW)**. The work is directly inspired by and improves upon the results from the following paper:

> 📖 Yuhua Li (2024). *Optimization Strategy of Mixed-Integer Linear Planning in Logistics Distribution*  
> Published in *Applied Mathematics and Nonlinear Sciences*  
> [DOI:10.2478/amns-2024-1904](https://doi.org/10.2478/amns-2024-1904)

---

## 🎯 Objective

- Replicate the logistics distribution problem addressed in the paper using real data from Company A.
- Replace the MILP model with a heuristic PSO approach.
- Achieve better or comparable results in terms of:
  - Total cost (transport + penalties)
  - Customer time window satisfaction
  - Customer demand
  - Route efficiency

---

## 📊 Dataset and Scenario

- **24 customers** with:
  - Coordinates
  - Demand (in kg)
  - Acceptable and required time windows
- **5 delivery vehicles**
  - Max load: 2000 kg
  - Transport cost: 2.5 CNY/km
  - Fixed start-up cost: 100 CNY
  - Penalty for early/late delivery: up to 50 CNY
- **Start time:** 5:00 AM (300 minutes after midnight)

---

## 🧠 Solution Approach

- **Algorithm:** Particle Swarm Optimization (PSO)
- **Objective:** Minimize total cost = transport cost + penalty cost
- **Constraint handling:**
  - Vehicle capacity
  - Time windows
  - Demand
- **Evaluation:**
  - Per-vehicle load, distance, cost, penalty
  - Route visualization

---

## 🧾 Results Summary

| Metric             | MILP (Paper) | PSO (This Project) | Outcome       |
|--------------------|--------------|--------------------|---------------|
| Transport Cost     | 4370.51      | 995.01             | ✅ Improved   |
| Penalty Cost       | 191.74       | 0                  | ✅ Reduced    |
| **Total Cost**     | 4562.25      | 1495.01            | ✅ Lowered    |
| Vehicles Used      | 5            | 5                  | Same          |


---

## 🖥️ How to Run

1. Clone the repo:

```bash
git clone https://github.com/ias09/Optimized-Route-Using-PSO.git
cd Optimized-Route-Using-PSO
