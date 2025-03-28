# ME5413 Homework 3: Path Planning

This repository contains the implementation and results for **ME5413 Homework 3**, which focuses on path planning algorithms. The tasks involve implementing and comparing various path planning algorithms, computing optimal routes, and visualizing the results on a given map.

---

## Table of Contents
1. Overview
2. Requirements
3. Tasks
4. Results
5. How to Run
6. References

---

## Overview

The goal of this homework is to explore and implement path planning algorithms, including:
- **A\*** with different heuristics (Euclidean and Manhattan distances).
- **Greedy Best-First Search** with different heuristics.
- **Traveling Salesman Problem (TSP)** solutions using exhaustive search and the Held-Karp algorithm.

The provided map represents a floor plan of a shopping mall, with designated locations such as `start`, `snacks`, `store`, `movie`, and `food`. The task is to compute paths between these locations while avoiding obstacles.

---

## Requirements

The project requires the following dependencies:
- Python 3.8+
- Libraries:
  - `numpy`
  - `matplotlib`
  - `imageio`
  - `heapq` (standard library)
  - `time` (standard library)
  - `pandas`
  - `itertools` (standard library)

Install the required libraries using:
```bash
pip install numpy matplotlib imageio pandas
```

---

## Tasks

### Task 0: Load the Map
- Load the map and visualize the free and occupied cells.
- Mark the designated locations (`start`, `snacks`, `store`, `movie`, `food`) on the map.

### Task 1: Path Planning Algorithms
#### Task 1.1: A* Algorithm
- Implement the **A\*** algorithm with:
  - **Euclidean heuristic**
  - **Manhattan heuristic**
- Compute the shortest path between each location.

#### Task 1.2: Comparison of A* and Greedy Best-First Search
- Implement **Greedy Best-First Search** with:
  - **Euclidean heuristic**
  - **Manhattan heuristic**
- Compare the performance of A* and Greedy Best-First Search in terms of:
  - Path distance
  - Runtime
  - Number of visited cells

### Task 2: Optimal Route for TSP
- Compute the shortest route visiting all locations (`start`, `snacks`, `store`, `movie`, `food`) and returning to the start.
- Implement two methods:
  1. **Exhaustive Search** (Brute Force)
  2. **Held-Karp Algorithm** (Dynamic Programming)

---

## Results

### Task 1: Path Planning
- **A\*** with Euclidean heuristic produced the shortest path with fewer visited cells compared to Manhattan heuristic.
- **Greedy Best-First Search** was faster but less optimal in terms of path distance.

#### Comparison Table:
| Algorithm                          | Distance (m) | Runtime (s) | Visited Cells |
|------------------------------------|--------------|-------------|---------------|
| A* (Euclidean)                     | 236.04       | 0.22        | 5966          |
| A* (Manhattan)                     | 249.44       | 0.38        | 14172         |
| Greedy Best-First (Euclidean)      | 204.80       | 0.47        | 3842          |
| Greedy Best-First (Manhattan)      | 217.80       | 0.51        | 9513          |

### Task 2: Optimal Route for TSP
- **Exhaustive Search** and **Held-Karp Algorithm** produced the same optimal route:
  ```
  start → store → food → movie → snacks → start
  ```
- **Total Distance**: 656.30 m

---

## How to Run

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd ME5413_HW3
   ```

2. Ensure the required dependencies are installed:
   ```bash
   pip install numpy matplotlib imageio pandas
   ```

3. Run the Jupyter Notebook:
   ```bash
   jupyter notebook homework3.ipynb
   ```

4. Follow the notebook cells to execute the tasks and visualize the results.

---

## References

- **A\*** Algorithm: Hart, P. E., Nilsson, N. J., & Raphael, B. (1968). A formal basis for the heuristic determination of minimum cost paths.
- **Held-Karp Algorithm**: Held, M., & Karp, R. M. (1962). A dynamic programming approach to sequencing problems.

--- 

**Note**: The results and visualizations are included in the notebook and can be reproduced by running the code.