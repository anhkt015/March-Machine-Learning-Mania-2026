# March-Machine-Learning-Mania-2026
March Machine Learning Mania 2026 competition on kaggle 
📌 Overview

This project is my participation in the Kaggle competition March Machine Learning Mania 2026, where the goal is to predict outcomes of NCAA basketball tournament games.

🎯 Objective

Predict the probability of one team beating another

Optimize model performance based on log loss (Kaggle metric)

📂 Dataset

Historical NCAA game results

Team statistics and rankings

Tournament seed information

⚙️ Approach
1. Data Processing

Merged multiple datasets (regular season + tournament data)

Created matchup-based dataset (Team A vs Team B)

2. Feature Engineering

Team performance statistics (win rate)

Seed difference

Historical head-to-head features

3. Model

### 🤖 Model

The final prediction (`final_proba`) is an ensemble of two Logistic Regression models trained on different time periods:

- Model 1: trained on historical data from 2023–2024 seasons  
- Model 2: trained on more recent data from the 2025 season  

The intuition behind this approach is to balance:
- long-term team performance (historical stability)
- short-term form (recent performance)

The final probability is computed using weighted averaging:

final_proba = w1 * proba_model_2023_2024 + w2 * proba_model_2025

This helps the model better capture current team strength while still leveraging historical patterns.

4. Validation Strategy

Time-based split (important for sports prediction)

K-fold cross-validation

📈 Results

Public Leaderboard: xxx

Private Leaderboard: xxx

Final Rank: 3099

🧠 Key Learnings

Feature engineering plays a crucial role in sports prediction

Simple models can perform competitively with good features

Validation strategy significantly affects leaderboard performance

🔗 Links

Kaggle Notebook: https://www.kaggle.com/code/hackertrip/b-ng-r-pro/edit

Competition: https://www.kaggle.com/competitions/march-machine-learning-mania-2026

🚀 Future Improvements

Try ensemble models

Hyperparameter tuning
