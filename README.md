# 🫀 Organ Transplant Matching and Logistics Optimizer

![Python](https://img.shields.io/badge/Language-Python-blue.svg)
![AI Search](https://img.shields.io/badge/Domain-AI%20Search%20%26%20Optimization-brightgreen.svg)
![Status](https://img.shields.io/badge/Status-In%20Development-orange.svg)

## 📋 Project Description

This project aims to develop an AI-based system that simulates the process of **matching organ donors with suitable recipients** and **optimizing organ transportation routes** between hospitals. 

To reflect real-world complexity, the system models the problem under multiple critical constraints:
- **Medical Compatibility:** Blood type compatibility, tissue matching, and medical eligibility.
- **Urgency & Fairness:** Patient clinical priority levels.
- **Time & Logistics Constraints:** Organ preservation time (viability window), transportation time, and distance between hospitals.

---

## 🧠 AI Search Algorithms

The system splits the problem into **allocation/matching** and **route optimization**, applying various uninformed, informed, and constraint-based search algorithms to explore valid solutions and benchmark performance:

| Algorithm | Role in the System |
| :--- | :--- |
| **BFS & DFS** | Explore the state space of possible donor-recipient allocation states. |
| **Backtracking** | Find valid allocation combinations by pruning and rejecting incompatible/invalid matches early. |
| **Uniform Cost Search (UCS)** | Determine the least-cost transportation route between donor and recipient hospitals. |
| **A\* Search** | Find optimal transportation routes efficiently by combining actual path cost $g(n)$ and heuristic estimation $h(n)$. |
| **Branch and Bound** | Reduce the allocation search space by eliminating unpromising options based on cost/priority bounds. |

---

## Project Goals

- **Feasible Matching:** Identify medically compatible and time-viable donor-recipient pairs.
- **Route Optimization:** Minimize organ delivery time and transportation cost while respecting preservation limits.
- **Performance Benchmarking:** Compare the implemented AI search algorithms in terms of solution optimality, execution time, and expanded search nodes.

---

## 🗂️ Planned Project Structure

```text
├── src/
│   ├── matching/        # BFS, DFS, Backtracking, and Branch & Bound allocation logic
│   ├── routing/         # UCS and A* hospital graph pathfinding
│   └── simulation/      # Constraints validation, synthetic data loader, and benchmarking
├── data/                # Synthetic datasets (hospitals graph, donors, recipients, organ viability rules)
├── docs/                # Problem formulation, state-space diagrams, and experimental results
├── .gitignore
└── README.md
