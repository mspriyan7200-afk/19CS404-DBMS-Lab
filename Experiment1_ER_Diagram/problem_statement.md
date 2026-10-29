# ER Diagram Workshop – Submission Template

## Objective
To understand and apply ER modeling concepts by creating ER diagrams for real-world applications.

## Purpose
Gain hands-on experience in designing ER diagrams that represent database structure including entities, relationships, attributes, and constraints.


# Scenario C: Restaurant Table Reservation & Ordering

**Business Context:**  
A popular restaurant wants to manage reservations, orders, and billing.

**Requirements:**  
- Customers can reserve tables or walk in.  
- Each reservation includes date, time, and number of guests.  
- Customers place food orders linked to reservations.  
- Each order contains multiple dishes; dishes belong to categories (starter, main, dessert).  
- Bills generated per reservation, including food and service charges.  
- Waiters assigned to serve reservations.

### ER Diagram: 
<img width="4512" height="1797" alt="erdplus (3)" src="https://github.com/user-attachments/assets/36b84341-fc05-43eb-9844-63b0725a5573" />


### Entities and Attributes

|Entity |	Attributes (PK, FK)|
|-------|--------------------|
|SUPERVISER	| Supervisor_ID (PK), Name, Contact_Details|
|CHEF	|Chef_ID (PK), Name, Contact_Details|
|WAITER |	Waiter_ID (PK), Name, Contact_Details|
|BILL	| Bill_ID (PK), Order_ID (FK), Total_Amount, Payment_Status|
|ORDER	| Order_ID (PK), Supervisor_ID (FK), Waiter_ID (FK), Total_Amount, Status, Date_Time|
|ORDERITEM	| OrderItem_ID (PK), Order_ID (FK), Chef_ID (FK), Food_Item_ID (FK), Table_ID (FK), Quantity|
|FOODITEM	| Food_Item_ID (PK), Name, Description, Price, Category|
|TABLE	| Table_ID (PK), Table_Number, Status, Location|
|CUSTOMER	| Customer_ID (PK), Table_ID (FK), Name, Contact_Details|

### Relationships and Constraints

| Relationship | Cardinality | 
|--------------|------------|
|MANAGES |	One-to-Many|
|GENERATES|	One-to-One|
|CREATES |	One-to-Many|
|SERVES	| Many-to-Many|
|CONTAINS	| One-to-Many|
|PREPARES	| One-to-Many|
|REFERS TO	| Many-to-One|
|BELONGS TO	| Many-to-One|
|HAS	| One-to-Many|



## Instructions for Students

1. Complete **all three scenarios** (A, B, C).  
2. Identify entities, relationships, and attributes for each.  
3. Draw ER diagrams using **draw.io / diagrams.net** or hand-drawn & scanned.  
4. Fill in all tables and assumptions for each scenario.  
5. Export the completed Markdown (with diagrams) as **a single PDF**
