# 0-1-Knapsack-Problem
Evolutionary algorithm for the 0/1 Knapsack Problem using a repair-based direct binary representation, evaluated on low-dimensional benchmark instances.

# Evolutionary Algorithm for the 0/1 Knapsack Problem

This repository contains a Jupyter notebook that implements an evolutionary algorithm for the 0/1 Knapsack Problem using a **repair-based direct approach**.

Each solution is represented directly as a binary vector, where each gene indicates whether an item is selected or not. Since the knapsack has a capacity constraint, infeasible individuals are repaired after initialization, crossover, and mutation by removing selected items until the total weight fits within the allowed capacity.

## Approach

This notebook uses a **direct representation**:

```text
binary vector -> selected items -> total value and total weight
