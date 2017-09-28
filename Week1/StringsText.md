## Learning Objectives
- Students should know what property to use to find the length of a string.
- Students should understand the difference between the length of a string and the number of the last index.
- Students should understand when and how to use the listed string methods.

## Topics
#### String Basics
  - Like an array of characters
  - `.Length`

#### Escaping Special Characters
  - tab `\t`
  - new line `\n`
  - backslash `\\`
  - bell sound `\a`

#### Comparing Strings for Equality
  - `==` vs. `.Equals(...)`

#### Concatenation 
  - `+` vs. `string.Concat(...)`

#### String Methods
  - Trim()
  - ToString()
  - ToUpper()
  - ToLower()
  - IndexOf()
  - LastIndexOf()
  - Substring()
  - Remove()
  - Split() **We'll come back to this when we get to arrays.
  - Replace()

## Resources & Practice Problems
- [Strings & Text Slides](https://docs.google.com/presentation/d/1s_6Fv0zKtNI53nvYdnBS-8ywgEkvuoWlwcR5JikHE4g/edit?usp=sharing)
- [Strings Resource](http://www.completecsharptutorial.com/csharp-articles/csharp-string-function/)

- .Length Property
  - Find the length of your first name and print it.
  - Find the length of your last name and print it.
  - If the first name is longer than the last name, print "First is longer."
  - If the first name and last name are the same length, print "Samesies!"
  - Otherwise, print "last must be longer!"
  - EXTENSION: Get user input for the first and last name instead of hardcoding, such as `string fName = "Mary";`
  
- Escaping Special Characters
  - Using the escape sequences for tab, backslash, new line, and bell sound, print this result using only ONE `Console.WriteLine(...)`.
  *See result [here](https://github.com/WeCanCodeIT/WCCI-Spring2017-CLE/blob/master/Images/CharacterEscaping.png)*

- Comparing Strings for Equality
  *First try the following using `==` and then try it using `.Equals()`
  - Create a variable and assign a person's first name to it.
  - Create a variable and assign a different person's first name to it.
  - If the two names are the same, print "The names are the same."
  - If they're not the same, print "The names are different."

- Concatenation 
  *First try the following using `+` and then try it using `.Concat()`

  - Ask the user for his/her first name.
  - Ask the user for his/her last name.
  - Using concatenation, print the user's full name including a space to separate the names.
  
- String Methods
  - Ask the user to guess the type of pet (Hint to the user it's the opposite of a dog)
  - Assign an answer variable to the answer of cat.
  - If they guess cat correctly, print "You guessed correctly!"
  - If they guess incorrectly, print "You guessed incorrectly..."
  - Use the `ToLower()` or `ToUpper()` methods to ensure if they enter cat or CAT or Cat, it will be correct.


## Homework
- Continue class exercises.
