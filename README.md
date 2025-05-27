# Optimal Markdown Strategy for Retail Revenue Management

_A comprehensive simulation framework evaluating fixed and adaptive markdown schedules to optimize revenue under demand uncertainty._

## Table of Contents

1. [Description](#description)  
2. [Key Features](#key-features)  
3. [Tech Stack](#tech-stack)  
4. [Installation](#installation)  
5. [Usage](#usage)  
6. [Project Structure](#project-structure)  
7. [Configuration](#configuration)

---

## Description

This project simulates a 15-week retail selling season under 100,000 demand scenarios to compare five markdown strategies: Early Aggressive, Original Pattern (baseline), Moderate, Late Conservative, and a novel Adaptive Strategy driven by early-season demand signals. It quantifies performance using revenue gaps, success rates, variability, and inventory depletion patterns.

## Key Features

- **Fixed Strategies**: Implements heuristic markdown schedules (weeks 2→7→14, 4→8→15, 5→9→15, 8→12→15).  
- **Adaptive Strategy**: Bayesian decision rule with thresholds (≤85, 86–95, 96–105, >105 units) to select markdown timing based on weeks 1–3 sales.  
- **Performance Metrics**: Perfect Foresight Revenue, Performance Gap, Success Rate (%), and Variability (Std Dev).  
- **Simulation Framework**: 100,000 independent demand curve realizations with reproducible seeds.  
- **Visualization**: Comparison charts, heatmaps by demand level, depletion curves, and time-based performance phases.

## Tech Stack

- **Language:** Python 3.8+  
- **Notebook:** Jupyter Notebook (`Group_Assignment_1.ipynb`)  
- **Libraries:** pandas, numpy, matplotlib, seaborn

## Installation

```bash
git clone https://github.com/your-username/mgsc670-markdown-strategy.git
cd mgsc670-markdown-strategy
python -m venv venv
source venv/bin/activate   # macOS/Linux
venv\Scripts\activate    # Windows
pip install -r requirements.txt
```

## Usage

1. **Open the analysis notebook**:  
   ```bash
   jupyter notebook Group_Assignment_1.ipynb
   ```  
2. **Run cells in sequence**:  
   - Demand generation and perfect foresight  
   - Implementation of each markdown strategy  
   - Calculation of performance metrics  
   - Visualization of results  
3. **Review the PDF report** (`MGSC 670_Group Assignment 1.pdf`) for detailed findings and executive summary.

## Project Structure

```
mgsc670-markdown-strategy/
├── README_MGSC670.md            # This file
├── requirements.txt             # Python dependencies
├── data/                        # (optional) any input files
├── Group_Assignment_1.ipynb     # Simulation and analysis notebook
├── MGSC 670_Group Assignment 1.pdf  # Project report
└── figures/                     # Generated plots (if saved)
```

## Configuration

- **Simulation Count**: Modify `n_simulations` in the notebook (default 100000).  
- **Adaptive Thresholds**: Adjust early-demand breakpoints in decision logic.  
- **Markdown Levels**: Change price levels and weeks in strategy definitions as needed.  
