# SQL
## Description
  - What is SQL?
  - What is a query?


### What are queries?
- Up until now we've been designing and modifying our database via SQL Server Management Studio(SSMS)
    - SQL management studio gives us a lot of useful features and helps us visualize our database, but it has a lot of limitations
    - We can write SQL queries to utilize interface with our database directly. This grants us a lot more power, flexibility, features.
        - Note: When writing SQL queries directly a lot of the safety features granted by SSMS. Always double check your queries before running!

- Let's practice creating a database by hand. First open up SSMS and create a new database called QueryPractice.
- To start a new query right click your new database and select "New Query". 

    ![New query](/Images/NewQuery.png)
- This opens a new Query Window for us. We can chance the table we are working with the drop down in the top left. 
![Table selector](/Images/TableSelector.png)

    Be sure your query window says QueryPractice.
    
- We are able to enter our queries into this window. There are two way we can run our transactions in this query window.
    - Each time we hit the red "Execute" button, or we hit the F5 key it will run all SQL commands in our query window.
    - Another common way to execute queries is to select a line or lines that contain SQL commands and hit the red "Execute" button, or the F5 key. This will only run the selected lines. This can be useful if you have a number of different SQL commands, you don't need to create a new query window for each new set of commands. 
        - BUT, you need to be very careful to make sure you _ALWAYS_ have something selected or else it will run every command in your query window.
- Formatting SQL: SQL is non case sensitive, but it's convention to write all the the SQL specific keywords in all uppercase. We can end our statements with a semicolon(;). They aren't always required and our query will probably work without them, but it is the standard to include them. We can break our SQL into as many lines as we like, people like to format their SQL queries in different ways. 

### Queries
- We'll be creating a database to help track the menu items as a restaurant. 
- Lets start with a query to create a new table:

#### Creating a table
```SQL
CREATE TABLE MenuItem(
    MenuItemID int IDENTITY(1,1) NOT NULL,
    ItemName varchar(50) NOT NULL,
    ItemDescription varchar(50) NULL,
    Price float NULL,
    CONSTRAINT PK_MenuID PRIMARY KEY CLUSTERED (MenuItemID)
)
```
- Before you run the preceding query take some time to discuss the command with your neighbor. What looks the same? What looks different? Do you notice anything familiar?

- Now, add query into your query window and run. If everything ran successfully you should get the following message: `Command(s) completed successfully.`

#### INSERT 
- Now that we have a table lets insert some data into it. We can use the `INSERT` command to do that.


- Before running the INSERT command take some time to review these commands. Take note at how we list each column we want to _insert_ into, separated by commas. Then in the next section we list each of the values to be inserted into the columns.
```SQL
INSERT INTO MenuItem ([ItemName],[ItemDescription],[Price]) VALUES ('Hamburger','Angus beef', 12.00);
INSERT INTO MenuItem ([ItemName],[Price]) VALUES ('Salad',7.00);
INSERT INTO MenuItem ([ItemName],[ItemDescription],[Price]) VALUES ('Cheese','Swiss', 5.00);
INSERT INTO MenuItem ([ItemName],[ItemDescription],[Price]) VALUES ('Hamburger','Black Bean Burger', 8.00);
```
- After performing the operation you should see the following message: `(1 row(s) affected)`, once per insert statement.

### SELECT

- Now that we have some info in the database how do we view it? Let's start with the following SELECT statement

```SQL
SELECT * FROM MenuItem;
```

- It starts out with the SELECT keyword. The next part is the asterisk (*), this means we will pull back _all_ columns for the table. Which table exactly? The FROM keyword is what we use to designate which table we're selecting from. And FROM is followed with the table we're selecting from. In this case its our `MenuItem` table.

- How else can we select things? If we don't need all columns, we can specify exactly which columns we want to pull information from. Here is how we select just the ItemName and the Price columns that.

```SQL
SELECT ItemName,Price FROM MenuItem;
```

- There's a lot more we can do with select statements. Work together through the following queries:


```SQL
/*If we want to make sure we don't get any duplicates we can use DISTINCT*/
SELECT DISTINCT ItemName FROM MenuItem;


/*We can use COUNT to sum the total items in a column. We can use it with DISTINCT to make sure we're only counting unique values*/
SELECT COUNT(DISTINCT ItemName) FROM MenuItem;


/*We can use AVG to calculate the average value of a column*/
SELECT AVG(Price)
FROM MenuItem;


/*WHERE lets us further define what we're selecting. We can use conditionals similar to an "if" statement in C#*/
SELECT * FROM MenuItem WHERE ItemName = 'Hamburger'
SELECT * FROM MenuItem WHERE MenuItemID = 1;

/*It's also fairly common to see a SQL statement split up where each part is on a new line for readability*/
SELECT * FROM MenuItem 
WHERE ItemName = 'Hamburger'


/*We can use WHERE to determine when things are not equal as well. Both statements are equivalent, the second uses a SQL specific form*/
SELECT * FROM MenuItem WHERE ItemName != 'Hamburger'
SELECT * FROM MenuItem WHERE ItemName <> 'Hamburger'


/*We can compare using SELECT, just like in C#*/
SELECT * FROM MenuItem WHERE Price > 7;


/*We can use the keyword AND to create range to compare with.*/
SELECT * FROM MenuItem WHERE Price BETWEEN 7 AND 9;


/*We can use ORDER BY and ASC to order our results in ascending order*/
SELECT * FROM MenuItem ORDER BY Price ASC;

/*We can also use ORDER BY and DESC to order our results in descending order*/
SELECT * FROM MenuItem ORDER BY Price DESC;
```

