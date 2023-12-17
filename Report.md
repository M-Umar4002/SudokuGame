# Project

## Members:

### Muhammad Abser Mansoor (23K-0030): Initialization of sudoku boards
### Syed Fahad Faheem Shah (23k-0062): Validation of sudoku boards and Save state feature
### Muhammad Umar (23K-0023): Input and Output

## Main Idea: Create a Sudoku game with multiple difficulties using C.

## Input: 
The very first input will be the selection of difficulty using a char input of E, M or H pertaining to Easy, Medium, and Hard difficulties respectively.
After selection of difficulty, the user will be prompted to enter coordinates for the desired position they want to modify and will then be able to modify the value at those coordinates, although the clues generated at the start of the matrix creation cannot be modified.

## Working:

After selection of difficulty, one of 3 starting matrices will be chosen pertaining to each difficulty, starting from a 6x6 with 14 clues then a 9x9 with 22 clues and then a 12x12 with 37 clues. These clues will be filled in by the computer which will randomly choose a number between 1 and 9, inclusive, whilst also obeying the rules of sudoku. After clue insertion, those values cannot be changed by the user. The checking for conformity to the rules of sudoku will be done by separate functions after each clue is inserted and each input is given.
## UI: 
User will be asked for difficulty selection and the starting matrix with the clues filled in will be shown after which they will be asked to input coordinates and then input a value at those coordinates. After each input the modified matrix will be displayed and the user will have the ability to replace previously inputted values.

## Future plan:
As planned, a save state feature has been added along with 2 new difficulties and more user friendly interface.

## No Data Structures were used.

## Difficulties:
**Abser:**
Initialisation of the matrices required the creation of checking conditions and the checking conditions I used were not working. There was only a syntax error which was that I was passing the 2d array as both a pointer and an array and obviously that was incorrect. This was solved after my teammates found the problem at first glance despite my rigorous checks.

**Fahad:**
I faced problems while creating the save state feature as our matrix is character based but when the matrix was being loaded the sizes and data was required to be in integer format therefore juggling 3 different matrices with 3 sizes (for each difficulty) whilst keeping track of the datatypes proved difficult. This was solved when I realised how fscanf treated spaces.

**Umar:**
Since my work depended upon calling the functions of my teammates and handling the arguements for the final product, it proved difficult to properly connect all the different functions and their arguements for a coherent code. This required time to properly understand the different functions although there was not much logically wrong in my work.

##Algorithm:
The way this code works is as follows:-
1. An initial matrix is created containing random values between 1 and 9 (inclusive) and this is done using the checking functions.
2. The player is shown this matrix and asked for input (first the position then the value). For every following input the player will also be asked if they want to replace or add onto the matrix.
3. Following the value input, the value is passed through the checking condition functions which check if there are any duplicates present in the same row, column or subblock. If yes, then the value is rejected and user is prompted to input again. If no, then the value is stored in the user picked position.
4. After the user fills in the matrix, a final check function is used to determine if the board is valid and complete and accordingly declares victory or failure.
