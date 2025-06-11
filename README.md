# Team-Based Battle Simulation and Predictive Modeling

This repository presents a structured framework for simulating competitive 6-versus-6 team battles and constructing a predictive machine learning model to estimate battle outcomes. The system integrates role-based team composition, probabilistic combat simulation, and iterative model training using PyTorch.

## Overview

The project is designed for applications in:
- Synthetic data generation for classification tasks
- AI behavior modeling in turn-based competitive environments
- Adaptive systems that evolve via real-time feedback

## Core Capabilities

- **Strategic Team Generation**  
  Classifies entities into predefined roles (Tank, Sweeper, Balanced) based on statistical heuristics.

- **Battle Simulation Engine**  
  Executes high-volume (100,000+) team battle simulations using stochastic turn-based logic to yield labeled outcome data.

- **Machine Learning Architecture**  
  Implements a supervised learning model (multi-layer perceptron) to predict battle outcomes from team configurations.

- **Interactive Interface**  
  Allows human users to input teams, evaluate predicted outcomes, simulate turn-by-turn interactions, and update the dataset.

- **Continuous Learning Loop**  
  Automatically retrains the model with newly logged data to improve generalization and AI performance over time.

## Requirements

Install dependencies:
```bash
pip install pandas numpy torch scikit-learn tqdm
```

## File Placement

Ensure the following directory structure:

```
D:/adc/
 ├─ creature_with_4_moves.npy
 └─ team_battle_results.csv

D:/idm downloads/data/csv/
 ├─ moves.csv
 ├─ stats.csv
 ├─ pokemon.csv
 └─ pokemon_stats.csv
```

## Execution

Run the notebook `team_battle_ai.ipynb` in a Jupyter environment to initiate simulation, training, or interactive inference.

## Licensing

This project is intended for educational, research, and non-commercial use.

© 2025. All rights reserved.
