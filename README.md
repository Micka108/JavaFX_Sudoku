# JavaFX_Sudoku
Cours UQAC IA

![alt text]()

**Objective**

Fill a 9x9 grid with digits

**Rules**
1. Each row contains the numbers 1 to 9
2. Each column contains the numbers 1 to 9
3. Each box contains the numbers 1 to 9


## Binary Constraint Satisfaction Problem

### Variables

Variable for each tile in the sudoku grid with a total of 81 variables. Variable is a combination of a letter indicating the row, and a digit indicating the column. 

X = {X<sub>1</sub>, X<sub>2</sub>, ..., X<sub>81</sub>}

### Domains

Each variable X<sub>i</sub> has the domain of the digits [1,9]

D = {D<sub>1</sub>, D<sub>2</sub>, ..., D<sub>81</sub>}

D<sub>i</sub> = {1, 2, 3, 4, 5, 6, 7, 8, 9}

### Constraints

The value of each variable X<sub>i</sub> cannot be equal to any value in its:
- Row
- Column
- Box

![alt text]()

## Algorithm

### Minimum Remaining Values heuristic (MRV)

Searches for variables with the smallest domains

In this example, the grayed cells are the mrv of the grid
![alt text]()

### Degree Heuristic (DH)

Searche the variable with the largest degree

### Least Constraining Value heuristic (LCV)

Sorts the domain of a variable taking into account the constraints of its neighbours

### Arc Consistency algorithm #3 (AC-3)

First, the AC-3 (arc-consistency checking) algorithm will be implemented. This algorithm will propagate the constraints and reduce the domain size of the variables by ensuring all possible (future) assignments consistent. As can be seen, very few of the puzzles can be solved by using this algorithm alone, as expected

## File

Using a file to add a grid to sudoku can be done with the Load file button. The file must respect the following path **src/file/sudoku.txt**, and must respect the architecture shown in the image below

![alt text]()

## Further information

The stop button does not work at the moment 