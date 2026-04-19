# 🧠 Computer Architecture – Lab 3
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
- Understand agent-based AI systems
- Implement state-space search algorithms
- Apply BFS, DFS, and A* Search
- Simulate perception–action loop
- Visualize AI behavior using GUI

---

# 🧠 3. SEARCH ALGORITHMS

## BFS (Breadth-First Search)
- Level-by-level exploration  
- Guarantees shortest path in unweighted grid  
- Uses FIFO queue  

## DFS (Depth-First Search)
- Deep exploration first  
- Uses LIFO stack  
- Memory efficient but not optimal  

## A* Search
- Combines path cost and heuristic  
- Faster than BFS in large environments  

Formula:
f(n) = g(n) + h(n)

---

# 🏠 4. SYSTEM ARCHITECTURE

## Environment (vacuum.py)
- Grid world representation  
- Handles dirt, walls, agent movement  
- Provides percepts (bump, dirt, home)  

## Agent (myvacuumagent.py)
- Maintains internal world state  
- Implements BFS / DFS / A*  
- Controls movement and cleaning  

## GUI (Lab2 class)
- Built using Tkinter  
- Displays grid, agent, direction, logs  
- Provides Start / Stop / Step controls  

---

# 🖥 5. USER INTERFACE

## Controls
- Start Simulation  
- Stop Simulation  
- Step Execution  
- Clear Log  

## Grid Colors
- Clean: White  
- Dirty: Gray  
- Wall: Black  
- Home: Blue  

---

# 📊 6. PERFORMANCE METRICS

The system tracks:
- Number of steps  
- Nodes expanded  
- Final score  
- Algorithm efficiency  

---

# ⚙️ 7. COMPILE & RUN (PYTHON PROJECT)

## Prerequisites
- Python 3.8+ installed  
- PyCharm 2025.2.4 (optional)  
- Project root contains:

lab2/  
run_lab2.py  

---

## Command-line Execution (Recommended)

Open terminal in project root (folder containing lab2 and run_lab2.py).

Create virtual environment:

python3 -m venv .venv  
source .venv/bin/activate  

Run application:

python3 run_lab2.py  

---

## PyCharm Execution (Optional)
- Open project in PyCharm  
- Set interpreter to Python 3.8+ or .venv  
- Open run_lab2.py  
- Click Run  

---

# 📁 8. PROJECT STRUCTURE

.
├── lab2/
│   ├── vacuum.py              # Core environment + GUI engine
│   ├── myvacuumagent.py       # AI agent (BFS / DFS / A*)
│   ├── reactivevacuumagent.py # Reflex-based agent (no memory)
│   ├── randomvacuumagent.py   # Random movement agent
│   └── utils.py               # Helper data structures
│
└── run_lab2.py                # Main entry point

---

# 🚀 9. CONCLUSION

This project demonstrates an intelligent vacuum agent operating in a grid-based environment using classical AI search algorithms.

The agent is capable of:
- Autonomous exploration  
- Dirt detection and cleaning  
- Obstacle avoidance  
- Returning to home position  

The system successfully implements BFS, DFS, and A* search strategies and evaluates performance using steps, nodes expanded, and final score.

Overall, this project demonstrates effective application of AI search techniques with real-time visualization using Tkinter GUI.
