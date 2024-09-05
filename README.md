# Programming Fundamentals Homework 1: Transaction Management Application

## Overview

The application is designed to manage the transactions of a company in Turkey. The records consist of products and shop assistants, and their interactions in the form of transactions. Data for the products and shop assistants are provided in CSV files.

The **`products.CSV`** file contains:
- **ID**
- **Product Name**
- **Price**

The **`shopAssistants.csv`** file contains:
- **ID**
- **Name**
- **Surname**
- **Phone Number**

The application will manage **1500 transactions**, each involving:
- A unique **transaction ID**
- **3 products** randomly selected based on their ID
- A **1-dimensional array** to hold the products
- A **random quantity** for each product (1 to 10 units)
- A **total price** calculated by multiplying the quantity with the product price and summing them up
- A **transaction fee** calculated based on the total price using the following table:

| Total Price (TL)        | Transaction Fee (%) |
|-------------------------|---------------------|
| ≤ 499                   | 1%                  |
| 500 ≤ Total Price ≤ 799  | 3%                  |
| 800 ≤ Total Price ≤ 999  | 5%                  |
| ≥ 1000                  | 9%                  |

## Shop Assistant Details

Each shop assistant aids **15 transactions**. Their salary is commission-based:
- If the total revenue of the 15 transactions exceeds **7500 TL**, the commission is **3%**.
- Otherwise, the commission is **1%**.

Additionally, the weekly salary is based on their seniority:

| Seniority (Years)      | Weekly Salary Basis (TL) |
|------------------------|--------------------------|
| < 1                    | 1500                     |
| 1 ≤ Seniority < 3      | 2000                     |
| 3 ≤ Seniority < 5      | 2500                     |
| ≥ 5                    | 3000                     |

## Class Structure

You are expected to implement the following classes:

### Product
- **ID**
- **Product Name**
- **Price**

### ShopAssistant
- **ID**
- **Name**
- **Surname**
- **Phone Number**

### Transaction
- **ID**
- **1-D Array** of 3 Products
- **Total Price**
- **Transaction Fee**

### SalaryManagement
- **Array of ShopAssistants**

### TransactionManagement
- **2-D Array of Transactions** for each shop assistant
  - Example: For the 3rd shop assistant's 7th transaction, use `transactions[2][6]`.

### FileIO
- Helper class to load data from CSV files.

### Query
- Implement necessary methods to perform the following queries:
  1. The highest-total-price transaction.
  2. The most expensive product in the lowest-price transaction.
  3. The lowest transaction fee.
  4. The highest-salary shop assistant (ID, name, seniority, weekly salary basis, commission, total salary).
  5. The total revenue earned from the 1500 transactions (including both total price and transaction fee).
  6. The total profit earned after paying the shop assistant salaries.

## Example Output
```text
The highest total price transaction= 301.32
The most expensive product in the lowest price transaction= Sweet Potato
The lowest transaction fee= 0.07
The highest salary shop assistant= {ID:79, Name:Valentina, Seniority:14, Weekly Salary:3000, Commission:13.72, Salary:12,013.72}
The total revenue= 107,895.52
The total profit= -989,180.21
