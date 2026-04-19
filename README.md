
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

**# ⚙️ 7. COMPILE & RUN (PYTHON PROJECT)
**
---

## 📌 Prerequisites

Before running the project, ensure the following requirements are met:

- Python **3.8+** installed
- PyCharm **2025.2.4** (optional)
- Project root contains the following structure:

---

## 💻 Command-line Execution (Recommended)

### 📍 Step 1: Open Terminal in Project Root

Navigate to the folder containing:

---

### 📍 Step 2: Create Virtual Environment

```bash
python3 -m venv .venv
source .venv/bin/activate
.venv\Scripts\activate
python3 run_lab2.py
run_lab2.py
.
├── lab2/
│   ├── vacuum.py              # Core Environment & GUI engine
│   ├── myvacuumagent.py       # AI agent (BFS / DFS / A*)
│   ├── reactivevacuumagent.py # Reflex-based agent (no memory)
│   ├── randomvacuumagent.py   # Stochastic agent (random movement)
│   └── utils.py               # Helper utilities and data structures
│
└── run_lab2.py                # Main entry point of the system
