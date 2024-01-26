# 26 Puzzle Problem - A* Algorithm

## Introduction
This project is an implementation of the A* algorithm to solve the 26 Puzzle Problem. The problem involves a 3D puzzle, conceptualized as a 3x3x3 cube, where the goal is to move from a start state to a goal state through a series of spatial movements.

## Implementation Details
The solution uses the A* algorithm with Manhattan distance as a heuristic. The key functionalities include:

- `manhattanDistance`: To calculate the Manhattan distance from the current state to the goal state.
- `validMovesList`: To find valid moves from a given state.
- `generateMoves`: To generate new states based on valid moves.
- `aStar`: To apply the A* algorithm for finding the shortest path to the goal state.
- `createArray`: To read initial and goal states from an input file and create 3D arrays.

### Technologies Used
- Python
- NumPy
- heapq (Python's priority queue module)

## Setup and Execution
1. Ensure Python and NumPy are installed.
2. Clone the repository to your local machine.
3. Place an `input.txt` file with the start and goal states in the project root.
4. Run the script: `python <script_name>.py`
5. The solution is written to `output.txt`.

## File Formats

### Input File Format
The `input.txt` file should contain 18 lines, 9 for the start state (`n`) and 9 for the goal state (`m`), structured as follows:

n n n<br>
n n n<br>
n n n<br>

n n n<br>
n n n<br>
n n n<br>

n n n<br>
n n n<br>
n n n<br>

m m m<br>
m m m<br>
m m m<br>

m m m<br>
m m m<br>
m m m<br>

m m m<br>
m m m<br>
m m m<br>

#### Symbols Explanation
- `n`: Represents a digit in the start state of the 3x3x3 cube.
- `m`: Represents a digit in the goal state of the 3x3x3 cube.

### Output File Format
The `output.txt` file will contain:

- The start and goal states.
- Depth level `d` of the shallowest goal node.
- Total number of nodes `N` generated, including the root node.
- Solution path `A`, represented by characters {E, W, N, S, U, D} for East, West, North, South, Up, and Down movements.
- Sequence of `f(n)` values for the nodes along the solution path.

n n n<br>
n n n<br>
n n n<br>

n n n<br>
n n n<br>
n n n<br>

n n n<br>
n n n<br>
n n n<br>

m m m<br>
m m m<br>
m m m<br>

m m m<br>
m m m<br>
m m m<br>

m m m<br>
m m m<br>
m m m<br>

d<br>
N<br>
A A A A A A A<br>
f f f f f f f f<br>

#### Symbols Explanation
- `n`: Represents a digit in the start state of the 3x3x3 cube.
- `m`: Represents a digit in the goal state of the 3x3x3 cube.
- `d`: Depth level of the shallowest goal node found by the A* algorithm.
- `N`: Total number of nodes generated in the search tree, including the root node.
- `A`: Sequence of actions (moves) from the root node to the goal node. Each action is represented by a character from {E, W, N, S, U, D}, indicating East, West, North, South, Up, and Down movements of the blank position, respectively.
- `f(n)`: The f-values for each node along the solution path, representing the estimated cost from the start state to the goal state through that node.

## License
This project is available under the [MIT License](LICENSE).