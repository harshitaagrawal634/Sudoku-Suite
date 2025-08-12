# Sudoku-Suite

A **header-only C++17-compatible** library that provides essential utilities to **solve, validate, and generate** standard 9x9 Sudoku puzzles.

---

## Features

- Solve puzzles using recursive backtracking  
- Validate Sudoku grids for correctness  
- Generate new puzzles (WIP or extendable)  
- Modular design with clear documentation  

---

## How the Solver Works

The algorithm uses **backtracking**, a popular technique for solving constraint satisfaction problems like Sudoku.

### Step-by-Step Logic

1. Start with the first empty cell.  
2. Generate a list of valid values that can be placed in that cell.  
3. Try the first value from the list and place it.  
4. Move to the next empty cell and repeat.  
5. If no valid value exists for the current cell, **backtrack** to the previous cell and try the next option.  
6. Continue until all 81 cells are filled with valid values.  
7. The puzzle is now solved.  
> The algorithm stops once it reaches the last cell and finds a consistent value.

---

## Running the Tests

You can compile and run the test file using:

```bash
c++ --std=c++17 tests/test_sudoku_suite.cpp -o test_sudoku
./test_sudoku

