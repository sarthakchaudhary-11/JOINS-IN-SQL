Here's a sample `README.md` file for your MySQL JOINs practice project. You can use this to document the dataset and SQL queries you're using:

---

# 📘 SQL Joins Practice Project

This project is designed to help understand and practice different types of **SQL Joins** using MySQL. It includes simple relational tables like `Customers` and `Orders`, which are ideal for practicing join operations.

---

## 📂 Dataset Description

### `customers.csv`
| customer_id | name     | city      |
|-------------|----------|-----------|
| 1           | Sarthak  | Noida     |
| 2           | Priya    | Delhi     |
| 3           | Aman     | Gurugram  |
| 4           | Riya     | Noida     |

### `orders.csv`
| order_id | customer_id | amount | order_date  |
|----------|-------------|--------|-------------|
| 101      | 1           | 1000   | 2024-12-01  |
| 102      | 2           | 1500   | 2024-12-05  |
| 103      | 1           | 800    | 2024-12-12  |
| 104      | 5           | 600    | 2024-12-15  |

---

## 🧠 Learning Objectives

- Understand and apply different types of **SQL Joins**:
  - INNER JOIN
  - LEFT JOIN
  - RIGHT JOIN
  - FULL OUTER JOIN (if supported)
  - CROSS JOIN

---

## 🧪 Example Queries

### 🔹 INNER JOIN

```sql
SELECT 
    customers.name,
    customers.city,
    orders.amount
FROM customers
INNER JOIN orders 
    ON customers.customer_id = orders.customer_id;
```

### 🔹 LEFT JOIN

```sql
SELECT 
    customers.name,
    customers.city,
    orders.amount
FROM customers
LEFT JOIN orders 
    ON customers.customer_id = orders.customer_id;
```

### 🔹 RIGHT JOIN

```sql
SELECT 
    customers.name,
    customers.city,
    orders.amount
FROM customers
RIGHT JOIN orders 
    ON customers.customer_id = orders.customer_id;
```

### 🔹 FULL OUTER JOIN (if supported or emulate using `UNION`)

```sql
SELECT 
    customers.name,
    customers.city,
    orders.amount
FROM customers
LEFT JOIN orders 
    ON customers.customer_id = orders.customer_id

UNION

SELECT 
    customers.name,
    customers.city,
    orders.amount
FROM customers
RIGHT JOIN orders 
    ON customers.customer_id = orders.customer_id;
```

### 🔹 CROSS JOIN

```sql
SELECT 
    customers.name,
    orders.order_id
FROM customers
CROSS JOIN orders;
```

---

## 🛠️ How to Use

1. Import the provided `customers.csv` and `orders.csv` into MySQL Workbench or any MySQL database.
2. Create tables using the CSV files.
3. Use the example queries to practice different types of joins.

---

## 📚 Tip

Always double-check column names and spelling. A common error is referencing columns like `customer.customer.id` instead of `customer_id`.

---

Let me know if you'd like me to tailor this `README.md` to a different dataset or add visualizations!
