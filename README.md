# Jan Burger Database Project - IT222: Database Principles

## Project Overview

This project focuses on developing a database for Jan Burger, an online restaurant that offers its services and promotions through mobile phone applications or websites. The primary goal of the Jan Burger Database (DB) is to maintain and manage the data used and generated to support the online restaurant's operations for its clients.

## View Description

The database view primarily revolves around the customer, who can order meals and customize their orders by adding special notes or modifying ingredients according to their preferences.

## Data Requirements

### Entities:

* **Customer:** Represents a person who orders meals from the restaurant application. Each customer has a Name, address, Email, Phone Number, and password, and is identified by a unique Customer ID. A customer can have zero or many orders.
* **Orders:** Represents a customer's request to buy meals. Each order has a Date, Status, TotalPrice, and is identified by an Order ID. Each order is owned by one and only one customer.
* **Branch:** Represents a franchise location of the restaurant business chain. Each branch has an address, contact number, and a unique branch number. Each branch provides multiple item options.
* **Item:** Represents a food or drink item available for order. Each item has a price, description, extras, calories, type, size, name, and a unique item number. Each item can be included in zero or many orders and is provided by at least one branch.

## Relational Schema

* **Item** (`ItemNo` (PK), `Price`, `Extras`, `Name`, `Calories`, `Type`, `Size`) 
* **Branch** (`BranchNo` (PK), `Address`, `ContactNo`) 
* **Provide** (`ItemNo` (FK), `BranchNo` (FK)) - Primary Key: (`BranchNo`, `ItemNo`) 
* **Orders** (`OrderID` (PK), `Date`, `Status`, `TotalPrice`, `CustomerID` (FK)) 
* **Included** (`OrderID` (FK), `ItemNo` (FK), `Quantity`) - Primary Key: (`OrderID`, `ItemNo`) 
* **Customer** (`CustomerID` (PK), `Name`, `Address`, `Email`, `PhoneNum`, `Password`) 

## Transaction Requirements

### Data Entry:
Customers can enter their name, address, phone number, and email.

### Data Update/Deletion:
Customers can update/delete their address and account password.

### Data Queries:
The system supports various queries, including:
* Displaying customer information.
* Displaying all items and orders.
* Displaying items by price (lowest to highest), type (side dishes), specific size, or specific name.
* Displaying orders from oldest to newest and completed status orders.
* Displaying items by calorie count (lowest to highest).
## Database Creation and Insertion

The SQL commands for creating tables and inserting sample data are included within the project files.

## Work Distribution

This project was a collaborative effort by the following team members:

* **Raghad Ahmed Hassan (443204743):** Transaction requirements (Data entry, update/deletion, queries), Order, Included, and Customer schemes.
* **Raseel Aldawish (443203036):** Data Requirements (branch & item), Data Dictionary for entities, Insertion commands (Item, Branch, Provide).
* **Doaa Abdul hakim (443203882):** Data Requirements (customer order), Data Dictionary for relationships, Data Queries commands and outputs.
* **Norah Nasser aljedai (443200841):** Global enhanced entity relationship diagram, Data Dictionary showing description of all attributes, Insertion commands (Customer, Order, Included).
* **Ghadah Suod Alismail (443200501):** Project description, View description, Schemes (Item and Branch), Data Queries commands and outputs.

---
*Supervised By: Abeer Aldrees* [cite: 3]
*King Saud University, College of Computer and Information Sciences, Department of Information Technology* [cite: 1]

