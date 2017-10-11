## Topics
#### What is inheritance?
- Base Class (Parent Class)
- Derived Class (Child Class)
- Protected access modifier
- base keyword
- Abstraction

#### What is polymorphism?
- Virtual 
- Override 
- Base
- Abstract class 
- Method OverLoading

## Description
- Inheritance simply means a parent-child relationship. 
- Think about how a child may inherit properties like eye color from a parent
- By using inheritance in C#, we can create a new class by using an existing class
  - This allows us to be able to reuse properties and methods of the original class in our new class
  - For example, let's say we have a Transportation parent or base class. We could create new classes/child or derived classes from our Transportation class, such as a Car class, a Motorcycle class, and a Boat class.
  - What properties and methods might our derived classes inherit from our base Transportation class?
    - Capacity (property)
    - Turn (method)
    - Go (method)
    - Reverse (method)
    - Stop (method)
- This is where polymorphism comes into play. Polymorphism comes from the roots Poly meaning many and Morph meaning form. In programming, polymorphism refers to the same method being implemented in different ways. So, for example:
  - The Turn method could be called on a Boat object, a Motorcycle Object, or a Car object. However, the method may function differently depending on which object is calling the method. A car turns differently, than a boat, and a so on.

## Do It
- [In Class Slides](https://docs.google.com/presentation/d/17WM4gT6L5uKMIbb3vCOULNriJxLvPVUruUKOxVZU9Ew/edit?usp=sharing)

## Student Resources & Practice Problems
- C# Player's Guide: Chapter 21 Inheritance
- C# Player's Guide: Chapter 22 Polymorphism Virtual Methods, Abstract Classes
- [Polymorphism MSDN](https://msdn.microsoft.com/en-us/library/ms173152.aspx)
- [Virtual Methods](https://www.dotnetperls.com/virtual)
- [Inheritance](https://www.dotnetperls.com/inheritance)
- [Polymorphism C# Corner](http://www.c-sharpcorner.com/UploadFile/puranindia/polymorphism-in-C-Sharp/)
- [Base Keyword](https://www.dotnetperls.com/base)
