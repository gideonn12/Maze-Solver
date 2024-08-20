# Maze Solver Project

## Description

This project is a simple maze-solving algorithm implemented in Python. The program uses the `curses` library to create a visual representation of a maze and solve it using the Depth-First Search (DFS) algorithm. A BFS implementation is also available. The maze is represented as a 2D grid, where `"#"` represents walls, `" "` represents open paths, `"O"` is the start point, and `"X"` is the endpoint.

The program highlights the path from the start to the endpoint as it explores the maze.

## Getting Started

### Prerequisites

- Python 3.x
- The `curses` module (for Unix-like systems) or the `windows-curses` package (for Windows).

### Installing Dependencies

For Unix-like systems (Linux, macOS):

No additional installation is necessary as the `curses` module is included with Python on these systems.

For Windows:

1. Install the `windows-curses` package using pip:
    ```bash
    pip install windows-curses
    ```

### Running the Program

1. Clone this repository to your local machine.
2. Ensure you have all the dependencies installed.
3. Run the program:

    For the DFS algorithm:
    ```bash
    python3 dfs.py
    ```

    For the BFS algorithm:
    ```bash
    python3 bfs.py
    ```

### Controls

- The program runs automatically upon execution and will display the maze along with the path it is exploring.
- Press any key to exit once the path is found and displayed.

## Project Structure

- `maze`: The maze is represented as a 2D list where each character represents a different element in the maze.
- `print_maze`: A function that prints the maze to the terminal using the `curses` library, with the current path highlighted.
- `find_start`: A helper function that locates the starting position ("O") in the maze.
- `find_path`: The main algorithm function that uses DFS (or BFS) to find a path from start to end.
- `find_neighbors`: A helper function that finds all possible moves from a given position.
- `main`: The entry point of the program that initializes `curses` and starts the maze-solving process.

## Algorithms Used

### Depth-First Search (DFS)

DFS explores a path by going as deep as possible before backtracking. It uses a stack (LifoQueue) to keep track of the current path. The algorithm follows these steps:
1. Start at the "O" position.
2. Explore as far as possible along each branch before backtracking.
3. If the end "X" is found, the path is returned.

### Breadth-First Search (BFS)

BFS explores the maze level by level, ensuring the shortest path is found. It uses a queue to explore all possible positions from the current location before moving on to the next level.

## Example Output

Below is an example of the program running and solving the maze. The path is highlighted as the algorithm progresses.

![Maze Solver Running](assets/maze_solver_running.png)

*Place your screenshot of the program running in the `assets` directory with the filename `maze_solver_running.png`. Make sure to create the `assets` directory if it doesn't exist.*

## Troubleshooting

- **Curses errors on Windows:** Ensure you have installed the `windows-curses` package if you're running this on a Windows system.

## Contributing

If you wish to contribute to this project, feel free to fork the repository and submit a pull request.

## License

This project is open-source and available under the MIT License.
