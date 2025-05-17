# DDoS Attack Detection Using Reinforcement Learning

This project implements an adaptive intrusion detection system for DDoS attacks using a Deep Q-Network (DQN). It transforms the detection task into a reinforcement learning problem using a custom OpenAI Gym environment built on the NSL-KDD dataset.

## Requirements

To run the notebook and experiments, install the following Python packages:

```bash
pip install gym
pip install numpy pandas matplotlib scikit-learn torch
```

## How to Run

1. Clone the repository or open the notebook file `DDoS_RL_IDS.ipynb` in Jupyter or Google Colab.
2. The dataset is automatically downloaded via a `wget` command from the NSL-KDD GitHub repository.
3. The notebook performs the following steps:
   - Loads and preprocesses the NSL-KDD dataset
   - Sets up a custom Gym environment for intrusion detection
   - Defines and trains a DQN agent
   - Evaluates the agent's performance using reward trends and training plots

No additional configuration is needed beyond running the cells sequentially.

## Expected Results

- The agent learns to classify network traffic as either benign or DDoS attack.
- It improves detection accuracy over training episodes using a reward-driven strategy.
- Visualizations show:
  - Cumulative reward increasing over time
  - Epsilon decay reflecting a shift from exploration to exploitation

## Future Development

- Extend support to multi-class intrusion detection (e.g., R2L, U2R, Probe)
- Test deployment in real-time network simulation environments
- Explore alternative RL algorithms like Proximal Policy Optimization (PPO) or Actor-Critic methods for improved performance
