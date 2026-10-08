# Chess AI

A chess engine that learns from self play, with two implementations in this repo: one in Python using TensorFlow, and one in C++. It can use Stockfish as a training opponent and reference.

## Layout

- `V-Python`: the Python version. Contains the model and training code (`Ai`) and rating tools (`rating`).
- `V-Cpp`: the C++ version, as a Visual Studio solution (`ChessBot.sln`).

## Python version

Requirements are pinned in `requirements.txt`:

- numpy 1.22.0
- tensorflow 2.8.0
- keras-tuner 1.1.0
- python-chess 0.31.3

Set up and install:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

From there you can run the training and play scripts under `V-Python/Ai`. The model improves through self play and reinforcement learning. Stockfish is used as an opponent during training, so you need a Stockfish binary available if you want that path.

## C++ version

Open `V-Cpp/ChessBot.sln` in Visual Studio and build the solution. It mirrors the same idea in C++.

## Notes

This is a learning project for building a chess engine and training it over time. Results depend on how long you train and the hardware you use.
