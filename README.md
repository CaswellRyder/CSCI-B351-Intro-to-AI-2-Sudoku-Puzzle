# Sudoku Solver - Constraint Satisfaction Problem (CSP) Implementation

## Overview

This project is part of the **B351/Q351: Introduction to Artificial Intelligence** course at Indiana University. The objective of this assignment is to implement a Sudoku solver using **constraint satisfaction problem (CSP)** techniques. The solver is built using **backtracking** and **forward checking** algorithms to efficiently solve various Sudoku puzzles.

## Features

- **Sudoku Solver**: Solves Sudoku puzzles of different sizes, including the standard 9x9 board.
- **Constraint Satisfaction**: Ensures each number appears exactly once in every row, column, and box.
- **Backtracking & Forward Checking**: Utilizes CSP techniques to propagate constraints and solve the puzzle effectively.
- **CSV Input**: Accepts Sudoku boards as CSV files, where empty cells are represented by blanks.

## Data Structures

### Board Class
- **n2**: Size of the board (e.g., 9 for a 9x9 board).
- **n**: Size of the smaller boxes (e.g., 3 for a 9x9 board).
- **spaces**: Total number of cells in the Sudoku board.
- **board**: Dictionary that maps coordinates to values.
- **unsolvedSpaces**: Set containing all unsolved cells.
- **valsInRows, valsInCols, valsInBoxes**: Helper structures to track used values in rows, columns, and boxes.

### Solver Class
- The `Solver` class serves as the entry point and implements the core `solveBoard()` function, which performs the backtracking search with forward checking to solve the Sudoku puzzle.

## Functions

- **Board.makeMove()**: Assigns a value to a cell and updates row, column, and box constraints.
- **Board.undoMove()**: Reverts a move, clearing the cell and updating constraints.
- **Board.isValidMove()**: Checks if a move is valid according to Sudoku rules.
- **Board.getMostConstrainedUnsolvedSpace()**: Returns the cell with the fewest valid values left to try.
- **Solver.solveBoard()**: Implements the backtracking search with forward checking to find a solution to the Sudoku puzzle.

## How to Run

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/sudoku-solver.git
   cd sudoku-solver
   ```

2. Ensure you have **Python 3** installed. The project is not compatible with Python 2.x.

3. Place your Sudoku puzzle CSV file in the `tests/` directory, or use the provided examples.

4. Update the input path in `a2.py` to point to your desired puzzle file.

5. Run the program:
   ```
   python3 a2.py
   ```

## Example Input

An example 9x9 Sudoku puzzle in CSV format (saved as `example.csv`):

```
,3,,8,,5,,
,,1,2,,,,
5,,,,,7,,
,4,,,,1,,
9,,,,,,,,
,5,7,,,,3,
,2,,,,,1,,
,,4,9,,,,
,,,7,,2,,
```

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

## Acknowledgements

This project is part of an assignment for the **B351/Q351: Introduction to Artificial Intelligence** course at Indiana University.

---

## Notes:
My program achieved 5 hours for test-4-hard/19.csv and achieved 5.16 seconds in /named-boards/bowser.csv
