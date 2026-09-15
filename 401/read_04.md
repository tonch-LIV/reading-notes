# 401_Read_04 - Data Modeling

- [noSQL vs SQL](#nosql-vs-sql)
  - [Answers.1](#answers1)
- [SQL Modeling Techniques](#sql-modeling-techniques)
  - [Answers.2](#answers2)
- [SQL vs noSQL - (Video)](#sql-vs-nosql---video)
  - [Answers.3](#answers3)
- [Bookmark and Review](#bookmark-and-review)
- [Things to Learn More About](#things-to-learn-more-about)

## [noSQL vs SQL](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)

Two ways to organize and store information, albeit differenty than one other.  

A SQL DB (database) maintain a structure throughout the tables emplyed and the relationships between them. noSQL DBs use 'documents' rather than tables, and are flexible in realtion to the relatiosnhip between them and for the data stored within as well; they make use of key-value pairs as well as, graphs, and other forms of data.  

Whichever one chooses to use depends on the structure and complexity of the data, the queries that will be made, while also keeping in mind future growth.

### Answers.1

1. What type of database is the best fit for the **complex, query intensive** environment?
    - SQL; powerful tools for filtering, combining related tables, and performing complicated queries.
2. What type of database is the best fit for **hierarchical** data storage?
    - noSQL; information can be stored in a nested-like structure, similar to JS object / JSON.
3. Describe the **differences in scalability** between a SQl and NoSQL database as though you were speaking to a non-technical friend.
    - noSQL grows *horizontally*; as if you get more bread minions to bake / deliver and split the workload between them, simultaneously allowing them to handle more requests.
    - SQL grows *vertically*; as if improve and strengthen the one master baker by upgrading his internal resources (oven, racks, mixer, trays, tables, delivery system, etc.)
      - (*\*NOTE: modern SQL DBs can support horizontal scaling; See [The Geek Stuff](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=chatgpt.com) for more info.*)

## [SQL Modeling Techniques](https://www.essentialsql.com/get-ready-to-learn-sql-7-simplified-data-modeling/)

Before even making tables; one must plan how the information will be divided between the tables and the relationshiop between those tables, this process is known as **Data Modeling**.  

Tools such as diagrams can help illustrate the goal of what a developer(s) are trying to build; what the table is called, and what the columns, keys, and relationships look like.

### Answers.2

1. Among data tables, what is a **one-to-many relationship** and how do we "relate" them?
    - one record in one table connected to various other records in another table.
    - through the use of a *primary key* (from the main table) and a matching *foreign key* (one the corresponding record(s)).
2. Prior to designing your relational database, it might be useful to  \_\_**create**\_\_ a \_\_**diagram**\_\_ of the database tables and their relationships.
3. Explain the difference between a **primary and foreign key**.
    - A primary key is a unique identifier for each record inside the table it resides in.
    - A foreign key, refrences a primary key in another table.

## [SQL vs noSQL - [Video]](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y)

SQL syntax,  
Relation DB schema,  
Normalization,  
Relationships,  
Information divided across tables, but still connected...

### Answers.3

1. How do we treat **keywords** and **parameters** differently in SQL syntax?
    - KEYWORDS (***SELECT***, ***FROM***, ***WHERE***, **INSERT**, **UPDATE**, ETC.) written in all caps.
    - *parameters* (*table names*, *column names*, etc.) written in lowercase.
2. Define **normalization** within the context of schemas and data.
    - Data organized into focuses and related tables; with the goal to reduce duplicate information and maintain consistency.
    - The point of using primary and foreign keys.
3. Explain the difference between one-to-one, one-to-many, and many-to-many relationships to a non-technical recruiter.
    - one-to-one: unique identifiers. not shared between other records; like ID numbers, DNA, *bread recipes*
    - one-to-many: a single record shared among many; a company to many employees; bread orders from many clients of a specific bread
    - many-to-many: no exclusivity; a record connects to many others, and vice-versa, many are connected to it;

## Bookmark and Review

- [Sequalize API](https://sequelize.org/master/)
  - An ORM, Object-Relational Mapper for Node.js; allowing an application to work with an SQL DB, through JS methods and models, w/o the need to write every DB operation to be written in SQL syntax.

## Things to Learn More About

- What are your learning goals after reviewing the readings?
  - documents or other non-relational DB structures.
  - scaling, in both realtional and non-relational DBs.
  - practice with primary / foreign keys.
  - KEYWORDS,
    - how extensive a query can be, and how to build it, piece-by-piece.
  - Sequalize
