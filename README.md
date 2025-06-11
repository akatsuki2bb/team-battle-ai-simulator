# Team Battle AI Simulator

This project provides a machine learning-powered simulation of strategic 6v6 team battles, where outcomes are predicted based on team composition. It includes structured data generation, a neural network classifier, and a real-time interactive prediction loop.

## Features

- Role-based team formation (Tank, Sweeper, Balanced)
- Large-scale battle simulation to generate training data
- PyTorch-based outcome prediction model
- Adaptive AI opponent that improves over time
- Interactive user vs AI match interface

## Setup Instructions

1. **Install dependencies**:
```bash
pip install pandas numpy torch scikit-learn tqdm
```

2. **Prepare required data**:
- `creature_with_4_moves.npy` → Place in `D:/adc/`
- `*.csv` files (moves, stats, etc.) → Place in `D:/idm downloads/data/csv/`

3. **Run the Notebook**:
Open and execute `team_battle_ai.ipynb` in Jupyter.

## Author

Built for applied AI research in game simulation and predictive modeling. Open for extension into advanced strategy or educational use cases.
