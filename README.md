# Team Battle AI Simulator

This repository presents a modular and scalable framework for simulating competitive team-based battles and training a machine learning model to predict outcomes based on team composition. The simulation draws inspiration from creature-based strategy games, employing role-based team generation, structured combat simulations, and supervised learning techniques.

## 🔍 Key Features

- **Strategic Role-Based Team Generation**  
  Creatures are categorized into functional roles such as Tank, Sweeper, and Balanced based on their statistical profiles.

- **High-Volume Battle Simulation**  
  Simulates 100,000+ 6v6 battles using probabilistic turn-based logic to generate labeled training data.

- **Neural Network Predictor**  
  A PyTorch-based feedforward neural network is trained to classify match outcomes with vectorized team inputs.

- **Interactive User-AI Interface**  
  Allows real-time team entry, model-based battle outcome prediction, and live turn-by-turn simulation.

- **Adaptive Learning Loop**  
  Continuously retrains the model using newly logged battle data, increasing AI difficulty over time.

## 🛠️ Setup Instructions

1. **Install Python Dependencies**
```bash
pip install pandas numpy torch scikit-learn tqdm
```

2. **Prepare Input Data**
Ensure the following data files are placed correctly:
- `creature_with_4_moves.npy` → `D:/adc/`
- CSVs (`creature.csv`, `moves.csv`, `stats.csv`, etc.) → `D:/idm downloads/data/csv/`

3. **Run the Jupyter Notebook**
Open and execute:
- `team_battle_ai.ipynb`

## 📊 Applications

- Research on AI strategy generation and classification models
- Simulated environments for performance benchmarking of predictive models
- Educational demonstrations of real-time ML feedback loops

## 🧠 Technologies Used

- Python, NumPy, pandas
- PyTorch for deep learning
- Scikit-learn for data preprocessing
- Jupyter for interactive development

## 📁 Structure

```
team_battle_ai.ipynb     # Main notebook with full pipeline
README.md                # Project overview and instructions
```

## 🧑‍🔬 Authorship

Developed for educational and experimental purposes. The framework can be extended to support more realistic physics, external APIs, or competitive strategy games.

---

© 2025 Team Battle AI Research
