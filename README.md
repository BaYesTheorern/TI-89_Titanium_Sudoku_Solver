### TI-89 Sudoku Solver — Program Overview

This program is a **Sudoku solver for the TI-89 calculator**. It provides an interactive grid for entering a Sudoku puzzle and uses a memory-efficient backtracking algorithm to solve it.

**Main functions:**

* **Interactive Sudoku grid:**
  A 9×9 square grid is displayed on the calculator screen.

* **Puzzle input:**
  Use the arrow keys to move between cells and the number keys `1–9` to enter values. `0` or `CLEAR` can be used to remove a value.

* **Automatic solving:**
  The program searches for a valid solution using constraint propagation and backtracking.

* **Efficient candidate management:**
  Row, column, and 3×3 box constraints are represented using compact bit masks, reducing memory usage and improving solving speed.

* **Minimum-candidate branching:**
  When guessing is necessary, the solver selects the empty cell with the fewest possible candidates first. This substantially reduces the search space.

* **Non-recursive search:**
  The solver uses an explicit branch stack instead of deep recursive function calls, helping avoid TI-89 stack and memory limitations.

* **Checkpoint support:**
  The current solving state can be saved so that a long calculation can be interrupted and resumed later without restarting the search.

* **Minimal interface:**
  The screen is kept simple, showing essentially only the Sudoku grid and the current solving state.

* **Safe reset:**
  Clearing the entire puzzle requires a deliberate key combination and confirmation sequence, reducing the risk of accidentally deleting the entered puzzle.
