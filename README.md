# 🔬 Lab Space Optimizer

A group project that tackles the combinatorial problem of assigning university modules to computer labs efficiently. The solution evolves across three phases — from feasibility checking and greedy scheduling, to local search optimisation — minimising unused seats while respecting capacity and software constraints.

---

## 📋 Project Overview

Given a set of labs (each with a capacity and available software) and a set of modules (each with a student count and required software), the goal is to find the best possible assignment of modules to labs that:

- Satisfies software compatibility requirements
- Does not exceed lab capacity
- Minimises wasted (unused) seats across all assignments

---

## 🗂️ File Overview

| File | Description |
|------|-------------|
| `Lab Space Optimizer.ipynb` | Main notebook containing all three phases of the project |
| `Phase 1 Report.pdf` | Report covering problem modelling, data structures, and feasibility checking |
| `Phase 2 Report.pdf` | Report covering greedy algorithm design and comparison |
| `Phase 3 Report.pdf` | Report covering hill-climbing and swap search optimisation |

---

## 🔄 Project Phases

### Phase 1 — Problem Modelling & Feasibility
- Defines lab and module data as Pandas DataFrames
- Implements a feasibility check function (`check_fit`) to determine if a module can be assigned to a lab based on capacity and software availability
- Displays a compatibility matrix of modules vs. compatible labs

### Phase 2 — Greedy Algorithms
- Implements two greedy scheduling strategies:
  - **Largest Module First** — prioritises modules with the most students
  - **Smallest Lab First** — prioritises filling smaller labs first
- Compares both strategies by total unused seats and assignment quality

### Phase 3 — Local Search Optimisation
- Applies **Hill-Climbing** to iteratively improve the greedy solution
- Applies **Swap Search** to explore neighbour solutions by swapping module-lab assignments
- Compares all stages (Greedy → Hill Climb → Swap Search) across both strategies using bar charts

---

## 🚀 Running the Notebook

### Option 1: Google Colab (Recommended)

1. Go to [Google Colab](https://colab.research.google.com/)
2. Click **File → Upload notebook**
3. Upload `Lab_Space_Optimizer.ipynb`
4. Click **Runtime → Run all**

> No additional setup needed — all libraries used (`pandas`, `matplotlib`) are pre-installed in Colab.

---

### Option 2: Run Locally

**Prerequisites:** Python 3.8+ installed on your machine.

**Step 1 — Clone the repository:**
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

**Step 2 — Install dependencies:**
```bash
pip install pandas matplotlib notebook
```

**Step 3 — Launch Jupyter Notebook:**
```bash
jupyter notebook Lab_Space_Optimizer.ipynb
```

**Step 4 — Run the notebook:**
- Click **Kernel → Restart & Run All**

---

## 🛠️ Dependencies

| Library | Purpose |
|---------|---------|
| `pandas` | Data manipulation and DataFrames |
| `matplotlib` | Visualisation and bar charts |
| `numpy` | Numerical operations (Phase 3) |

---

## 👥 Contributors

This was a group project. Contributions spanned problem modelling, algorithm design, optimisation, and reporting across all three phases.
