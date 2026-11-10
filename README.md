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


---

## Play the 2.5D pixel-art browser battle

The repository now includes a standalone browser game at [`index.html`](index.html).
It preserves the spirit of the notebook's **6-versus-6 turn-based simulator**:
accuracy, type-effectiveness multipliers, STAB, a 10% critical-hit chance,
random damage variation, level-50 damage calculations, speed order, and Elo updates.

The interface adds:

- Animated Gen V-style Pokémon front/back sprites and a CSS perspective battlefield.
- Six-Pokémon teams, health bars, four attacks per Pokémon, and switching.
- A tactical CPU with 10 difficulty levels (stronger levels choose higher expected damage).
- Randomized team rematches, optional original 8-bit-style sound effects, keyboard shortcuts
  (keys 1–4), responsive mobile layout, and locally saved Elo ratings.

### Run locally

No Python, Node.js, npm install, or API key is needed for the browser demo.
Open [`index.html`](index.html) in a modern browser or serve it locally:

```bash
python -m http.server 8000
```

Then navigate to `http://localhost:8000`.

### Put it online using GitHub Pages

1. Merge the browser-game pull request into `main`.
2. Open the repository's **Settings → Pages**.
3. Under **Build and deployment**, choose **GitHub Actions** as the source.
4. Run the **Deploy pixel battle to GitHub Pages** workflow if it did not trigger automatically.
5. Once the deployment succeeds, the page should be available at
   **https://akatsuki2bb.github.io/team-battle-ai-simulator/**.

### Current demo boundaries

This is **2.5D**: layered scenery, perspective ground, sprite movement and combat effects;
it is not a 3D world or a real-time multiplayer server.

The notebook remains unchanged. Its local training data and the serialized XGBoost model
are **not committed in this repository**, so the web demo uses **illustrative, hard-coded
Pokémon stats** and a JavaScript tactical opponent. It does **not** run the trained
XGBoost prediction model or retrain it in the browser. For real model inference,
add a Python API (for example FastAPI) and host the model and compatible datasets separately.

Sprites are loaded from the public [PokéAPI Sprites](https://github.com/PokeAPI/sprites)
repository at runtime; an internet connection is required for the artwork.
Pokémon names and related character artwork are owned by their respective rights holders.
This fan-made demo is not affiliated with Nintendo, Game Freak, or The Pokémon Company.
