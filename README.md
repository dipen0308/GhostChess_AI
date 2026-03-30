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

## Why "GhostChessAI"?
Because the AI is like a ghostly opponent: always present, never seen, and ready to challenge you at chess!

---
Enjoy your game, and feel free to explore or modify the code to make the AI smarter or the interface even friendlier!
