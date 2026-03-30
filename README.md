# GhostChessAI

Welcome to **GhostChessAI** – a simple, human-friendly chess engine you can play right in your terminal!

## Overview
GhostChessAI is a Python-based chess engine that lets you play against an AI using a clean, labeled board interface. The AI uses a classic Minimax algorithm with Alpha-Beta pruning to make its moves, and you play by entering moves in standard UCI format (like `e2e4`).

### How It Works
- **AI as White:** The AI always starts as White and makes the first move.
- **Human as Black:** You play as Black, entering your moves in UCI format (e.g., `d7d5`).
- **Labeled Board:** The board is displayed with clear rank and file labels, making it easy to follow the game.
- **Engine Logic:** The AI evaluates positions using material count and basic checkmate detection, searching several moves ahead to pick the best option.
- **Game End:** The match ends when checkmate, stalemate, or draw is detected, and the result is displayed.

## How to Play
1. **Install Dependencies:**
   - Make sure you have Python 3 installed.
   - Install the `python-chess` library:
     ```bash
     pip install python-chess
     ```
2. **Run the Game:**
   - Open a terminal in the project folder.
   - Start the game with:
     ```bash
     python main.py
     ```
3. **Enter Your Moves:**
   - When prompted, type your move in UCI format (e.g., `e7e5`).
   - Type `exit` or `quit` to end the game early.

## File Structure
- **main.py** – Handles the game loop, user input, and board display.
- **engine.py** – Contains the AI logic (Minimax with Alpha-Beta pruning).

## Example Gameplay
```
--- CHESS ENGINE v1.2 (Labeled Interface) ---
AI starts as White. Use UCI format (e.g., e7e5) to play.

     a b c d e f g h
   +-----------------+
 8 | r n b q k b n r | 8
 7 | p p p p p p p p | 7
 6 | . . . . . . . . | 6
 5 | . . . . . . . . | 5
 4 | . . . . . . . . | 4
 3 | . . . . . . . . | 3
 2 | P P P P P P P P | 2
 1 | R N B Q K B N R | 1
   +-----------------+
     a b c d e f g h

AI is calculating...
AI Move: e2e4
Your move (Black):
```

## How the AI Thinks: Minimax & Alpha-Beta Pruning

### Minimax Algorithm
The Minimax algorithm is a decision-making process used in two-player games like chess. It works by simulating all possible moves for both players up to a certain depth, assuming both play optimally:
- **Maximizing Player (AI):** Tries to get the highest possible score.
- **Minimizing Player (You):** Tries to get the lowest possible score for the AI (i.e., the best for themselves).
- The AI looks ahead several moves, evaluating each possible position, and chooses the move that leads to the best outcome assuming you also play your best.

### Alpha-Beta Pruning
Alpha-Beta pruning is an optimization for Minimax that makes it much faster:
- **Alpha** is the best score the maximizing player (AI) can guarantee so far.
- **Beta** is the best score the minimizing player (you) can guarantee so far.
- As the AI explores possible moves, if it finds a move that is worse than a previously examined move, it stops considering that branch ("prunes" it), because it knows it would never choose it.
- This means the AI doesn't waste time on moves that won't affect the final decision, allowing it to search deeper and play stronger.

**In short:**
- Minimax helps the AI "think ahead" and plan its moves.
- Alpha-Beta pruning lets it do this much more efficiently, so you get a challenging opponent without long wait times!

## Why "GhostChessAI"?
Because the AI is like a ghostly opponent: always present, never seen, and ready to challenge you at chess!

---
Enjoy your game, and feel free to explore or modify the code to make the AI smarter or the interface even friendlier!
