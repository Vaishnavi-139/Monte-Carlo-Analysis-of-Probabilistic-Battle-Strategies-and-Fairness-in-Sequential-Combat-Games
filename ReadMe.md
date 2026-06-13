
# Monte Carlo Analysis of Probabilistic Battle Strategies and Fairness in Sequential Combat Games

## Overview

This project investigates a probabilistic combat game involving two competing armies with warriors of varying strengths. The objective is to analyze different warrior-selection strategies, estimate winning probabilities through Monte Carlo simulation, and mathematically verify whether the game is fair.

The study combines simulation, probability theory, expected value analysis, and mathematical induction to evaluate strategic decision-making under uncertainty.

---

## Problem Statement

Two players, Alice and Bob, possess armies consisting of warriors with predefined strengths.

### Alice's Army

```text
[3, 4, 6, 7]
```

### My Army

```text
[9, 3]
```

During each round:

1. Alice randomly selects one warrior.
2. A strategy determines which of my warriors is selected.
3. The probability of winning a duel is proportional to warrior strength:

P(Win) = My Strength / (My Strength + Opponent Strength)

4. The winner absorbs the loser's strength.
5. The process continues until one army is eliminated.

The goal is to estimate the probability of winning under different strategies and analyze the fairness of the game.

---

## Methodology

### Monte Carlo Simulation

The battle process is simulated thousands of times to estimate empirical winning probabilities.

Number of simulations:

```text
5000
```

Each simulation represents a complete match from start to finish.

---

## Strategies Evaluated

### 1. Maximum Strength Strategy

Always select the strongest available warrior.

Example:

```text
My Warriors: [9, 3]
Selected Warrior: 9
```

Estimated Winning Probability:

```text
0.375
```

---

### 2. Minimum Strength Strategy

Always select the weakest available warrior.

Example:

```text
My Warriors: [9, 3]
Selected Warrior: 3
```

Estimated Winning Probability:

```text
0.373
```

---

### 3. Random Strategy

Select a warrior uniformly at random.

Estimated Winning Probability:

```text
0.385
```

---

## Results

| Strategy         | Winning Probability |
| ---------------- | ------------------- |
| Maximum Strength | 0.375               |
| Minimum Strength | 0.373               |
| Random Selection | 0.385               |

### Observation

All three strategies produce remarkably similar winning probabilities.

This suggests that the game outcome is primarily governed by total army strength rather than the specific warrior selection strategy.

---

## Expected Value Analysis

For warriors with strengths:

```text
x = Alice's warrior
y = My warrior
```

Expected gain is:

E(Gain) =
P(Win) × Gain on Win +
P(Loss) × Gain on Loss

Substituting:

E(Gain) =
(xy/(x+y)) -
(xy/(x+y))

E(Gain) = 0

### Interpretation

Every individual duel is fair in expectation.

Neither player possesses a systematic probabilistic advantage.

---

## Mathematical Proof

The project further proves, using mathematical induction, that the probability of winning depends solely on the total remaining army strengths.

For armies with total strengths:

```text
a = Alice's total strength
b = My total strength
```

The winning probability is:

P(a,b) = a / (a+b)

The proof is established using:

* Base Case
* Inductive Hypothesis
* Inductive Step

This result demonstrates that strategic selection has negligible long-term impact on winning probability.

---

## Technologies Used

* Python
* NumPy
* Pandas
* Google Colab
* Monte Carlo Simulation
* Probability Theory

---

## Key Concepts Demonstrated

* Monte Carlo Methods
* Game Theory
* Probabilistic Modeling
* Randomized Algorithms
* Expected Value Analysis
* Mathematical Induction
* Strategy Evaluation
* Statistical Simulation

---



## Learning Outcomes

Through this project, I developed an understanding of:

* Simulation-based probability estimation
* Modeling stochastic systems
* Comparing decision strategies quantitatively
* Mathematical validation of empirical findings
* Combining theory with computational experimentation

---

## Future Improvements

* Dynamic strategy optimization
* Reinforcement learning-based warrior selection
* Larger army configurations
* Visualization of battle progression
* Sensitivity analysis on army strengths
* Multi-player battle environments

---
