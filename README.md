# Subtle ZeroDivisionError in Python despite explicit checks

This repository demonstrates a subtle error where despite explicit checks for division by zero, a function can still raise a ZeroDivisionError. This is due to the way Python evaluates conditional statements.

The `bug.py` file contains the erroneous code. The `bugSolution.py` file provides the corrected version.

## Explanation of the Bug

The original code contains a conditional statement that checks if either x or y is 0 before performing the division. However, if both x and y are 0, the `elif` condition will not be evaluated after the `if` condition is true, and the code proceeds to the `else` block and raises the ZeroDivisionError. 

## Solution

The solution involves rearranging the conditional statements. By putting the condition for checking both x and y being equal to 0 as the first condition, the ZeroDivisionError can be avoided.