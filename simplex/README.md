# lpp-simplex-solver
This is a python implementation of the simplex algorithm for solving LPP.

This repository contains the below file:
1. Simplex Method.pdf --> Step-wise instruction handbook for solving a linear programming problem using simplex method.
2. simplex_method_theo.ipynb --> Further theory and the general form of a linear programming problem.
3. simplex.ipynb --> Actual code implementation of simplex algorithm. This code uses the below linear programming problem to solve using simplex algorithm:

$\text{maximize}$ $$3x_1 + x_2 + 2x_3$$

$\text{subject to}$ $$x_1 + x_2 + 3x_3 \leq 30$$

$$2x_1 + 2x_2 + 5x_3 \leq 24$$

$$4x_1 + x_2 + 2x_3 \leq 36$$

$$x_1,\;x_2,\;x_3 \geq 0$$


**Further improvement areas**:
1. The code currently works on a fixed problem and everytime the coefficient matrices $c$, $A$, $b$ need to be changed manually. Further changes to be done in the code so that user can input the coefficient matrices during runtime.

2. In `get_pivot_position()`, during the selection of pivot column it selects the first positive element from the objective function row (last row of the tableau) instead of the maximum positive element from the row. This may impact the number of iterations required, but it doesn't impact the optimal solution.

3. The code only works the linear programming problems already in standard form, meaning that user needs to convert it to standard form manually before feeding the coefficients to this program. A new function to be incorporated which will convert a linear programming problem of any form to a standard form before implementing simlpex algorithm.

4. During showing the final solution vector, it prints the entire set of solution (basic and non-basic) together. However, there should be a provision to print the set of basic solutions and non-basic solutions separately.

5. A new function to be implemented to print and visualize the inequality constraints as well as color code the feasible regions and feasible solutions.

The above points will be implemented in due time and the repository will be updated with the revised code.
