# Defination
Lots of states that might happen with the steps going on.

* Assume both opponents are infinitely intelligent and always chose the best move.

Each grid is assigned a numerical score that indicates how optimistic we are about winning.

    1: The computer is guaranteed a win.
    -1: The opponent is guarantted a win.
    0: if perfect players will draw.

Scoring a grid.

Suppose computer is playing X.

    3 X's in a row: 1.
    3 O's in a row: -1.
Any other grid: computed by a `minimax-algorithm`.

# Minimax Algorithm
- Consider each possible move. 
- Determine each child grid.
- Score each child grid by calling minimax recursively. 
- Score parent grid.
        
        Computer's turn: choose move that yields the maximum score.
        Opponent's turn: choose move that yields the minimum score.
Each grid in game tree represents one invocation of chooseMove().  

# Simple pruning
If a player discovers a guaraneed winning move, there's no reason to search for a better move. (剪枝)

**Saves time**

# Alpha-beta pruning
`alpha`: a score the computer knows with certainty it can achieve.

The opponent can achieve a score of `beta` or better.

If `beta` becomtes <= `alpha`, further investigation of current grid is useless.


