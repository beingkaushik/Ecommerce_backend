# 🛒 E-Commerce Backend API

This project is a **Node.js backend application** for a simple e-commerce system developed to demonstrate **REST API design, modular architecture, and backend business logic**.

The system allows management of **products, categories, and orders** while handling stock validation and automatic price calculation during order creation.

---

## Project Structure
```
ecommerce-backend
│
├── app.js
│
├── routes
│ ├── productRoutes.js
│ ├── categoryRoutes.js
| ├── orderRoutes.js
│ └── package.json
│
├── controllers
│ ├── productController.js
│ ├── categoryController.js
| ├── orderController.js
│ └── package.json
│
├── data
│ ├── products.js
│ ├── categories.js
| ├── orders.js
│ └── package.json
│
└── package.json
```

Each module is separated into **routes, controllers, and data layers** to maintain a clean and maintainable backend structure.

---


## Technologies Used

- Node.js
- Express.js
- REST APIs
- JavaScript
- JSON File Storage

---

## Features

- View products
- Add products
- Update products
- Delete products
- Manage categories
- Create orders
- Validate product availability
- Automatically calculate order total price
- Reduce stock after successful order

---

## API Endpoints

### Product APIs

| Method | Endpoint | Description |
|------|------|------|
| GET | /products | Get all products |
| POST | /products | Add new product |
| PUT | /products/:id | Update product |
| DELETE | /products/:id | Delete product |

---

### Category APIs

| Method | Endpoint | Description |
|------|------|------|
| GET | /categories | Get all categories |
| POST | /categories | Create category |

---

### Order APIs

| Method | Endpoint | Description |
|------|------|------|
| GET | /orders | Get all orders |
| POST | /orders | Create new order |

---

## Example Order Request

POST `/orders`

```json
{
  "productId": 1,
  "quantity": 2
}
```

## Example Order Response
```

{
"id": 1,
"productId": 1,
"quantity": 2,
"totalPrice": 1600
}


```

## Order Processing Logic

When a new order is created:

1. Check whether the product exists
2. Verify that enough stock is available
3. Calculate the total price automatically
4. Reduce the product stock
5. Store the order

---

## How to Run the Project

### Install Dependencies


npm install


### Start the Server


node app.js


Server will run at:


http://localhost:5000


---

## Testing APIs

You can test the APIs using:

- Postman
- Thunder Client
- cURL

Example request:


POST http://localhost:5000/orders

## ⚠️ Important Note

This project uses in-memory storage.

That means:

-  Data will reset whenever the server restarts.

-  This project is designed for learning REST API backend development.
