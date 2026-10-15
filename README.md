# Error Budget Optimization for Fault-Tolerant Quantum Computing

This project explores **resource-efficient error budget allocation** in fault-tolerant quantum computing (FTQC) using game-theoretic and metaheuristic optimization techniques. The objective is to minimize **physical qubit requirements and execution runtime** by optimizing the distribution of a fixed error budget across logical errors, T-state distillation, and rotation synthesis.

The framework integrates **Microsoft Quantum Resource Estimator**, **Qiskit**, and **MQT Bench** for resource estimation and benchmark evaluation.

## Implemented Methods

| Method | Description |
|---|---|
| **Nash Equilibrium** | Game-theoretic optimization using iterated best response |
| **Simulated Annealing (SA)** | Adaptive stochastic optimization of error budgets |
| **Quantum Particle Swarm Optimization (QPSO)** | Population-based optimization of budget allocations |
| **Uniform Baseline** | Equal error budget allocation for comparison |

## Repository Contents

- [`error-budget-distribution-nash.ipynb`](./error-budget-distribution-nash.ipynb) — Nash-equilibrium-based optimization
- [`mqt-sa-analysis.ipynb`](./mqt-sa-analysis.ipynb) — Simulated annealing experiments
- [`mqt-qpso-analysis.ipynb`](./mqt-qpso-analysis.ipynb) — QPSO optimization and benchmarking
- [`error-budget-visualization.ipynb`](./error-budget-visualization.ipynb) — Results visualization and analysis

## Experimental Workflow

1. Generate quantum circuits using **MQT Bench** and transpile with **Qiskit**.
2. Optimize error budgets across logical, T-state, and rotation errors.
3. Estimate physical qubits and runtime using the **Microsoft Quantum Resource Estimator**.
4. Evaluate **space-time overhead (qubits × runtime)** against uniform allocation.

Experiments cover QFT, QPE, Grover, QAOA, VQE, quantum arithmetic, and other MQT benchmarks.

## Setup & Execution

**Dependencies:** Python 3, Jupyter/Google Colab, .NET SDK 8.0, Qiskit, MQT Bench, Q#, NumPy, SciPy, and Pandas.

```bash
pip install qiskit mqt.bench qsharp azure-quantum numpy scipy pandas
```

Run the notebooks in Jupyter or Google Colab, following their environment setup cells. The default total error budget is `0.1`. Experimental results are exported as CSV files for comparative analysis.
