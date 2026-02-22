# goit-rdb-hw-03

## SQL Data Query Language (DQL) Practice

### Overview

This project demonstrates practical usage of SQL DQL commands for querying and analyzing relational data.  
The assignment focuses on data retrieval, aggregation, filtering, sorting, grouping, and result limiting using MySQL.

All queries were executed and validated in MySQL Workbench.

---

## Database Context

**Database:** `goit_hw_03`  
**Tables used:**
- `products`
- `shippers`

The dataset represents a simplified product management structure including product pricing, supplier relations, and shipping details.

---

## Implemented SQL Concepts

### 1️⃣ Basic Data Retrieval
- `SELECT *`
- Column selection
- Schema usage with `USE`

### 2️⃣ Aggregate Functions
- `AVG()`
- `MAX()`
- `MIN()`
- `COUNT()`

### 3️⃣ Filtering
- `WHERE`
- `BETWEEN`

### 4️⃣ Deduplication & Sorting
- `DISTINCT`
- `ORDER BY DESC`
- `LIMIT`

### 5️⃣ Grouping & Aggregation
- `GROUP BY`
- Aggregated statistics per supplier

---

## Implemented Queries

### Retrieve all products
```sql
SELECT *
FROM products;
````

### Retrieve selected shipper columns

```sql
SELECT name, phone
FROM shippers;
```

### Price statistics

```sql
SELECT 
    AVG(price) AS avg_price,
    MAX(price) AS max_price,
    MIN(price) AS min_price
FROM products;
```

### Unique category-price combinations

```sql
SELECT DISTINCT category_id, price
FROM products
ORDER BY price DESC
LIMIT 10;
```

### Products in price range

```sql
SELECT COUNT(*) AS product_count
FROM products
WHERE price BETWEEN 20 AND 100;
```

### Supplier-level aggregation

```sql
SELECT 
    supplier_id,
    COUNT(*) AS product_count,
    AVG(price) AS avg_price
FROM products
GROUP BY supplier_id;
```

---

## Project Structure

```
goit-rdb-hw-03/
│
├── queries.sql
├── p3_1.1.png
├── p3_1.2.png
├── p3_2.png
├── p3_3.png
├── p3_4.png
├── p3_5.png
└── README.md
```

---

## Technical Focus

This assignment validates understanding of:

* Structured Query Language fundamentals
* Relational data querying
* Aggregate analysis
* Data filtering logic
* Result set transformation
* Clean query structuring and aliasing

---

## Tools Used

* MySQL 8+
* MySQL Workbench
* Git
* GitHub

---

## Author

Yuliya Kostenko
MSc Computer Science (Software Engineering)

Ти ж все-таки MSc Computer Science 😉
```
