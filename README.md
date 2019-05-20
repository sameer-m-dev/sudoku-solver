# sudoku-solver
Python program to solve any Sudoku puzzle automatically

It has 6 functions, namely:
# 1) display
Display the values as a 2-D grid.

# 2) grid_values
Convert grid string into {<box>: <value>} dict with '123456789' value for empties.
  
# 3) eliminate
Eliminate values from peers of each box with a single value.
Go through all the boxes, and whenever there is a box with a single value, eliminate this value from the set of values of all its peers.

# 4) only_choice
Finalize all values that are the only choice for a unit.
Go through all the units, and whenever there is a unit with a value that only fits in one box, assign the value to this box.

# 5) reduce_puzzle
Iterate through eliminate() and only_choice(). If at some point, there is a box with no available values, return False.
If the sudoku is solved, return the sudoku.
If after an iteration of both functions, the sudoku remains the same, return the sudoku.

# 6) search
Using depth-first search and propagation, try all possible values.
Creates seperate branch for every possible value and returns the branch that solves the sudoku.
