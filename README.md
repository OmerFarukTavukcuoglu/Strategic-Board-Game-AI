# 🎮 AI-Based Strategic Board Game

## Project Overview
This project implements an AI-driven strategic board game, developed as a term project using Python and the PyCharm IDE. The game is designed for a **7x7 board**, where an **AI (Player 1) competes against a human player (Player 2)**. The AI is built using **Min-Max, Q-Learning, or Deep Q-Learning Networks** to make strategic moves and defeat the opponent.

---

## Game Rules & Mechanics

### Initial Setup
- The game board consists of **7 rows × 7 columns**.
- **Triangle (△) pieces** represent the AI (**Player 1**).
- **Circle (○) pieces** represent the human player (**Player 2**).
- Each player starts with **4 pieces** placed in a specific formation.
- The **AI always makes the first move**.

### Move Rules
- Pieces **can move horizontally and vertically**.

- **No diagonal moves** allowed.

- If a player has **multiple pieces**, they must make **two consecutive moves**.

✔ If a player has **only one piece**, they can **only make one move**.

### Capturing System
- A piece (or group of pieces) is **captured** if:
  - It is **trapped between an opponent’s piece and the board edge**.
  - It is **sandwiched between two opponent pieces**.
  - Both players' pieces are trapped between opponent pieces, leading to **multiple captures**.

### Win Conditions
- **Draw**:
  - Both players have **no pieces left**.
  - Both players have **only one piece left**.
- **Victory**:
  - The opponent has **no remaining pieces**.
  - After **50 total moves**, the player with **more pieces wins**.
- **Defeat**:
  - The player has **no pieces left**, but the opponent does.
  - After **50 moves**, the player with **fewer pieces loses**.

---

## AI Implementation
The AI engine is built using **advanced decision-making algorithms** to maximize efficiency and strategic play.

### **1️⃣ Min-Max Algorithm**
- Evaluates possible future moves and assigns scores.

- Selects the move that **maximizes advantage** while minimizing the opponent's.

- Can be optimized using **Alpha-Beta pruning**.

### **2️⃣ Q-Learning (Reinforcement Learning)**
- AI **learns from experience**, improving over time.

- Rewards **optimal moves**, penalizes **bad decisions**.

- Makes AI more adaptable.

### **3️⃣ Deep Q-Learning Networks (DQN)**
- Uses **Neural Networks** to predict the best moves.

- Allows for **dynamic, self-learning AI**.

- More computationally intensive but highly effective.

---

## Technical Implementation

### User Interface
- **Supports CLI & GUI** versions.

- Allows players to **input moves, view board state, and track AI decisions**.

###  Move Validation & Capture Detection
- Ensures only **valid moves** are executed.

- **Automatically detects and removes captured pieces**.

- Implements **turn-based gameplay rules**.

###  Turn Management & Move Counter
✔ Tracks total moves and **enforces the 50-move rule**.

✔ Ensures **AI moves first**.

✔ Prevents illegal moves.
