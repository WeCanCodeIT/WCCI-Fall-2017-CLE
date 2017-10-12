## High St. Hospital

### Objective

Students will employ software design principles in order to create a class hierarchy using inheritance and polymorphism 

## The Scenario

High St. Hospital is an organizational mess.  They have unkempt files of employee information scattered throughout manilla folders, computer data files, and old tin filing cabinets.  With the madness of the daily grind, patients are the priority.  But the utmost care cannot be given to the patients if the hospital is disorganized.  High St. Hospital wants to get it together.  They have subcontracted We Can Code IT full-stack apprentices to come in and organize.  They enable you to set up shop with a few company laptops in an old disheveled break room.  Your mission is to create a set of classes that contain information on the employees at Hammond Hospital:

High St. Hospital has the following categorical positions in its facility:
-	A generic Hospital Employee
-	Doctor
-	Nurse
-	Surgeon
-	Receptionist

Include methods in each class that are named according to the services provided by that person and that print appropriate messages.  The program class will be used to enter in the names of the employees at Hammond Hospital and print out appropriate information.

## The Data
The following information will need to be taken care of for each employee:

- **Hospital Employee**: Employee Name, Employee Number
- **Doctor**: Employee Name, Employee Number, Specialty Area (Heart, Brain, Foot, etc…)
- **Surgeon**: Employee Name, Employee Number, Specialty Area, and whether they are operating or not)
- **Nurse**: Employee Name, Employee Number, Department, and Number of Patients they are taking care of
- **Receptionist**: Employee Name, Employee Number, Department, whether they are on the phone or not



### Part 1 

Let's get organized.  Your team is meeting for the first time at High St. Hospital.  Programming at this time is out of the question.  You need to get a feel for the task at hand.  You do not even want to create an algorithm yet.  

Diagram the classes you will need for this program.  What are the inheritance relationships?  How and where does the problem tell you this information?

### Part 2

We can stare at this stuff all we want but until we actually make some software, High St. Hospital will have patients that are not being served with the best possible care. Time is of the essence! Hurry up, but take your time...

#### Our first iteration of this new software might look similar to this...

```
High St. Hospital Employees: 

Jenny	234	Heart  operating false
Meredith	645	Brain	 operating true
Sonny	789 Nursing	 6 patients
Tom	951	Office	on phone true
Anthony	123	Nursing	 4 patients
```

### Part 3
- Stretch task: Using Polymorphism let's pay our employees (getPaid() method)
- Stretch task: Place our employees in a collection
- Stretch task: Through user input, type search for an employee by name and access their info/what they are doing
