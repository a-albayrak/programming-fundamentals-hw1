# CENG211 – Programming Fundamentals

## Homework #1

In this homework, you are expected to implement a “Transaction Management Application” in Java.  
You should fulfill the concepts of: 

- Defining Classes  
- CSV file I/O  
- Arrays  
- 2-dimensional Arrays  
- Constructors, Getters & Setters  

In the Transaction Management Application, there are the records of the products and the shop assistants of a company in Turkey. In addition to the products and the shop assistants, there are transactions that are performed with the aid of the shop assistants.  
The product records of this company are in the attached 'products.CSV' file that has the "ID, product name, price" format.  
In this application, there are 1500 transactions. The following are the requirements for the transactions.  

- Each transaction has a transaction ID, 3 products that are held in a 1-dimensional array, a total price, and a transaction fee.  
- The products of each transaction are randomly determined according to the product ID.  
- Multiple transactions could contain the same product.  
- The quantity of each product is also determined randomly between 1 and 10 (if the product is uncountable, the quantity could be assumed as kilograms).  
- The total price of a transaction is found by multiplying the quantity and the price for each product in the transaction and adding up all the results.  
- The transaction fee of each transaction is determined according to the following table:  

| Total Price (TL)      | Percentage                           |
|-----------------------|--------------------------------------|
| totalPrice <= 499     | transactionFee = 1% of totalPrice    |
| 500 <= totalPrice <= 799 | transactionFee = 3% of totalPrice |
| 800 <= totalPrice <= 999 | transactionFee = 5% of totalPrice |
| totalPrice >= 1000    | transactionFee = 9% of totalPrice    |

In the Transaction Management Application, the shop assistant records are given in 'shopAssistants.csv' file which has the "ID, name, surname, phone number" format. In this app, each shop assistant aids 15 transactions, and they are paid commission-based salaries. If the total revenue of the 15 transactions is more than 7500 TL, the commission is 3%, otherwise it is 1%. Also, the weekly salary basis of each shop assistant is according to their seniority. The weekly salary basis table is given below. (It can be assumed that there are 4 weeks in a month.)

| Seniority (Years)     | Weekly Salary Basis (TL) |
|------------------------|--------------------------|
| seniority < 1          | 1500                     |
| 1 <= seniority < 3     | 2000                     |
| 3 <= seniority < 5     | 2500                     |
| seniority >= 5         | 3000                     |

---

In this homework, you are expected to implement the necessary classes to load the data from the given CSV files and create the desired queries. You are expected to implement classes for:

- `Product`
- `ShopAssistant`
- `Transaction`
- `TransactionManagement`
- `SalaryManagement`
- `Query`
- `SalesManagementApp` (the class with `main` method)
- and other helper classes (e.g. `FileIO`)  

with the information given below:

### Product:
- ID  
- Product Name  
- Price  

### ShopAssistant:
- ID  
- Name  
- Surname  
- Phone Number  

### Transaction:
- ID  
- 1-D Array of 3 Products  
- Total Price  
- Transaction Fee  

### SalaryManagement:
- ShopAssistant  
> Note: One-dimensional array that holds ShopAssistant objects.  

### TransactionManagement:
- Transaction  
> Note: Two-dimensional array that holds Transaction objects for each shop assistant.  
> Ex: For 3rd shop assistant 7th Transaction, it is [2][6].  

### Implement necessary methods to respond to the following queries in `Query` class:

1. The highest-total-price transaction.  
2. The most expensive product in the lowest-price transaction.  
3. The lowest transaction fee.  
4. The highest-salary shop assistant. (Please, include his/her ID, name, seniority, weekly basis salary, commission, and total salary)  
5. The total revenue that is earned from 1500 transactions including both total price and transaction fee of each transaction.  
6. The total profit that is earned after paying the shop assistant salaries.  

> If the result of any of the queries is more than one, please display one result. Since almost all data are randomly determined, the results of your projects will differ each time you execute your code and, also from each other. This is completely normal.  

---

## Important Notes:

1. Do NOT request inputs in your app. Printing the results of the queries will be enough. You should print names of the results instead of printing IDs or indices.  
2. You are NOT allowed to use List / ArrayList interfaces in this homework.  
3. You can use standard `java.io` packages to read files. Do NOT use other 3rd party libraries.  
4. You should use relative paths (e.g. `Files/sample.csv`) instead of absolute paths (e.g. `C:\\user\\eclipse-workspace\\MyProject\\Files\\sample.csv`). Please be sure of it, otherwise there will be no output of your application and you certainly will lose points.  
5. To support Turkish characters, you may need to change your project’s text file encoding to UTF8:  
   - Right click on your project (in package explorer) → Properties → Text file encoding → Other → UTF8 → Apply.  
6. You are expected to write clean, readable, and tester-friendly code. Please try to maximize reusability and prevent redundancy in your methods.  

---
