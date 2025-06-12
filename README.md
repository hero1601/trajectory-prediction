# 🚶‍♂️ Trajectory Prediction with AttentionSocialLSTM

This repository contains the implementation of trajectory prediction models, developed as part of **CSE 251B – Deep Learning** at **UC San Diego**.

The primary focus is on modeling and predicting the future positions of agents (e.g., pedestrians) using their past movement data and the influence of nearby agents. The key model used is **AttentionSocialLSTM**, which improves upon traditional sequence models by incorporating attention mechanisms for better spatial and temporal understanding. It also includes features like speed and acceleration to handle sudden stops for the ego agent.

---

## 📄 Project Description

The notebook `cse-251b-trajectory.ipynb` implements a complete pipeline for trajectory prediction. It includes:
- Loading and preprocessing trajectory datasets
- Implementing multiple models, including:
  - Linear Baseline (constant velocity)
  - Social LSTM
  - **Attention Social LSTM**
- Visualizations of predicted vs. ground truth trajectories

---

## 🧠 Models Overview

| Model               | Social Awareness | Temporal Modeling | Attention Mechanism | Learning Type |
|--------------------|------------------|-------------------|---------------------|----------------|
| Linear Baseline     | ❌               | ❌                | ❌                  | Heuristic      |
| Social LSTM         | ✅ (via pooling) | ✅ (LSTM)          | ❌                  | Supervised     |
| **AttentionSocialLSTM** | ✅ (learned)    | ✅ (LSTM)          | ✅                  | Supervised     |

### 🧩 Why AttentionSocialLSTM?
- Models **individual** and **social dynamics**.
- Uses **temporal attention** to weigh past positions.
- Uses **social attention** to weigh influence from nearby agents.
- Performs better in dense and interactive environments.

---
