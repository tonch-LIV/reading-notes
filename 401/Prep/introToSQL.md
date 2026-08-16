# Introduction to SQL

Structured Query Language (**SQL**) is used in databases for data manipulation; to retrieve and update information.  
SQL databases are structured systems built by containing tables, which are collections of related data organized into rows and columns.  

Relational databases include **MySQL**, **PostgreSQL**, and **SQLite**. Each with their own individual features and pros & cons.  

## Recommended SQL Clients / IDEs

Free cross-platform client / editor integration for hands-on practice;

- [*DBeaver*](https://dbeaver.io/) - A GUI that supports many DBMSs  
- [*pgAdmin*](https://www.pgadmin.org/) - PostgreSQL-specific GUI  
- [*MySQL Workbench*] - available from MySQL site  
- [*VS Code*](https://code.visualstudio.com/) - w/ extensions like "SQLTools"

## Commands

`CREATE TABLE` and `ALTER TABLE` are used to define structure and modify, respectively.  

*Transactions* are a method of delivery that ensure either all statements suceed or fail, concurrently.  
`SAVEPOINT`'s are useful to `ROLLBACK` part of a transaction w/o loosing / aborting the entire transaction.  

`SELECT`, `FILTER`, `SORT` are used to query data.  

`JOIN` combines related rows *across* tables.  

![SQL practice result](401/Prep/img/SQL_practice.png)
