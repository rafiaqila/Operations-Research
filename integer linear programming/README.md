# Optimization of Capacity Allocation in Semiconductor Manufacturing

This repository contains MATLAB code that supports the research paper titled "Optimization of Capacity Allocation Using Integer Linear Programming in a Semiconductor Manufacturing Company," authored by Rafi Aqila Hidayat and Kuan Yew Wong, presented at ICMLSC 2025.

## Abstract
The research focuses on optimizing capacity allocation in the photolithography area of semiconductor manufacturing using Integer Linear Programming (ILP). The primary goal is to enhance machine utilization rates and balance workloads across various machines while satisfying the wafer demand for each machine and recipe.

## Research Highlights
- Development of an ILP model to optimize capacity allocation in semiconductor manufacturing.
- The model significantly improved machine utilization from 88.87% to 69.46%.
- Reduction in the Mean Absolute Deviation (MAD) from 43.23 to 0.003, indicating a more balanced workload.

## Integer Linear Programming Model
The ILP model aims to minimize the maximum machine utilization rates while ensuring the total workload is evenly distributed across all machines without exceeding their capacities.

### Objective Function:
Minimize \( Z = \max(\sum U_{1j}, \sum U_{2j}, \ldots, \sum U_{nj}) \)

Where \( U_{ij} \) represents the utilization of machine \( i \) for recipe \( j \).

### Constraints:
- **Capacity Constraint:** Ensures that no machine's utilization exceeds 100%.
  \[ \sum U_{ij} \leq 100\%, \forall i \]

- **Demand Constraint:** Ensures the total wafer allocations for each recipe meet the demand.
  \[ \sum x_{ij} = D_j, \forall j \]

- **Process Capability Constraint:** Indicates whether a machine is capable of processing a specific recipe.
  \[ mpc_{ij} = \{0, 1\} \]

- **Integer and Non-Negativity Constraints:** Decision variables should be non-negative integers.
  \[ x_{ij} \geq 0, x_{ij} \in \mathbb{Z}^+, \forall i, j \]

## Repository Contents
- `capacity allocation optimization.m`: Main MATLAB script that implements the ILP model for optimizing the allocation of machine capacity in semiconductor manufacturing.

## Contact
- Rafi Aqila Hidayat - [email](mailto:rafi.hidayat@graduate.utm.my)
- Kuan Yew Wong - [Google Scholar Profile](https://scholar.google.com/citations?user=8Hm4IsYAAAAJ&hl=en&oi=ao)
