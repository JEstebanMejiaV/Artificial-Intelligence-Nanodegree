# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Introductory Project: Diagonal Sudoku Solver

## Question 1 (Naked Twins)

Q: How do we use constraint propagation to solve the naked twins problem?  
A: we first find pairs of identical values within each unit. To do this, we first identify potential candidates and match them in pairs (using sorting and grouping by value). After this, we simply remove the digits of the naked-twin pair from the other boxes in the unit. By repeatedly applying this constraint until the Sudoku puzzle stops changing.


## Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: we perform constraint propagation by repeatedly enforcing the strategy rules (the constraints), reducing the set of possible values toward a possible solution for the Sudoku. To solve the diagonal sudoku problem, we actually do not need to modify the constraint propagation code itself. The constraint propagation code does not actually care where each unit is located in the puzzle. It only needs to know which units it needs to transform. To add support for the diagonal constraint, we only had to create two additional units that represent the diagonals of the grid.

A brief explanation of constraint propagation. Constraint propagation is about reducing the number of possibilities, is the process of finding a solution to a set of constraints that impose conditions that variables must satisfy(new rules or constraints). A solution is therefore a set of values for the variables that satisfies all constraints. To converge toward that set of values, we repeatedly enforce the strategy rules, reducing the set of possible values toward a possible solution for the Sudoku.

 ##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solution.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the `assign_value` function provided in solution.py

### Submission
Before submitting your solution to a reviewer, you are required to submit your project to Udacity's Project Assistant, which will provide some initial feedback.  

The setup is simple.  If you have not installed the client tool already, then you may do so with the command `pip install udacity-pa`.  

To submit your code to the project assistant, run `udacity submit` from within the top-level directory of this project.  You will be prompted for a username and password.  If you login using google or facebook, visit [this link](https://project-assistant.udacity.com/auth_tokens/jwt_login) for alternate login instructions.

This process will create a zipfile in your top-level directory named sudoku-<id>.zip.  This is the file that you should submit to the Udacity reviews system.
