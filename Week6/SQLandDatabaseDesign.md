# SQL
## Description
  - What is SQL?
  - What is a Relational Database?
  - Why do we use SQL?
  - Where do we use SQL?


### What is a database?
- Databases are a way for us to store data in an organized manner. 
    - Discuss what types of databases you encounter every day.

- We will be using SQL. SQL stands for Structured Query Language. SQL is a relational database. Relational databases are largely based on set theory in mathematics. They hold sets of information in tables composed of fields (columns) and records (rows). Tables are related to one another by key fields that are unique to a given record.

### Relational Databases
- Relational Databases are made up of tables. You can think of tables like an excel spreadsheet. Like a spreadsheet a table as columns, each column has a name and a type(similar to a datatype in C#). Rows are contain the actual data for multiple columns. Each individual entry is a field.

- When designing a database we are said to be designing the schema. A schema means the layout of the of the columns, fields and other parts of the database. We can use Primary Keys as a unique identifier for each row that is created. That way not matter what, we can be confident a referenced row is the same. image

- One of the most important parts of designing a database it to make sure the information is not duplicated when it's stored. Often times we will have multiple related tables that need to reference the same information. We can use foreign keys to reference information from other tables and describe relationships. This is where relational databases get their name. There are different types of relationships we'll talk about a bit later.


## Guidelines for designing database tables
- Each table has a unique identifier; i.e., primary key.
- Each field in a table describes a concept associated with what the table represents.
- The fields are deconstructed to the degree that you might search on / report the data (e.g., instead of address, use street, city, state, and zip). 
- Do not repeat data fields -- this is a bad practice. 


### Different database relationships
- There are different types of database relationships we can model between our tables.
    - One-to-one
    - One-to-many
    - Many-to-many


### Do It

- Name the types of relationship
    - Biological Mother and Children
    - US Resident and Social Security Number
    - Parents and Children
    - Cars and Drivers
    - Students and Classes
    - Lead Instructor and Classes

- Design a database called FamilyHomes
    - There could be multiple people living in a home, but each person only lives in one home.

    - Each home has a street address, city,  state, and zip (assume US is the country). Each person has a first name, last name, and address.

- Design a database
    - Design a database with at least 3 tables. Try to model a simple organization you see in everyday life, like Families.

    - Don’t over think it. You’ll soon see how you can continue to model more complex relationships. Keep it to a minimum.
    
    - Make sure to mark your primary and foreign keys in tables, and make sure you identify relationships between tables. Do not repeat data -- instead use foreign keys.  Try and implement it in SQL Server Management Studio.

- Create one table to collect Employee Information for a new hire. What fields would you include? What data types for those fields 
  should you use?
- Design two tables that demonstrate the relationship between an individual author and her book, with at least four fields in each table.
- Design three tables to illustrate the following relationship: 
  - An animal shelter needs to keep track of their adoptions. 
    - They would like to keep information for each animal (type of animal, breed, and three other fields) 
    - Each family who is adopting (whether or not they have a fenced in yard, if they have other pets, and three other fields) 
    - And a record of each adoption (which family adopted which animal, the date of the adoption, and three other fields). 
    


- [Relational Databases and Database Design](https://docs.google.com/presentation/d/1C22bQhknL34QW85iaMa5mumTprDXnzk279ErWFOo45I/edit#slide=id.p)

## More SQL
- If you want a more in-depth understanding of SQL, we recommend checking out this tutorial. It can take several days to get through, but it can also be extremely helpful in preparing for tech interviews. [SQL Tutorial](https://github.com/WeCanCodeIT/SQLTutorial)
