# SQL Learning Repository

Welcome to the SQL Learning Repository! This repository is designed to help you learn SQL, with a focus on **CRUD operations** (Create, Read, Update, Delete) along with additional important SQL concepts. Whether you are new to SQL or looking to brush up on your skills, this repository contains everything you need to get started.

This repository covers the basics of SQL, focusing on CRUD operations, which are the foundational building blocks of database interactions. You'll find SQL scripts, interactive exercises, and explanations of key concepts. The aim is to provide hands-on practice while deepening your understanding of database management systems.

Here is the generic schema used for in-class demonstrations.

### Customers

| customer_id | first_name | last_name | age  | country |
| ----------- | ---------- | --------- | ---- | ------- |
| 1           | John       | Doe       | 31   | USA     |
| 2           | Robert     | Luna      | 22   | USA     |
| 3           | David      | Robinson  | 22   | UK      |
| 4           | John       | Reinhardt | 25   | UK      |
| 5           | Betty      | Doe       | 28   | UAE     |

### Orders

| order_id | item     | amount | customer_id |
| -------- | -------- | ------ | ----------- |
| 1        | Keyboard | 400    | 4           |
| 2        | Mouse    | 300    | 4           |
| 3        | Monitor  | 12000  | 3           |
| 4        | Keyboard | 400    | 1           |
| 5        | Mousepad | 250    | 2           |

### Shippings

| shipping_id | status    | customer |
| ----------- | --------- | -------- |
| 1           | Pending   | 2        |
| 2           | Pending   | 4        |
| 3           | Delivered | 3        |
| 4           | Pending   | 5        |
| 5           | Delivered | 1        |

This markdown will create tables that mirror the structure of the data as displayed in the image you provided.

### Data Types and Their Relationships

The dataset consists of three tables: **Customers**, **Orders**, and **Shippings**. Each table contains different attributes, and their relationships can be defined based on customer data and orders made by those customers.

#### 1. **Customers Table**

| Column Name | Data Type | Description                                                  |
| ----------- | --------- | ------------------------------------------------------------ |
| customer_id | Integer   | Unique identifier for each customer. This is the **Primary Key**. |
| first_name  | Varchar   | First name of the customer.                                  |
| last_name   | Varchar   | Last name of the customer.                                   |
| age         | Integer   | Age of the customer.                                         |
| country     | Varchar   | Country where the customer resides.                          |

**Primary Key:** `customer_id`

- Each customer has a unique identifier in the form of `customer_id`.
- This table contains personal details like `first_name`, `last_name`, `age`, and `country`.

#### 2. **Orders Table**

| Column Name | Data Type | Description                                                  |
| ----------- | --------- | ------------------------------------------------------------ |
| order_id    | Integer   | Unique identifier for each order. This is the **Primary Key**. |
| item        | Varchar   | Name of the item ordered.                                    |
| amount      | Integer   | Cost of the ordered item.                                    |
| customer_id | Integer   | Foreign key linking to the `customer_id` in the **Customers** table. |

**Primary Key:** `order_id`
**Foreign Key:** `customer_id`

- The `customer_id` in this table references the **Customers** table, meaning each order is placed by a specific customer.
- The `item` column records what the customer ordered, and `amount` refers to the price.

**Relationship:**

- The relationship between **Orders** and **Customers** is a **many-to-one** relationship. One customer can place many orders, but each order is associated with one specific customer.

#### 3. **Shippings Table**

| Column Name | Data Type | Description                                                  |
| ----------- | --------- | ------------------------------------------------------------ |
| shipping_id | Integer   | Unique identifier for each shipping entry. This is the **Primary Key**. |
| status      | Varchar   | Status of the shipping (e.g., Pending, Delivered).           |
| customer    | Integer   | Foreign key linking to the `customer_id` in the **Customers** table. |

**Primary Key:** `shipping_id`
**Foreign Key:** `customer`

- The `customer` column in this table references the `customer_id` from the **Customers** table.
- The `status` column tracks whether the order's shipping is pending or delivered.

**Relationship:**

- The relationship between **Shippings** and **Customers** is also a **many-to-one** relationship. One customer can have multiple shipping records, but each shipping entry is linked to one customer.

### Relationships Between Tables:

1. **Customers to Orders**:
   - One customer can place multiple orders.
   - The relationship is defined through the `customer_id` foreign key in the **Orders** table that references the **Customers** table.
2. **Customers to Shippings**:
   - One customer can have multiple shipping entries.
   - The relationship is defined through the `customer` foreign key in the **Shippings** table that references the **Customers** table.

### Primary and Foreign Keys

- **Customers Table**:
  - **Primary Key:** `customer_id`
- **Orders Table**:
  - **Primary Key:** `order_id`
  - **Foreign Key:** `customer_id` (links to the **Customers** table)
- **Shippings Table**:
  - **Primary Key:** `shipping_id`
  - **Foreign Key:** `customer` (links to the **Customers** table)