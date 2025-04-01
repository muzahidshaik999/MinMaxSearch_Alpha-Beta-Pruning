# Alpha-Beta Pruning with Minimax Search

## Overview
This repository contains two Python programs implementing the Minimax search algorithm with Alpha-Beta pruning optimization. The programs compute the optimal path and value for given game trees using decision-making strategies in artificial intelligence.

## Files
### MinMaxSearch_Alpha-Beta Pruning1.py
- Implements the Minimax algorithm with Alpha-Beta pruning for a game tree with three child nodes at each level.
- Computes the optimal value and path.

### MinMaxSearch_Alpha-Beta Pruning2.py
- Implements the Minimax algorithm with Alpha-Beta pruning for a deeper game tree with multiple levels.
- Computes the optimal value and path for a more complex structure.

## Algorithm Description
The algorithm follows these steps:

### Initialize Alpha and Beta:
- `alpha = -∞` (best value for the maximizer)
- `beta = ∞` (best value for the minimizer)

### Recursive Minimax Function with Pruning:
1. If the current node is a leaf node, return its value.
2. If the node is a maximizing player:
   - Initialize `max_value = -∞`
   - Iterate through child nodes:
     - Recursively call Alpha-Beta Pruning for child nodes.
     - Update `max_value` and `alpha`.
     - If `alpha >= beta`, prune the remaining branches.
   - Return `max_value`.
3. If the node is a minimizing player:
   - Initialize `min_value = ∞`
   - Iterate through child nodes:
     - Recursively call Alpha-Beta Pruning for child nodes.
     - Update `min_value` and `beta`.
     - If `alpha >= beta`, prune the remaining branches.
   - Return `min_value`.

### Finding the Optimal Path:
- Start from the root node and iteratively choose the best child node.
- Store the selected nodes to represent the optimal path.

## How to Run
1. Install Python (if not already installed).
2. Clone this repository or download the script files.
3. Open a terminal or command prompt.
4. Run either of the scripts:
   ```bash
   python MinMaxSearch_Alpha-Beta Pruning1.py
   ```
   or
   ```bash
   python MinMaxSearch_Alpha-Beta Pruning2.py
   ```

## Expected Output
Each script prints:
- The optimal value computed by the algorithm.
- The optimal path taken from the root node to the leaf node.

## Applications
- Decision-making in AI-based games.
- Optimization of search trees in complex decision problems.
- Efficient pruning of unnecessary computations in game strategies.

