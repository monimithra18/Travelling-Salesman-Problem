# TSP Genetic Algorithm

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

Solving the classic **Travelling Salesman Problem (TSP)** using a Genetic Algorithm. The algorithm evolves a population of routes over generations — using selection, crossover, and mutation — to find the shortest possible path that visits all cities exactly once.

---

## 🧬 Overview

The Travelling Salesman Problem is a well-known NP-hard combinatorial optimisation problem: given N cities, find the shortest route that visits each city exactly once and returns to the origin. This project uses a **Genetic Algorithm (GA)** — a population-based metaheuristic inspired by natural evolution — to approximate the optimal solution.

---

## 🗂 Project Structure

```
tsp-genetic-algorithm/
├── TSP.ipynb       # Full implementation — GA, visualisation, and results
└── README.md
```

---

## 🛠 Tech Stack

- **Python** — Core language
- **NumPy** — Distance calculations and array operations
- **Matplotlib** — Route visualisation and convergence plots
- **Jupyter Notebook** — Interactive development

---

## ⚙️ Algorithm

The Genetic Algorithm follows this pipeline:

### 1. Initialisation
Generate a random initial population of routes (chromosomes), where each route is a permutation of all cities.

### 2. Fitness Evaluation
Rank each route by its total distance — shorter routes have higher fitness.

### 3. Selection
Select parent routes using rank-based selection, giving higher-fitness routes a better chance of reproducing.

### 4. Crossover (Ordered Crossover)
Combine two parent routes to produce offspring, preserving the order of cities from each parent.

### 5. Mutation
Randomly swap two cities in a route to avoid local optima and maintain genetic diversity.

### 6. New Generation
Replace the old population with offspring and repeat from step 2.

### 7. Convergence
Return the best route found after a fixed number of generations.

---

## 🔑 Key Methods

| Method | Description |
|---|---|
| `Population()` | Creates the initial population of random routes |
| `Fitness()` | Ranks each individual by total route distance |
| `Selection()` | Returns a list of parent route IDs for reproduction |
| `Breed()` | Fills the next generation via ordered crossover |
| `Mutate()` | Introduces novel routes by swapping random city pairs |
| `NextGeneration()` | Combines selection, breeding, and mutation into one generation step |
| `GeneticAlgorithm()` | Runs the full GA and returns the best route |
| `Plot()` | Visualises the best route and convergence curve |

---

## 🚀 Getting Started

```bash
# Clone the repo
git clone https://github.com/monimithra18/tsp-genetic-algorithm.git
cd tsp-genetic-algorithm

# Install dependencies
pip install numpy matplotlib jupyter

# Launch the notebook
jupyter notebook TSP.ipynb
```

---

## 📈 Results

The GA consistently finds near-optimal routes within a few hundred generations. The convergence plot shows the best route distance decreasing over generations as the algorithm evolves.

---

## 🔭 Future Improvements

- Add 2-opt local search for post-GA refinement
- Experiment with adaptive mutation rates
- Compare against Simulated Annealing and Ant Colony Optimisation
- Scale to larger city sets (100+ cities)

---

*Built by [Monish Mithra Kadiyala](https://linkedin.com/in/monishmithra) ·*
