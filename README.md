# Monte Carlo Blackjack Learning Agent

Implementation of a self-learning Blackjack AI using Monte Carlo methods for reinforcement learning.

## Overview

This project implements a Blackjack agent that learns optimal playing strategies through Monte Carlo control with epsilon-greedy exploration.

### Results

- **Win Rate:** 41.57% over 10,000 evaluation games
- **Average Reward:** -0.09
- Successfully learns basic strategy through self-play

## Features

- Monte Carlo reinforcement learning algorithm
- Epsilon-greedy exploration strategy
- Support for multiple rule variants (dealer hits soft 17, double anytime)
- Complete point-count card counting system integration
- Visualization of optimal policy for different scenarios

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

# Evaluate learned policy
winrate, avgreward, wins, losses, ties = evaluate_policy(Q)
```

## Game Actions

- **Hit (0):** Take another card
- **Stand (1):** Keep current hand
- **Double Down (2):** Double bet and take one card

## License

MIT License

[1](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/95587544/fd3aca22-1383-473f-b238-8bbe1fb7a58b/task-p3-1.ipynb)
