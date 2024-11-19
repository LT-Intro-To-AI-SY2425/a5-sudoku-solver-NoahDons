# Assignment 5 Write up

Assignment 5 can be broken up into the following parts:
1. Import the Necessary Modules:
- `copy`: For creating deep copies of objects
- `Stack` and `Queue`: Custom implementations for DFS and BFS operations
2. Utility Functions: 
- `remove_if_exists`: Removes a specified element from a list if it exists, which is used to remove the possibilites from a cell
3. Board Class:
- Represents the Sudoku board
- Consists of functions that will find the most constrained cell, and update the board, which eliminates possible solutions
4. DFS & BFS Functions:
- `DFS`: Uses depth-first search to solve the Sudoku puzzle. It works by trying to fill the most constrained cell with potential values until a solution is found or backtracks if a mistake is made
- `BFS`: Uses breadth-first search to solve the Sudoku puzzle in a similar fashion to DFS but explores nodes level by level
5. Main Execution:
- Defines two different sets of initial moves for Sudoku puzzles
- Uses both DFS and BFS to solve each puzzle and prints the results


After completing the assignment, answer the following reflection questions:

## Reflection Questions

1. How do the performance and efficiency of the Depth-First Search (DFS) and Breadth-First Search (BFS) algorithms compare when solving Sudoku puzzles? In what scenarios might one approach be preferable over the other?

The efficiency of the depth first search is, in most cases, greater than the breadth first search for sudoku puzzles. Since the solved board is always at the bottom of a tree of potential solutions, the breadth first search will always check almost every possibility every time. The breadth first search is faster however when the depth first search doesnt have one of the first couple of options as the solution.

2. How did the choice of data structures (like the Stack for DFS and Queue for BFS) impact the implementation and functionality of the algorithms? Are there alternative data structures or design patterns that could have been used to achieve the same objectives?

The Algorithm was completely identical. No changes were necessary except for making s=Stack() into s = Queue(). There are probably alternative algorithms that achieve the same goal, but I didn't look for any as the same algorithm worked for both DFS and BFS.


3. Considering the current implementation, how might the Sudoku solver be adapted or extended for larger puzzles or different types of grid-based logic games? How can the lessons learned from this assignment be applied to real-world problem-solving or optimization challenges?

The sudoku solver might need to be adjusted to search through a larger puzzle by changing a few parameters. The current search method should work for any sized puzzle, but it would just take a very long time if the puzzle is big enough. This same algorithm can be applied to real world problems. The values and goal may change, but the algorithm would stay constant.