# Adaptive Blackjack Player Using Monte Carlo Reinforcement Learning

Self-learning Blackjack AI agent using Monte Carlo control methods to develop optimal playing strategies through simulated gameplay.

## Overview

This project implements an intelligent Blackjack agent that dynamically adapts its strategy to maximize profits using reinforcement learning techniques.

## Key Features

- **Monte Carlo Control Algorithm** for optimal policy learning
- **Hi-Lo Card Counting System** integration for enhanced decision-making
- **Epsilon-Greedy Exploration** balancing exploration and exploitation
- **Rule Variations** support (Dealer Hits Soft 17, Double Anytime)
- **Basic Strategy** implementation as foundation
- Visualization of learned policies and training progress

## Performance Results

| Strategy | Win Rate | Loss Rate | Tie Rate | Avg Reward |
|----------|----------|-----------|----------|------------|
| Basic Strategy | 41.50% | 50.74% | 7.75% | -0.09 |
| Card Counting | 42.78% | 48.30% | 8.92% | -0.05 |
| Soft 17 Variation | 41.99% | 50.89% | 7.31% | -0.09 |
| Double Anytime | 42.00% | 50.94% | 7.05% | -0.09 |

[2][1]

## Technologies

- Python 3.7+
- NumPy
- Matplotlib

## Installation

```bash
pip install numpy matplotlib
```

## Usage

```python
# Train the agent
numgames = 100000
env = TwentyOneGame()
Q, winrates, rewards = montecarlo_control(env, numgames)

# Evaluate performance
winrate, avgreward, wins, losses, ties = evaluate_policy(Q, num_eval_games=10000)
```

## Game Actions

- **Hit (0):** Draw another card
- **Stand (1):** Keep current hand
- **Double Down (2):** Double bet and draw one final card

## Project Structure

```
├── task-p3-1.ipynb           # Implementation notebook
├── Research-papper.pdf       # Research paper with detailed analysis
└── README.md                 # Project documentation
```

## Algorithm

Monte Carlo control with Q-value updates:

$$ Q(s, a) \leftarrow Q(s, a) + \alpha (G - Q(s, a)) $$

## References

- Thorp, Edward O. "Beat the Dealer" (1966)
- Sutton & Barto. "Reinforcement Learning: An Introduction" (2018)

## Author

Ranjitha Umesh  
Technical University of Applied Science, Würzburg-Schweinfurt

## License

MIT License

[1](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/95587544/fd3aca22-1383-473f-b238-8bbe1fb7a58b/task-p3-1.ipynb)
[2](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/95587544/35f7f60e-1ba3-4ffe-a98e-68d4fc3b5457/Research-papper.pdf)
