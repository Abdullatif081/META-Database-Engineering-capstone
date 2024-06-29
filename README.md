# Coursera Meta Database Engineering Capstone Project
## Overview
This project revolves around creating a comprehensive booking system for the Little Lemon Company, a renowned restaurant chain. The primary objective is to develop a robust relational database in MySQL capable of storing and managing large amounts of data efficiently. The system will maintain information pertaining to various aspects of the business, including bookings, orders, delivery statuses, menus, customer details, and staff information.

## Project Structure
The project is divided into several distinct tasks, each focusing on a specific aspect of the database development process:

### 1) Data Modeling

- Creating an Entity-Relationship (ER) Diagram
- Generating the Database Schema
- Populating the Relations with Data
### 2) Adding Sales Report

- Implementing Joins
- Creating Views
- Utilizing Special Operators (e.g., ANY)
### 3) Creating Optimized Queries

- Developing Stored Procedures
- Utilizing Prepared Statements
### 4) Setting up Tableau Workspace for Data Analysis

### 5) Python Client

## Data Modeling
### Task 1: Creating an ER Diagram
In this task, a normalized ER diagram adhering to the 1st, 2nd, and 3rd Normal Forms (1NF, 2NF, and 3NF) was created using MySQL Workbench Model Editor. The diagram accurately represents the data requirements of Little Lemon, including entities, attributes, primary keys, foreign keys, data types, and constraints. The ER diagram was exported as a PNG file for documentation purposes.

![ER diagram](https://github.com/Abdullatif081/META-Database-Engineering-capstone/assets/82438183/ec9248e4-db8b-4599-9ffe-e2f347102ffd)

### Task 2: Creating Database Schema
The forward engineering feature in MySQL Workbench was utilized to generate the SQL schema for the Little Lemon Database. The SQL code for creating the database schema is provided in the project documentation.

![Database Schema](https://github.com/Abdullatif081/META-Database-Engineering-capstone/assets/82438183/275e7a77-e0dc-4160-8986-6b91dc8ee5c0)

### Task 3: Populating with Data
SQL queries were executed to insert data into the newly created tables, ensuring the database is populated with relevant information for testing and analysis purposes populating database with data.

## Adding Sales Report
### Task 1: Views
In this task, a virtual table named OrdersView was created, focusing on the OrderID, Quantity, and TotalCost columns from the Orders table for all orders with a quantity greater than 2.

CREATE VIEW OrdersView AS
    SELECT O.OrderID, O.Quantity, O.TotalCost
    FROM LittleLemonDB.Orders AS O
    WHERE O.Quantity > 2;

SELECT * FROM OrdersView;
