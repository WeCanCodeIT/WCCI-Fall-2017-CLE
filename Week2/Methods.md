## Topics
## Goals
- To understand what a method is.
- To understand what a method does.
- To discover the proper way to use a method in programming.
- Understand the key usages of methods.
- Understand `void` methods.
- Understand method construction.

### Methods
 - What is a method?
 - Why would you use a method?
 - When would you use a method?
 - `void` Methods
 - Return types
 - Method Syntax - use parentheses
 
 ### Parts of a method header
- A method header tells you information such as it's name, what information it needs to do it's work, what information it gives you after it's complete, and what code can call it. Lets take a look at a method header.

```csharp
    public int Add(int firstNumber, int secondNumber)
```
 ### Breaking a method header down
- The first part, `public`, is the access modifier. This tells us what parts of the program are allows to call this method. 

- The second part, `int`, is the return type of the method. We will explore the `return` keyword in the next section. After the method is done performing it's work what information is to going to give back to us? This can be any data type we've seen so far, `string`, `int`, `double`. Whatever makes sense for the problem we're trying to solve. The return type can also be complex types as well, so arrays, lists, or even objects.

- Following that is the name of the method. Methods are actions so they can be thought of as verbs in English. In this example it's `Add`. The names of methods are in Pascal Case. The name of the method should always correspond with the action the method is performing. So a method named `Add` shouldn't subtract instead.

- The last part are the parentheses and everything inside. This is where we're able to see what parameters the method needs. Parameters are the information we give to methods in order for them to do their work. Parameters function like _temporary_ variables. They only within the scope of the method, outside the method they don't exist. So if we have any information we want to persist after the method completes we need to

- This can be any data type we've seen so far, `string`, `int`, `double`. Whatever makes sense for the problem we're trying to solve. The return type can also be complex types as well, so arrays, lists, or even objects.

### Method Declaration
- A method header tells us all the information about the method, and what to expect with it. The _method body_ is where the implementation lives. Let's look at our `Add()~ method again with a body. A complete method -header and body- is called a method declaration.

```csharp
    public static int Add(int firstNumber, int secondNumber)
    {
        int sum =  firstNumber + secondNumber;
        
        return sum;
    }
```
- **Note**: We are using the keyword `static` in front of our methods here so we don't need to worry about objects. We will learn more about `static` in a later lesson.

- The method body above starts with calculating the sum. It's using the two parameters passed in. We can use any parameters in our methods to help calculate values. A method can contain as much code as necessary to complete it's task but remember methods should only accomplish one task, they should complete the task that they are named after.

- After the method completes it's work it needs to pass it back to the code that called it. That's where the `return` keyword comes in. We can return a single value, the type of that value must match the return type in the method header. Since the method says we're returning an `int` we need need to make sure we need to return an `int`. 

- In cases where we don't need to return a value we can use the keyword `void` instead. When we have a void return type we don't need to use the keyword `return` in our method.

### Calling Methods

- Now that we understand a how methods are created we need to understand how to call(or invoke) them. We can call methods with their name. If we are in the same class where the method is defined we can simply call it using the name of the method. If we're looking at the at our `Add()` example from earlier we could use the the method like the following:

```csharp
    int answer = Add(5, 7);
```

- In this example we call the method `Add`. But we know from the method header the method takes two int parameters. Each parameter passed into a method is separated by a comma. Here we're passing in the values  5 and 7.

- We know from the method header that this method returns an int. This means once the method is done with it's work we need to store it somewhere. We're storing the result in an `int` variable. If we can use the result any way we like.

- We can call the method from Main. If you've noticed by now Main is a method itself! It's a special method where the program begins running from.

---

Let's look at another method.

```csharp
public static void RobotWarning(string name)
{
    Console.WriteLine("Danger, " + name);
}
```

- Our `RobotWarning()` method takes one parameter which is a name. The return type is `void`, which means that it doesn't need to provide us any information after it's work is complete. We'd call our `RobotWarning()` method like this:
```csharp
    RobotWarning("Will Robinson");
```
- If you remember, since the return type is `void` so there's no information we need to save after the method is complete. So we can simply call the method and expect it to print out the correct output to the console.


### Do It
 - Create a method called FavoriteFood.
    - It should take two `string` parameters. One representing a name, and the other representing a favorite food.
    - The return type should be `void`.
    - The method should concatenate 

- Create a method called RetirementCalculator.
    - It should take an `int` as a parameter representing the users age.
    - The method should calculate how many more years until the user retires using 65 as the age of retirement.
        - The return type should be `void`.
    - Once it calculates the users retirement age it should print `The user will retire in X years`, where X represents the value that was calculated.

- Create a method called WageCalculator.
    - It should take two `double` parameters. One should represent the hours worked and the other represent the hourly wage. The return type should be of type of `double`.
    - The method should calculate the monthly wage.
    - Once it calculates the monthly wage it should 

----

- Create two methods of your choosing. At least one of the methods should have a non-void return type.
    - Both of the methods should take at least one parameter
    - Remember when naming your method that it should represent what your method should do.
    - Your method should only aim to accomplish one thing.

- Reference Materials
  - [Methods](https://docs.google.com/a/wecancodeit.org/presentation/d/1w7U0GGW6oVNJpgPFKjb-iny2EwcrQypZlIvNHsHQKF4/edit?usp=sharing)
  - [Methods Practice Problems](https://docs.google.com/a/wecancodeit.org/presentation/d/1PCziOM-s2T7MU3n9AVP_YKNLyirXO3cqAKLdFnBn9P0/edit?usp=sharing)
  - C# Player's Guide Chapter 15: Methods

- Problems/Projects
  -  [Methods Practice Problems - Problem 4 (Slide 5)](https://docs.google.com/a/wecancodeit.org/presentation/d/1PCziOM-s2T7MU3n9AVP_YKNLyirXO3cqAKLdFnBn9P0/edit?usp=sharing)
  -  [Methods Practice Problems - Problem 5 (Slide 6)](https://docs.google.com/a/wecancodeit.org/presentation/d/1PCziOM-s2T7MU3n9AVP_YKNLyirXO3cqAKLdFnBn9P0/edit?usp=sharing)
