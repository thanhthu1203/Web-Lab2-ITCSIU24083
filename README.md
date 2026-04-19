Compile & Run (Python project)
Prerequisites
Python 3.8+ installed
PyCharm 2025.2.4 (optional)
Project root contains the package directory lab1 (e.g. Lab1/lab1)
Command-line (recommended)
Open a terminal in the project root (the folder that contains lab1).

Create and activate a virtual environment:

python3 -m venv .venv  
source .venv/bin/activate
Run the application
//must direct to the folder lab1
python3 run_lab1.py
.
├── lab2/
│   ├── vacuum.py              # Core Environment & GUI engine
│   ├── myvacuumagent.py       # Main AI implementation (BFS/DFS/A*)
│   ├── reactivevacuumagent.py # Simple reflex agent (No memory)
│   ├── randomvacuumagent.py   # Stochastic agent (Random movement)
│   └── utils.py               # Helper data structures (Queue, PriorityQueue)
└── run_lab2.py                # Main entry point to launch the GUI

# 🧠 Computer Architecture – Lab 2  
## Vacuum Environment AI Simulation

---

# 🇻🇳 VIETNAM NATIONAL UNIVERSITY – HO CHI MINH CITY  
## 🏫 INTERNATIONAL UNIVERSITY  

---

## 📘 Course Information
- **Course:** Computer Architecture  
- **Instructor:** Ly Tu Nga  
- **Lab:** Lab 2 – Intelligent Vacuum Agent Simulation  

---

## 👤 Student Information
- **Full Name:** Phạm Thanh Thư  
- **Student ID:** ITCSIU24083  
- **Date Submitted:** 11/04/2026  

---

# 🤖 1. PROJECT OVERVIEW

This project implements an **Intelligent Vacuum Cleaner Agent** operating in a **grid-based simulated environment**.

The agent is capable of:
- Exploring unknown space
- Detecting and cleaning dirt
- Avoiding obstacles (walls)
- Returning to the home position after task completion
- Using classical AI search algorithms

The simulation includes a **Tkinter GUI interface** for real-time visualization.

---

# 🎯 2. OBJECTIVES

The main objectives of this lab are:

- Understand **agent-based AI systems**
- Implement **state-space search algorithms**
- Apply:
  - BFS (Breadth-First Search)
  - DFS (Depth-First Search)
  - A* Search
- Simulate perception-action loop in AI
- Visualize environment using GUI

---

# 🧠 3. SEARCH ALGORITHMS

## 📍 3.1 Breadth-First Search (BFS)
- Explores level by level
- Guarantees shortest path in unweighted grid
- Uses queue (FIFO)

## 📍 3.2 Depth-First Search (DFS)
- Explores deep paths first
- Uses stack (LIFO)
- Not optimal but memory efficient

## 📍 3.3 A* Search
- Uses heuristic + cost function
- Faster pathfinding than BFS in large grids
- Formula:
  - f(n) = g(n) + h(n)

---

# 🏠 4. SYSTEM ARCHITECTURE

## 🧩 Components

### 1. Environment (`vacuum.py`)
- Grid world representation
- Handles:
  - Dirt
  - Walls
  - Agent movement
  - Percepts (bump, dirt, home)

---

### 2. Agent (`myvacuumagent.py`)
- AI decision-making unit
- Maintains internal world state
- Implements:
  - BFS
  - DFS
  - A*
- Controls movement + cleaning

---

### 3. GUI (`Lab2 class`)
- Built with Tkinter
- Displays:
  - Grid map
  - Agent position
  - Direction
  - Logs
  - Controls (Start / Stop / Step)

---

# 🖥 5. USER INTERFACE

## Controls:
- ▶ Start Simulation
- ⏹ Stop Simulation
- 👣 Step-by-step execution
- 🧹 Clear log

## Grid Colors:
| Element | Color |
|----------|--------|
| Clean | White |
| Dirty | Gray |
| Wall | Black |
| Home | Blue |

---

# 📊 6. PERFORMANCE METRICS

The system tracks:

- Number of steps
- Nodes expanded
- Final score
- Algorithm efficiency

---

## 📌 Example Output

```text
========== RESULT ==========
Algorithm: BFS
Grid: 5x5
Steps: 53
Nodes explored: 96
Score: -62
Optimal: YES
============================
