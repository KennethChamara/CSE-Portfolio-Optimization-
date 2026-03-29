# Portfolio Optimization: Exact vs. Metaheuristic Approaches

## Problem

**Cardinality-Constrained Portfolio Optimization:** Given N assets, select at most K and allocate weights to maximize the Sharpe Ratio, subject to minimum/maximum position size constraints.

This is an NP-hard combinatorial optimization problem (the cardinality constraint introduces binary variables into the classic Markowitz model).

## Methods

| Method | Type | Guarantee | Scalability |
|--------|------|-----------|-------------|
| **Branch & Bound** | Exact | Global optimum | Exponential (practical for N≤30) |
| **Genetic Algorithm** | Metaheuristic | Near-optimal | Polynomial (scales to N=500+) |

## Project Structure

```
├── portfolio_optimization.ipynb   # Main notebook (all code + analysis)
├── members.txt                     # Team members
├── submission.txt                  # Dataset + links
├── report.pdf                      # PDF report
└── README.md                       # This file
```

## How to Run

```bash
pip install numpy pandas matplotlib scipy seaborn
jupyter notebook portfolio_optimization.ipynb
```

Run all cells sequentially. No API keys or external data downloads required.

## Dataset

Synthetic universe of 30 assets across 7 sectors, calibrated to real S&P 500 sector characteristics (returns, volatilities, correlations). See Section 3 of the notebook for details and justification.

## Key Results

- Branch & Bound finds the provably optimal portfolio
- Genetic Algorithm achieves near-optimal solutions (~1-3% gap) in a fraction of the time
- B&B runtime grows exponentially; GA scales linearly with problem size

## Dependencies

- Python 3.8+
- NumPy, Pandas, Matplotlib, SciPy, Seaborn

## Team

- Student 1: [Name] — Problem formulation, B&B implementation, report
- Student 2: [Name] — GA implementation, scalability experiments, video
