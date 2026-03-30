# 👻 GhostChess

> **"The board is a stage, and the moves are mere shadows."**

Welcome to **GhostChess**, a minimalist, high-performance Python chess engine. Developed for the **VIT BYOP project**, GhostChess strips away the bloat to focus on the core of computer science: recursive search, heuristic evaluation, and algorithmic efficiency.

It doesn’t just play chess; it haunts the possibilities of the board until it finds the inevitable win.

---

## 🧠 The Ghost in the Machine

GhostChess isn't just a basic script. It uses a sophisticated **Minimax search** paired with **Alpha-Beta Pruning** to "see" through the noise of the game.

* **Minimax Strategy:** It simulates thousands of potential futures, assuming you’ll play your best while it plays its own.
* **Alpha-Beta Pruning:** Like a ghost passing through walls, this optimization allows the engine to ignore "dead" branches of the move tree, making its calculations incredibly efficient.
* **Material Weighting:** The engine assigns value to every piece (e.g., Queens at **900**, Knights at **320**). It knows exactly what a sacrifice is worth.

---

## 📂 Project Anatomy

* `main.py` — The interface. Handles the game loop, ASCII board rendering, and user input.
* `engine.py` — The soul of the project. Contains the evaluation logic and search algorithms.
* `requirements.txt` — Powering the logic with the `python-chess` library.

---

## 🚀 Summoning the Engine

Get GhostChess running on your local machine in seconds.

### 1. Setup
We recommend using a virtual environment to keep your global Python space clean:

```bash
# Initialize and activate venv
python -m venv venv
source venv/bin/activate  # macOS/Linux
# OR
.\venv\Scripts\activate   # Windows

# Install dependencies
pip install -r requirements.txt

python main.py
