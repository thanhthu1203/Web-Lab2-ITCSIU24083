
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

This project implements an **Intelligent Vacuum Cleaner Agent** operating in a **grid-based simulation environment**.

The agent is capable of:
- Exploring unknown space
- Detecting and cleaning dirt
- Avoiding obstacles (walls)
- Returning to home position after task completion
- Using classical AI search algorithms (BFS, DFS, A*)

A **Tkinter-based GUI** is used for real-time visualization of the environment.

---

# 🎯 2. OBJECTIVES

The main objectives of this lab are:

- Understand **agent-based AI systems**
- Implement **state-space search algorithms**
- Apply:
  - Breadth-First Search (BFS)
  - Depth-First Search (DFS)
  - A* Search
- Simulate perception–action loop
- Visualize AI behavior using GUI

---

# 🧠 3. SEARCH ALGORITHMS

## 📍 BFS (Breadth-First Search)
- Level-by-level exploration
- Guarantees shortest path in unweighted grid
- Uses FIFO queue

## 📍 DFS (Depth-First Search)
- Deep exploration first
- Uses LIFO stack
- Memory efficient but not optimal

## 📍 A* Search
- Combines cost + heuristic
- Faster than BFS in large environments

---

# 🏠 4. SYSTEM ARCHITECTURE

## 🧩 Components

### 📌 Environment (`vacuum.py`)
- Grid world representation
- Handles:
- Dirt
- Walls
- Agent movement
- Percepts (bump, dirt, home)

---

### 📌 Agent (`myvacuumagent.py`)
- AI decision-making unit
- Maintains internal world state
- Implements:
- BFS
- DFS
- A*
- Controls movement and cleaning actions

---

### 📌 GUI (`Lab2 class`)
- Built using Tkinter
- Displays:
- Grid map
- Agent position
- Direction
- Logs
- Provides controls:
- Start / Stop / Step execution

---

# 🖥 5. USER INTERFACE

## 🎮 Controls
- ▶ Start Simulation
- ⏹ Stop Simulation
- 👣 Step Execution
- 🧹 Clear Log

## 🎨 Grid Colors
| Element | Color |
|--------|--------|
| Clean | White |
| Dirty | Gray |
| Wall | Black |
| Home | Blue |

---

# 📊 6. PERFORMANCE METRICS

The system tracks:

- Number of steps
- Nodes expanded during search
- Final score
- Algorithm efficiency

---

# 📌 Example Output

```text
========== RESULT ==========
Algorithm: BFS
Grid: 5x5
Steps: 53
Nodes explored: 96
Score: -62
Optimal: YES
============================
⚙️ 7. COMPILE & RUN (PYTHON PROJECT)
📌 Prerequisites
Python 3.8+ installed
PyCharm 2025.2.4 (optional)
Project root contains:
lab2/
run_lab2.py
💻 Command-line (Recommended)
📍 Step 1: Open terminal in project root

Make sure you are inside the folder containing:

lab2/
run_lab2.py
📍 Step 2: Create virtual environment
python3 -m venv .venv
📍 Step 3: Activate virtual environment
macOS / Linux:
source .venv/bin/activate
Windows:
.venv\Scripts\activate
📍 Step 4: Run the application
python3 run_lab2.py
🖥️ PyCharm (Optional)
Open project in PyCharm
Set Python interpreter to .venv or Python 3.8+
Open run_lab2.py
Click Run
📁 8. PROJECT STRUCTURE
.
├── lab2/
│   ├── vacuum.py              # Core Environment & GUI engine
│   ├── myvacuumagent.py       # AI agent (BFS / DFS / A*)
│   ├── reactivevacuumagent.py # Simple reflex agent
│   ├── randomvacuumagent.py   # Random movement agent
│   └── utils.py               # Helper utilities
│
└── run_lab2.py                # Main entry point
🚀 9. CONCLUSION

This project demonstrates:

Implementation of classical AI search algorithms
Intelligent agent behavior in a dynamic environment
Integration of AI logic with GUI visualization
Performance evaluation using measurable metrics

The vacuum agent successfully performs exploration, cleaning, and return-home behavior using BFS, DFS, and A* algorithms.
- Formula:
