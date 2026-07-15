# Evolutionary Algorithm for the 0/1 Knapsack Problem

This repository contains a Jupyter notebook that implements an evolutionary algorithm for the 0/1 Knapsack Problem using a **repair-based direct approach**.

Each solution is represented directly as a binary vector, where each gene indicates whether an item is selected or not. Since the knapsack has a capacity constraint, infeasible individuals are repaired after initialization, crossover, and mutation by removing selected items until the total weight fits within the allowed capacity.

## Approach

This notebook uses a **direct representation**:

binary vector -> selected items -> total value and total weight

Each gene corresponds directly to one item:

1 = item selected  
0 = item not selected

The constraint-handling strategy is repair-based. If a solution exceeds the knapsack capacity, the repair function removes selected items with the worst value-to-weight ratio first. This keeps evaluated individuals feasible while preserving as much value as possible.

## Features

- Implements an evolutionary algorithm for the 0/1 Knapsack Problem.
- Uses a direct binary representation.
- Applies a repair function for capacity violations.
- Uses binary tournament selection.
- Uses one-point crossover.
- Uses bit-flip mutation with probability 1/n.
- Includes elitism to preserve the best solution found.
- Evaluates performance on ten low-dimensional benchmark instances from Kaggle.
- Compares results against known optimal values.
- Reports best fitness, average population fitness, relative gap, hit rate, and runtime.
- Includes convergence plots and visual comparisons with known optima.

## Technologies

- Python
- NumPy
- pandas
- matplotlib
- Jupyter Notebook

## Purpose

This notebook is intended as an educational implementation of evolutionary optimization for a constrained combinatorial problem. It demonstrates how a direct binary representation can be combined with a repair mechanism to handle feasibility in the 0/1 Knapsack Problem.
