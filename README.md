# comp30020-assn2
Assignment 2 for COMP30020 - Declarative Programming. A solver for a 'Maths puzzle' written in Prolog

# Overview
This is completed code for Project 2 for the University of Melbourne subject COMP30020 - Declarative Programming. The aim to is to write Prolog code which can take a 'Maths Puzzle', as defined below, and return a filled-in puzzle which satisfies the defined constraints; i.e. a completed puzzle. SWI Prolog's constraint programming library, clpfd, and higher order functions were used to write succint, performant code, and to avoid Prolog searching possible assignments until the size of each variable/square's domain has been minimised.

# Usage
Load up SWI Prolog and load in the proj2_test.pl file with: `[proj2_test].`.
Run tests by typing `do_tests.` and pressing enter/return.

# Maths Puzzle
### Game Description
A maths puzzle is a square grid of squares, each to be filled in with a 
single digit 1–9 (zero is not permitted) satisfying these constraints:
  - each row and each column contains no repeated digits;
  - all squares on the diagonal line from upper left to lower right contain
    the same value; and
  - the heading of reach row and column (leftmost square in a row and topmost
    square in a column) holds either the sum or the product of all the digits
    in that row or column.

Note that the row and column headings are not considered to be part of the
row or column, and so may be filled with a number larger than a single digit.
The upper left corner of the puzzle is not meaningful. 

### Format
When the puzzle is originally posed, most or all of the squares will be
empty, with the headings filled in. The goal of the puzzle is to fill in all 
the squares according to the rules. A proper maths puzzle will have at most
one solution.

Here is an example puzzle as posed (left) and solved (right):
```
 ____ ____ ____ ____    ____ ____ ____ ____ 
|    | 14 | 10 | 35 |  |    | 14 | 10 | 35 |
| 14 |    |    |    |  | 14 |  7 |  2 |  1 |
| 15 |    |    |    |  | 15 |  3 |  7 |  5 |
| 28 |    |    |    |  | 28 |  1 |  1 |  7 |
 ---- ---- ---- ----    ---- ---- ---- ----  
```
 (^ As shown in the Project Specification)

The 'Puzzle' referred to in predicates defined below is an NxN list of lists
of equal length that fit the specification above and below.

### Input Format
A maths puzzle (Puzzle) will be represented as a lists of lists, each of the 
same length, representing a single row of the puzzle. The first element of 
each list is considered to be the header for that row. Each element but the
first list in the puzzle is considered to be the header of the corresponding
column of the puzzle. The first element of the first element of the list is 
the corner square of the puzzle, and thus is ignored."

### Assumptions
Assumption 1: "When puzzle_solution/1 is called, its argument will be a 
proper list of proper lists, and all the header squares of the puzzle (plus 
the ignored corner square) are bound to integers. Some of the other squares 
in the puzzle may also be bound to integers, but the others will be unbound."

Assumption 2: "This code will only be tested with proper puzzles, which have
at most one solution. If the puzzle is not solvable, the predicate should
fail, and it should never succeed with a puzzle argument that is not a valid
solution."

# Results
Final Mark: 99.00%

Correctness: 70/70 || Code style: 29/30

See feedback.txt for a full description of the results.