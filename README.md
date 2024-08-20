Maze Solver Using DFS and BFS
This project implements a maze solver using Depth First Search (DFS) and Breadth First Search (BFS) algorithms. The maze is represented by a grid, where # represents walls, O is the starting point, and X is the end goal. The pathfinding algorithms will attempt to find the shortest path from O to X, and the result is displayed using the curses library for terminal-based visualization.

Maze Representation
The maze is represented as a list of lists, with each element being one of the following:

# : Wall
: Free path
O : Start position
X : End position
Example:

python
Code kopiëren
maze = [
    ["#", "O", "#", "#", "#", "#", "#", "#", "#"],
    ["#", " ", " ", " ", " ", " ", " ", " ", "#"],
    ["#", " ", "#", "#", " ", "#", "#", " ", "#"],
    ["#", " ", "#", " ", " ", " ", "#", " ", "#"],
    ["#", " ", "#", " ", "#", " ", "#", " ", "#"],
    ["#", " ", "#", " ", "#", " ", "#", " ", "#"],
    ["#", " ", "#", " ", "#", " ", "#", "#", "#"],
    ["#", " ", " ", " ", " ", " ", " ", " ", "#"],
    ["#", "#", "#", "#", " ", " ", "#", " ", "#"],
    ["#", "#", "#", "#", "#", "X", "#", "#", "#"]
]
Installation
Prerequisites
Python 3.7 or higher is required.
The curses library is used to visualize the pathfinding algorithms. However, the native curses library is not supported on Windows, so you will need to install windows-curses on Windows.
Steps
Clone the repository:

bash
Code kopiëren
git clone https://github.com/yourusername/maze-solver.git
cd maze-solver
Install dependencies:

On Linux/macOS:

No additional dependencies are required for curses.

On Windows:

You will need to install windows-curses:

bash
Code kopiëren
pip install windows-curses
Usage
The project provides two different scripts: one for DFS and one for BFS. Both scripts are designed to find a path in the maze from the start position O to the end position X and visualize the process in the terminal using curses.

Running the DFS Solver
To run the DFS (Depth First Search) solver, use the following command:

bash
Code kopiëren
python3 dfs_maze_solver.py
Running the BFS Solver
To run the BFS (Breadth First Search) solver, use the following command:

bash
Code kopiëren
python3 bfs_maze_solver.py
Controls
The script will automatically run and visualize the search algorithm.
The terminal will display the maze, where the current path being explored is shown in red (or another color, depending on your terminal color scheme).
Once the algorithm finds the path from O to X, the path will be highlighted.
Press any key to exit the visualization.
Code Overview
main(stdscr)
This function is the entry point for the curses environment. It sets up color pairs and calls the find_path function, which implements the DFS/BFS logic.

find_path(maze, stdscr)
This function executes the search algorithm (DFS/BFS), prints the current maze state to the terminal, and highlights the path found.

print_maze(maze, stdscr, path=[])
Prints the maze to the terminal, using different colors to highlight the current path.

find_start(maze, start)
Locates the starting position O in the maze.

find_neighbors(maze, row, col)
Returns a list of valid neighboring cells (up, down, left, right) that can be visited from the current cell.

Example
Here is what you will see when the program runs:

The maze will be printed in the terminal.
The algorithm will explore the maze, updating the visualization with the current path.
The path to the goal will be highlighted in red once found.
