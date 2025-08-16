# 📌 Sudoku Solver
This project is a C++ based Sudoku Solver that uses backtracking to solve a standard 9×9 Sudoku puzzle. The program provides an interactive interface for the user to input the Sudoku puzzle and then applies recursive backtracking to compute the solution.

---

## ✨ Features
### 1.Two Input Modes
- Manual Input: Enter Sudoku values cell-by-cell through the console. Empty cells are represented by 0.
- File Input: Provide a text file containing all 81 values separated by spaces. Empty cells should be written as 0.

### 2.Grid Representation
- The Sudoku grid is stored internally as a 9x9 integer array.
- Values are displayed in a formatted grid with clear separators for 3×3 sub-grids.

### 3.Validation Checks
- Ensures that numbers follow Sudoku rules:
  - Each row must contain unique values (1–9).
  - Each column must contain unique values.
  - Each 3×3 sub-grid must contain unique values.
- Input values are checked for correctness (0–9 range).

Backtracking Algorithm

Uses recursion to try possible values for empty cells.

If a chosen number violates Sudoku rules, it backtracks and tries another value.

This continues until the grid is completely solved or no solution is possible.

Statistics

Tracks how many times the recursive singleCellSolve() function is called.

Displays recursion count after solving, giving insight into computational effort.

User Feedback

Prints intermediate messages like “Calculating possibilities...” and “Backtracking across puzzle...”.

Informs whether the puzzle has been solved or if it has no valid solution.

⚙️ Core Components
SudokuGrid Class

Manages the Sudoku grid (input, storage, display, set/get cell values).

Provides options to input from console or file.

Handles formatting of the Sudoku board for better visualization.

SudokuSolver Class

Implements the backtracking algorithm.

Contains methods for validating rows, columns, and 3×3 sub-grids.

Checks whether the grid is completely solved.

Calls recursive solving function until solution is found.

🚀 Working Flow
Menu Prompt → User selects input method (manual/file).

Input Puzzle → Sudoku grid is filled into memory.

Initial Display → Shows the unsolved Sudoku grid.

Solve Process → Recursive backtracking algorithm tries all valid possibilities.

Final Display → Prints the solved Sudoku grid (if solvable).

Statistics → Shows number of recursive calls used in solving.

📂 Example File Input
A text file (puzzle.txt) with values:

5 3 0 0 7 0 0 0 0
6 0 0 1 9 5 0 0 0
0 9 8 0 0 0 0 6 0
8 0 0 0 6 0 0 0 3
4 0 0 8 0 3 0 0 1
7 0 0 0 2 0 0 0 6
0 6 0 0 0 0 2 8 0
0 0 0 4 1 9 0 0 5
0 0 0 0 8 0 0 7 9
Empty spaces are represented by 0.

📊 Example Output
++=====================================++
|| 5  3     ||     7     ||             ||
++-----------++-----------++-----------++
|| 6         || 1  9  5   ||             ||
++-----------++-----------++-----------++
||    9  8   ||           ||     6       ||
++=====================================++
|| 8         ||     6     ||         3   ||
++-----------++-----------++-----------++
|| 4         || 8     3   ||         1   ||
++-----------++-----------++-----------++
|| 7         ||     2     ||         6   ||
++=====================================++
||    6      ||           || 2  8        ||
++-----------++-----------++-----------++
||           || 4  1  9   ||        5    ||
++-----------++-----------++-----------++
||           ||     8     ||     7  9    ||
++=====================================++
After solving, the complete Sudoku grid is displayed.

📌 Key Learning Outcomes
Understanding backtracking and recursion in problem solving.

Implementing input validation and structured user interaction.

Applying object-oriented programming (OOP) concepts in C++.

Visual representation of a grid-based puzzle.

👉 This project demonstrates how backtracking algorithms can be applied to real-world puzzles like Sudoku, and also emphasizes clean code structure, OOP practices, and user-friendly interaction.
