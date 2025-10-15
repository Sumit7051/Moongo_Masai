🛒 Order Management System - CRUD Operations (MongoDB)

This project demonstrates performing **CRUD operations** on an Order Management system using MongoDB.  
The `orders` collection contains sample data for customers, their orders, and order details.

## 🔍 Queries and Screenshots

### 1️⃣ Retrieve all orders with `order_status` = "shipped"

```js
db.orders.find({ order_status: "shipped" });
```
<img width="593" height="762" alt="image" src="https://github.com/user-attachments/assets/f428ef20-38dd-431d-be4d-c618daa709b2" />

###2️⃣ Update the total_amount of order with order_id: 1 to 70000
```js
db.orders.updateOne(
  { order_id: 1 },
  { $set: { total_amount: 70000 } }
);
```
<img width="439" height="337" alt="image" src="https://github.com/user-attachments/assets/04e3b916-9dd3-4e2b-93f3-5d6e3c148bc1" />
<img width="776" height="187" alt="image" src="https://github.com/user-attachments/assets/e3b34247-24fd-422a-8a6e-3967a19775af" />

### 3️⃣ Delete the order with order_id: 4
```js
db.orders.deleteOne({ order_id: 4 });
```
<img width="492" height="157" alt="image" src="https://github.com/user-attachments/assets/91bc127b-383e-4db4-9f59-8c8da4c46685" />

### 4️⃣ Retrieve the order with customer_name: "Alice Johnson"

```js
db.orders.find({ customer_name: "Alice Johnson" });
```
<img width="548" height="327" alt="image" src="https://github.com/user-attachments/assets/b6688989-089a-4ce8-bb28-74b24df812b3" />

### 5️⃣ Update the order_status of order with order_id: 2 to "delivered"

```js
db.orders.updateOne(
  { order_id: 2 },
  { $set: { order_status: "delivered" } }
);
```
<img width="480" height="348" alt="image" src="https://github.com/user-attachments/assets/2ac2de24-78b4-4ee6-83e1-29b54e8b3946" />

### 6️⃣ Retrieve all orders with total_amount >= 15000

```js
db.orders.find({ total_amount: { $gte: 15000 } });
```
<img width="580" height="677" alt="image" src="https://github.com/user-attachments/assets/6c724e34-aebe-4408-9b90-7b8f1af5cbe7" />






