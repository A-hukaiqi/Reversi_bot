# Reversi AI Bot

## Overview
This project implements an AI bot that plays Reversi (Othello) on any board size up to 26x26. The AI uses a **minimax algorithm with alpha-beta pruning** to play strategically and make optimal decisions. The game allows users to play against the bot by entering their moves.

## Game Rules
Reversi is a strategy board game played on a grid (typically 8x8, but adjustable here). The game involves two players, one controlling black discs (B) and the other controlling white discs (W).

### How to Play:
1. Players take turns placing their colored disc on the board.
2. A move is legal if it sandwiches one or more of the opponent’s discs between your newly placed disc and one of your other discs. You can sandwich them horizontally, vertically, or diagonally.
3. When a disc is sandwiched, all the opponent’s discs between your discs flip to your color.
4. If a player has no valid moves, they must pass their turn.
5. The game ends when neither player can make a valid move, and the player with the most discs wins.

## Bot Features
- **Dynamic board size**: You can play on any board size up to 26x26.
- **AI using Minimax Algorithm**: The bot uses minimax with alpha-beta pruning to make efficient decisions.
- **Evaluation Heuristics**: The AI evaluates each move based on:
  - **Corner control**: Capturing corners is prioritized.
  - **Mobility**: AI values keeping its options open and restricting the opponent.
  - **Piece count**: AI also considers how many pieces it controls.
 
## Areas of Improvements
- **Endgame optimization**: The bot could be better at handling endgame situations where piece count becomes more critical.
- **Dynamic depth:**: Introducing a dynamic search depth based on the current state of the game might improve performance.
- **Transposition Tables:** Caching previously evaluated board states to avoid re-evaluating them would further improve the AI's speed.
  
## How to Play Against the Bot
**1. Compile the code using a C compiler (e.g., GCC):**

   gcc -o reversi reversi.c necessary_functions.c
   
**2. Run the Game:**
After compiling, run the executable to start the game:

    ./reversi
   
**4. Enter the Board Size:**
For a standard 8x8 board, you can type 8, but you can choose any board size up to 26x26. For example:

    Enter the board dimension: 8

**5. Choose the AI's Color:**
Choose whether the AI should play as black (B) or white (W). Type B or W based on your choice:

    Computer plays (B/W): B
    
If you choose B, the computer will play as black, and you will play as white.
If you choose W, the computer will play as white, and you will play as black.

**5. Make Your Move:**
The game will display the current state of the board, and you will be prompted to make your move. Enter your move in the format RowCol (e.g., a1), where the first letter represents the row and the second letter represents the column. For example:

    Enter move for colour W (RowCol): b4
    
The first character (b) represents the row.
The second character (4) represents the column.

**6. Computer's Move:**
After you make your move, the AI will calculate and place its move on the board. The computer will print a message indicating where it placed its disc, and the updated board will be displayed. For example:

    Computer places B at c5.

**7. Continue Playing:**
The game will continue with alternating turns between you and the AI. The game will automatically check for valid moves. If neither player has a valid move, they will pass their turn.

If the AI or the player runs out of valid moves, the game will notify that player, and the other will continue until no moves are left for either side.

**8. End of Game:**
When neither player can make a valid move, the game will end, and the winner will be announced based on the number of discs each player controls. For example:

    B player wins.
   
If both players have the same number of discs, the game will result in a draw.

