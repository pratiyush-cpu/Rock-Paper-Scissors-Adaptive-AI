# Rock Paper Scissors – Adaptive AI

A Python Rock Paper Scissors game that learns from a player's previous moves using probability, frequency counts and Markov-chain pattern recognition. Developed as a Computational Thinking and Mathematics project.

## Features

- Tkinter graphical interface for playing against the AI
- Six prediction methods: overall frequency, recent frequency, Markov orders 1–3, and a combined fallback
- Predictor selection using smoothed accuracy and a 5% exploration rate
- Simulation mode with four artificial players: biased, cyclic, beat-own-last and uniform random
- Statistics, transition probabilities, charts and a built-in explanation screen
- Automated tests
- Separate terminal-based version

## Requirements

- Python 3 with Tkinter support
- No third-party Python packages are required

Tkinter is bundled with many Python installations. On some Linux distributions, install the OS package `python3-tk` if it is missing.

## Run

From the repository folder:

```bash
python rps.py
```

To run the automated tests:

```bash
python rps.py --test
```

To run the simpler terminal game:

```bash
python rock_paper_scissors.py
```

On systems where `python` points to Python 2, use `python3` instead.

## How it works

The computer predicts the player's next move from previous completed rounds and chooses the counter-move. The AI compares different predictors based on their past performance. It updates its records **after** the current round, so it cannot see the player's current move before deciding.

A uniformly random opponent cannot be reliably predicted; the theoretical win-rate baseline is approximately **33.33%**.

## Files

| File | Purpose |
| --- | --- |
| `rps.py` | Main GUI, adaptive AI, simulations and automated tests |
| `rock_paper_scissors.py` | Simpler terminal-based game |

## Notes

The project uses statistical learning and pattern recognition, **not** neural networks or deep learning. The full academic report is maintained separately.
