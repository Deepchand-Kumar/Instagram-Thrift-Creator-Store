# Instagram-Thrift-Creator-Store
This project focuses on designing an Entity Relationship Diagram (ERD) for a small Instagram-based business.
Instagram-Based Thrift & Handmade Store — ER Diagram Database Design

Project Overview
------------------------

This project focuses on designing an Entity Relationship Diagram (ERD) for a small Instagram-based business that sells:

Thrifted fashion items
Handmade products

Initially, the business operates through Instagram DMs and WhatsApp, but as orders increase, the owner needs a structured database system to manage:

products
inventory
customers
orders
payments
shipping information

The goal of this project is to create a clean and normalized database design that realistically represents how such a business works.

Problem Statement
-------------------------------
The business sells two different types of products:

1. Thrifted Products
Usually unique pieces
Only one quantity available
May include condition details such as:
Like New
Good
Vintage
Used
2. Handmade Products
Can be produced in batches
Multiple quantities may exist
May have different sizes/colors

The database should support:

customer order management
inventory tracking
payment status
shipping status
product categorization
reusable and unique inventory handling

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

Objectives
-------------------------------
The ER diagram should answer the following business questions:

What products are being sold?
Is the product thrifted or handmade?
How many units are available?
Which customer placed which order?
What products belong to an order?
Has payment been completed?
Has the product been shipped or delivered?
Can customers place multiple orders?
Can one order contain multiple products?
How are product details like size, color, condition, and price stored?

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Entities Included
---------------------------
The ER diagram contains the following major entities:

Entity	Purpose
Customer	Stores customer information
Product	Stores common product information
ProductType	Distinguishes thrifted vs handmade
Inventory	Tracks stock quantity
Order	Stores order details
OrderItem	Junction table between orders and products
Payment	Stores payment details and status
Shipping	Stores delivery/shipping information
Category	Organizes products into categories

Main Features of the Design
-------------------------------
Product Management
----------------
Supports both thrifted and handmade products
Stores:
size
color
condition
price
quantity

Inventory Handling
-------------------
Unique thrift products can have quantity = 1
Handmade products can have multiple stock units
Order Management
One customer can place multiple orders
One order can contain multiple products
Managed using the OrderItem junction table

Payment Tracking
---------------------
Tracks:
payment status
payment method
payment date

Shipping Tracking
-------------------
Tracks:
shipment status
delivery status
tracking details

Relationships Used
---------------------
Relationship	Type
Customer → Order	One-to-Many
Order → OrderItem	One-to-Many
Product → OrderItem	One-to-Many
ProductType → Product	One-to-Many
Category → Product	One-to-Many
Order → Payment	One-to-One / One-to-Many
Order → Shipping	One-to-One

Normalization Considerations
--------------------------------

The database design follows normalization principles to avoid redundancy:

Product information separated from order details
Junction table used for many-to-many relationships
Payment and shipping stored separately
Inventory handled independently

This makes the system scalable and easier to maintain.

Primary Keys and Foreign Keys
---------------------------------
The ERD clearly defines:

Primary Keys (PK)
Foreign Keys (FK)

to maintain relational integrity between entities.

Example:

customer_id → PK in Customer
order_id → PK in Order
customer_id in Order → FK referencing Customer

Tools Used
-----------------
DRAWDB

Learning Outcomes
--------------------------
Through this project, the following concepts are demonstrated:

Database modeling
ER diagram creation
Relationship mapping
Primary & foreign key usage
Inventory system design
Order management system structure
Real-world business analysis

Conclusion
------------------------
This ER diagram represents a practical database solution for a growing Instagram-based thrift and handmade business. The design focuses on scalability, clarity, and proper handling of both unique thrift items and reusable handmade inventory.

The system is structured to support future growth while keeping the database normalized and easy to manage.

Author
-------------------
Name: Deepchand Kumar
Project: Instagram Thrift & Handmade Store ER Diagram
Course/Subject: DBMS / Database Design Project
Date: 07-May-2026