- The wildcard character in SQL is the percentage sign %. We can use it like in the following example.

```SQL
/*Here we are using the LIKE and the wildcard character(%) to match the remainder of a string.*/
SELECT * from MenuItem WHERE ItemName LIKE 'Ham%';


/*Finally, we can combine everything we've learned in a query like the following. Have fun experimenting!*/
SELECT AVG(Price)
FROM MenuItem
WHERE ItemName LIKE 'Ham%';
 ```
### UPDATE
- We've learned how to insert data. What if we want to update the values? We have a lot of different ways of performing updates. The following update will find all the Hamburgers and change their price to 14.0

```SQL
UPDATE MenuItem  
    SET Price = 14.0  
    WHERE ItemName = 'Hamburger'
```

### DELETE
- We also have a DELETE keyword that removes data. We need to give it a condition, this is how it finds the data(rows) it should delete. NOTE: Be very careful with the DELETE command. There is no _undo_, so once the data is gone. It's gone! So just remember to double check before you delete, and don't leave any extra DELETE commands in your query window.

```SQL
DELETE FROM MenuItem
WHERE ItemName = 'Hamburger';
```

### Other commands
- There are many other SQL commands to learn but these are the most common. There are resources at the end of this page that point towards places to learn more about SQL commands.

---

### Relationships
- We know that Microsoft SQL Server is a _Relational_ database. How can we define a foreign key relationship using SQL queries?

- Before we begin we need to delete the table we've been using so far. Don't worry, using SQL queries we can quickly, delete, recreate, and populate our databases tables with information. To delete our table we can run the following command.

```SQL
DROP TABLE MenuItem
```

- Now lets create a two new tables with a foreign key relationship. Take some time to study the following example before proceeding.
```SQL
CREATE TABLE Category(
	CategoryID int IDENTITY(1,1) NOT NULL,
	Name varchar(50) NOT NULL,
	CONSTRAINT PK_CategoryID PRIMARY KEY CLUSTERED (CategoryID)

)

CREATE TABLE MenuItem(
	MenuItemID int IDENTITY(1,1) NOT NULL,
	ItemName varchar(50) NOT NULL,
    ItemDescription varchar(50) NULL,
    Price float NULL,
    Category int NOT NULL,
	CONSTRAINT PK_MenuID PRIMARY KEY CLUSTERED (MenuItemID),
    CONSTRAINT FK_PRODUCT foreign key (Category) references Category(CategoryID)
)
```
- Can you see the relationship between the two tables? 

- We're almost ready to start using our new tables. Before we can use our MenuItem table, we need to add data into our Category table.

```SQL
INSERT INTO Category ([Name]) VALUES ('Dinner');
```

- Now that we have at least one category we can add new menu items. Can you tell what's different with these INSERT statements?
```SQL
INSERT INTO MenuItem ([ItemName],[ItemDescription],[Price],[Category]) VALUES ('Hamburger','Angus beef', 12.00,1);
INSERT INTO MenuItem ([ItemName],[Price],[Category]) VALUES ('Salad',7.00,1);
INSERT INTO MenuItem ([ItemName],[ItemDescription],[Price],[Category]) VALUES ('Cheese','Swiss', 5.00,1);
INSERT INTO MenuItem ([ItemName],[ItemDescription],[Price],[Category]) VALUES ('Hamburger','Black Bean Burger', 8.00,1);
```
### Do It
- Practice using different SQL commands to insert, update, delete and select row from your table. Try calculating different values based on the information stored in your tables.

---

### Joins
- Joins are a way for us to group related information together. You can think about them like the linking tables we've used before, but they are not permanent. The joins are a transaction we can use in a query. It allows us to have flexibility in how we group and associate our information.

- An inner join is the most common type of join. There are other types of joins as well, they all function similarly but are used for asking slightly different types of questions.

### Reflect on it
- Resources
- [SQL Tutorial](https://www.w3schools.com/sql/default.asp)
- [Different Types of Joins](https://www.w3schools.com/sql/sql_join.asp)
- [Interactive SQL Zoo Tutorial](https://sqlzoo.net/)
- [SQL Server Tutorial](https://www.techonthenet.com/sql_server/index.php)
- [Relational Databases and Database Design](https://docs.google.com/presentation/d/1C22bQhknL34QW85iaMa5mumTprDXnzk279ErWFOo45I/edit?usp=sharing)
- [Step-by-Step Written Tutorial on Database-First MVC](https://docs.microsoft.com/en-us/aspnet/mvc/overview/getting-started/database-first-development/creating-the-web-application)
