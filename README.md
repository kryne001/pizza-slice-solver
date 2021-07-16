# Pizza Slice Instant Insanity solver and Minimum Obstacle finder

## Description

A pizza slice instanty insanity game in which <code>n</code> pizza slices, each with 3 sides that display a number, are stacked on top of each other. Goal is rotate the pizzas in such a way that each face down the stack displays a unique number. If there is no possible solution, there is a minimum subset of slices that when grouped together is unsolvable.

## Functionality

Currently has hard coded formulas to generate puzzles of <code>n = 30</code> pizzas. Will then first check if generated pizza is able to solve, then if unsolvable will check every possible subset of n = 2 to 30 to determine a minimum obstacle. Once an obstacle is found, program will end. 

## How to run

Download repository, run in either an IDE or through terminal with <code>python3 main.py</code> bash command when in directory. 

**IF NEED TO CHANGE FOR SPECIFIC CASES:**

different formulas:  

lines 4 - 11, change the formulas to fit your specifications. Comment out any unwanted puzzles. <code>puzzleFunctions</code> on line 12 is an array that holds the puzzles to be generated, so add or subtract puzzles to be tested from array. 

different size:

line 14: change <code>count = np.zeros(30)</code> to <code>count = np.zeros(n)</code>, replacing <code>n</code> with number of slices.  
line 18: change <code>puzzleMatrix[29,2]</code> to <code>puzzleMatrix[n-1,2]</code>, with <code>n</code> being the size of desired puzzle.  
line 58-59: change 30 to number of slices in desired puzzle. 
line 118: change 30 to number of slices in desired puzzle. 
line 135: change to <code>range(2, n)</code>, replacing n with number of slices in desired puzzle. 

## Bugs

Currently will be a memory size problem which stops program once done checking subsets of size 1 - 12.   
**WORKAROUND:** change the range in line 135 to be a single number, e.g. <code>range(13,14)</code> for each subset 13 <= n <= 17. 

Does not work for already-generated puzzles, e.g. puzzles already created.    
**WORKAROUND:** Line 123, assign a hardcoded numpy array to <code>puzzle</code> and comment out line 124. 
example: <code>puzzle = np.array([[1, 2, 3], [4, 5, 6], [6, 4, 5]])</code> then follow steps to handle changing code to specific puzzle size. 

