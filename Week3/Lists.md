## Topics
#### What is a list?
- How is a list different from an array?
- Syntax

#### Common Properties & Methods
- Count
- Clear
- Add
- Remove
- Sort
- IndexOf
- Contains
- RemoveAt
- Insert

#### Looping through Lists
- For Loop
- Foreach Loop

## Description
- A list is a type of linear data structure.
- A data structure is a way of organizing data that considers not only the items stored, but also their relationship to each other.
- A list is similar to an array. There are a few important similarities and differences to point out:
  - Lists are mutable, which means they can dynamically change in size, whereas arrays have a fixed size
  - Both Lists and Arrays have a property for evaluating the length. In a list it's called `Count`.

## Do It
- Let's create a list of favorite foods.
- When creating a list when you know the items in the list:
  - [EXAMPLE SLIDE](https://github.com/WeCanCodeIT/CSharp-Curriculum-Guide/blob/master/Images/lists.png)
  - Start with the keyword `List`
  - Inside the <> brackets is the data type for the elements being held in the list
    - For our favorite foods list inside the angle brackets would be `<string>`, but if we had a list of numbers we would use `<int>`
  - Next, create a name for your list
  - We are instantiating a new list object, so followed by the = is the keyword `new` and the list constructor
  - Because we know what elements we want in our list, inside the curly braces, we can add our elements
- When creating a list when you don't know the items in the list
  - [EXAMPLE SLIDE](https://github.com/WeCanCodeIT/CSharp-Curriculum-Guide/blob/master/Images/ListAdding.png)
  - Eliminate the curly braces, and instead use the Add method to manually add elements to the list
  ```CSharp
  List<int>luckyNumbers = new List<int>();
  luckyNumbers.Add(2);
  luckyNumbers.Add(3);
  luckyNumbers.Add(5);
  luckyNumbers.Add(7);
  //We now have a list called luckyNumbers that has the integer elements 2, 3, 5, 7
  ```
- Let's get back to creating our list of favorite foods. Following the first example of when you know what the elements are, create a list of your top 5 favorite foods.
  ```CSharp
  List<string>faveFoods = new List<string>(){"steak","chicken","fish","ice cream","nachos"};
  
  //Check your list by printing each element individually
  Console.WriteLine(faveFoods[0]);
  Console.WriteLine(faveFoods[1]);
  Console.WriteLine(faveFoods[4]);
  ```
  
- This time, let's create a list of our least favorite foods based on the second example where the elements are unknown. Use the Add method to add your 5 least favorite foods to the list.
```CSharp
  List<string>leastFaveFoods = new List<string>();
  leastFaveFoods.Add("Brussel Sprouts");
  leastFaveFoods.Add("Beets");
  leastFaveFoods.Add("Shrimp");
```

- Thinking back to our previous example. If we want to change the value stored an an element we can use the following format. In this example we'll take the first element in our `leastFaveFoods` list and change it to pizza.
```CSharp
  leastFaveFoods[0] = "Pizza";
```


- There are built-in methods and properties that can be used with lists.
  - Let's look at the `Count` property and the `Remove` and `Insert` methods.
  - Create a list called `faveFilms` and populate it with the movies Pretty in Pink, The Breakfast Club, and Sixteen Candles.
  ```CSharp
    List<string>faveFilms = new List<string>(){"Pretty in Pink","The Breakfast Club","Sixteen Candles"};
    
    //Let's try using a for loop to print the elements of our faveFilms list.
    for(int counter = 0; counter<faveFilms.Count; counter++)
    {
      Console.WriteLine(faveFilms[counter]);
    }
    //Notice how we use `Count` to find the length of lists
    
    //Now that we've verified our films are in our list, let's use the `Insert` method to add 3 films, Mean Girls, Clueless, and Heathers to the list as the first 3 list items.
    
    //The Insert method has 2 parameters. The first parameter is the index number for the location of where you want the element placed, and the second parameter is the actual value you want added to the list.
    
    faveFilms.Insert(0,"Mean Girls");
    faveFilms.Insert(1,"Clueless");
    faveFilms.Insert(2,"Heathers");
    
    //This time, use a foreach loop to print the elements in the list
    foreach(string film in faveFilms)
    {
      Console.WriteLine(film);
    }
    
    //Now, let's use the Remove method to remove The Breakfast Club and Sixteen Candles.
    faveFilms.Remove("The Breakfast Club");
    faveFilms.Remove("Sixteen Candles");
    
    //Use a foreach loop to print your list.
    foreach(string film in faveFilms)
    {
      Console.WriteLine(film);
    }
  ```
   
   
   
   
## Do It
- Create a List<string>
  - Add five animals using the .Add()
  - Print each animal in the list

- Create the following list:
	- List<bool> boolList = new List<bool>() { true,false, false,  true, false};
  - Loop through each value
  - If the value is true print:    "Better bring an umbrella"
  - If the value is false print:  "No rain today, enjoy the sun!"

- Create a list with the following numbers: 1, 23, 9, 77, 922, 6, 32, 63,14, 5
  - Use the .Contains() method with the following values 23, 77, 15
  - Remove the 4 elements 27, 77, 32 and 6
  - Use the .Contains() method with the following values 23, 77, 15
  
- Come up with an example for how to use each of the methods/properties listed in the Common Properties & Methods section.

## Student Resources & Practice Problems
- [Reference Slides](https://docs.google.com/presentation/d/1QxqlIIKN7rv_-Bud3t_PPU9RjrPIGCAR9gndzBX-3gg/edit?usp=sharing)
- [Syntax Slides](https://docs.google.com/presentation/d/1V-ubPNLHHRuD2_oFo8PaowOR1uWCSZrVvs7jh4Nwclg/edit?usp=sharing)

