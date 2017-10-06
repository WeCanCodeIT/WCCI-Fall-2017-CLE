# Lucky Numbers
## Due: Monday, October 9, 2017 By 9:30 AM
### - [GitHub Submission Link](https://docs.google.com/forms/d/e/1FAIpQLScUEvl_ZgH_OgBu0zbg_WIvB6zBSkkXh7wfxqjv4LwLdBDxLg/viewform)
  - Correct GitHub link must be submitted on time, or the project will be considered late/not submitted.
  - GitHub repository must be created from correct folder and contain solution file, or the project will be considered late/not submitted.
## Overview
Develop a console application that will be a lucky numbers guessing game similar to the lottery. The user will choose a range of numbers and then try to guess all 6 of the numbers that will be randomly generated within the range. The user will win a portion of the jackpot based on the number of numbers guessed correctly.

## Skills Required
-  Variables and Basic Types
-  Operators and Expressions
-  Conditionals
-  Loops
-  Arrays
-  Math Random (Not to be graded)

## Tasks

### Part 1
- [ ] Ask the user for a starting number for the lowest number in the number range.
- [ ] Ask the user for an ending number for the highest number in the number range.
- [ ] Ask the user to guess the 6 numbers the user thinks will be the lucky numbers generated within the number range.
    - [ ] Numbers must be stored in an array
    - [ ] Array must be populated using a loop
- [ ] If the user enters a number that is outside of the range set, prompt the user to give you a valid number. Do this until the user enters a valid number.

### Part 2
- [ ] The program should randomly generate 6 numbers using a loop
- [ ] The randomly generated numbers should be stored in an array
- [ ] Numbers should be displayed to the console as such and using a loop (Numbers below are for example only. Format must be exact):
  ```
  Lucky Number: 12
  Lucky Number: 47
  Lucky Number: 28
  Lucky Number: 3
  Lucky Number: 19
  Lucky Number: 35
  ```
  
### Part 3
- [ ] Hard-code a value for the jackpot amount and let the user know what the jackpot amount is at some point you decide in the program.
- [ ] The program should count the number of correctly guessed numbers and output console how many were correct to notify the user. Example:
  ```
  You guessed 3 numbers correctly!
  ```
- [ ] The program should calculate the user's winnings based on the number of numbers guessed correctly. e.g If the user correctly guessed 2 out of the 6 numbers correctly the program will calculate .33 of the total jackpot the winnings.
- [ ] The user's winnings should be output to the console. Example:
  ```
  You won $256,877.23!
  ```

  
### Part 4
- [ ] Ask the user if the user would like to play again.
- [ ] If the user says yes, then the program should run again from the beginning.
- [ ] If the user says no, then the program should say "Thanks for playing!" (Must be exact statement).

## Stretch Tasks:
- [ ] Make your program ensure none of the generated numbers are repeated. For example, the following is a valid output:
  ```
  Lucky Number: 12
  Lucky Number: 47
  Lucky Number: 28
  Lucky Number: 3
  Lucky Number: 19
  Lucky Number: 35
  ```
  But, the following output is invalid because 12 is generated twice.
    ```
  Lucky Number: 12
  Lucky Number: 47
  Lucky Number: 28
  Lucky Number: 3
  Lucky Number: 19
  Lucky Number: 12
  ```
  If there is a repeated number, replace it with a new number. Do this until there are no repeated numbers.
