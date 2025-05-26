# Vehicle Routing Problem (VRP) Optimization using Particle Swarm Optimization (PSO)

This project implements a metaheuristic solution to the classic **Vehicle Routing Problem (VRP)** with time windows, vehicle capacity constraints, and cost minimization using **Particle Swarm Optimization (PSO)**.

The goal is to minimize total logistics costs by optimizing the delivery routes for multiple vehicles from a central depot to a set of customers, considering:
- Transport costs
- Penalty costs for late deliveries
- Fixed costs per vehicle

---

## 🚚 Problem Description

- Deliver goods from a depot (node 0) to multiple customer locations.
- Each customer has:
  - A specific demand
  - A delivery time window
- Each vehicle has:
  - A fixed capacity
  - A fixed operating cost per use
- Routes must:
  - Start and end at the depot
  - Not exceed vehicle capacity
  - Minimize overall cost (transport + penalty + fixed)

---

## ✅ Features

- Custom fitness evaluation considering:
  - Transport cost (distance × cost per km)
  - Penalty cost (late arrivals)
  - Fixed vehicle usage cost
- Handles time windows and vehicle capacity
- PSO-based solution with:
  - Position and velocity updates
  - Particle evaluation based on cost
- Simulation-ready and customizable parameters
