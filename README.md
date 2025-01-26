# Chess AI Game with Genetic Algorithm and GUI

## Overview
This project is a Python-based chess game that combines Artificial Intelligence (AI) with an intuitive Graphical User Interface (GUI). The AI opponent is powered by a Genetic Algorithm, making gameplay challenging and engaging. The game allows human players to compete against a smart AI while adhering to chess rules and providing a realistic gaming experience.

---

## Features
- **Graphical User Interface (GUI):**
  - A visually appealing and interactive chessboard for user interaction.
  - Highlights possible moves and visually updates the board in real-time.
  - Alerts for game events such as check, checkmate, stalemate, or invalid moves.
  - Displays endgame messages (e.g., "Checkmate!").
  
- **AI Opponent:**
  - Built using a **Genetic Algorithm** to evaluate and select the best moves.
  - Optimizes gameplay by analyzing potential moves and simulating outcomes.
  - Implements Minimax and crossover techniques for strategic decision-making.

- **Chess Mechanics:**
  - Enforces official chess rules, including legal moves, checks, checkmate, and stalemates.
  - Handles turn-based gameplay between the human player and AI.

---

## Problem Description
Chess, while simple in rules, is a complex game requiring deep strategic and tactical thinking. Many beginners struggle against skilled players due to the game's intricacies. This project addresses this challenge by creating an AI-driven chess program that provides a smooth and engaging experience for users. The AI uses a Genetic Algorithm to simulate a challenging opponent, making it enjoyable for both beginners and experienced players.

---

## Program Functionality

### Inputs:
1. **Player Moves:** The user interacts with the GUI to make chess moves.
2. **AI Parameters:** Internal configurations like the number of generations, population size, mutation rate, and sequence length for the Genetic Algorithm.

### Outputs:
1. **Real-time Visual Updates:** The board and pieces update instantly after each move.
2. **Notifications:** Alerts for invalid moves, check, checkmate, or stalemate.
3. **AI Moves:** The program computes and displays the AI’s move using the Genetic Algorithm.
4. **Endgame Messages:** Displays the result, such as "Checkmate!" or "Player Wins!".

---

## Implementation

### 1. Libraries Used
- **customtkinter:** For creating the interactive and customizable GUI.
- **python-chess:** For chessboard representation, legal move validation, and game state management.
- **Pillow:** For handling chess piece images.
- **random:** For generating random sequences in the Genetic Algorithm.

### 2. Genetic Algorithm
The Genetic Algorithm powers the AI opponent and evaluates the board to determine the best possible moves. Key methods include:
- **evaluate_fitness:** Calculates the fitness score of each move based on piece safety and board position.
- **genetic_algorithm:** Simulates evolution to find the optimal sequence of moves by:
  - Initializing random populations of moves.
  - Evaluating fitness for each sequence.
  - Using crossover and mutation to generate new populations.
  - Selecting the best move sequence.
- **crossover_sequences:** Combines two strong sequences to create better strategies.
- **mutate_sequence:** Introduces randomness to explore new tactical opportunities.

### 3. Graphical User Interface (GUI)
The GUI is designed to ensure a seamless and intuitive user experience. Key features include:
- **Chessboard Display:** Shows the board with properly placed pieces.
- **Move Handling:** Validates and executes player moves, highlights possible moves, and sends updates to the AI.
- **Game Over Screen:** Displays the result (e.g., "Checkmate!") and disables further interactions.
- **AI Integration:** Automatically computes and executes AI moves during its turn.

---

## How to Run the Program

1. Install the required libraries:
   ```bash
   pip install customtkinter python-chess Pillow
