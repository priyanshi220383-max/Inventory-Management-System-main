# Inventory and Data Management System

A backend project built using **Node.js, Express.js, MongoDB, and Mongoose** to manage products, maintain stock records, and generate inventory reports.

## Features

- **Product Schema & Validation**
  - Stores product details with proper validation.
  - Ensures SKU values are unique and in uppercase.
  - Prevents negative prices and stock quantities.
  - Includes a virtual `stockValue` field to calculate the total value of available stock.

- **Product Management (CRUD)**
  - Add new products.
  - View all products and individual product details.
  - Update existing product information.
  - Delete products when required.

- **Search, Filter & Pagination**
  - Filter products based on categories.
  - Search products by name (case-insensitive).
  - Sort products as needed.
  - Use pagination to manage large product lists.

- **Stock Management**
  - Update stock using a dedicated `PATCH` route.
  - Increase stock when new items are added.
  - Decrease stock when products are sold.
  - Prevent stock quantity from going below zero.

- **Inventory Reports**
  - **Low Stock Report:** Finds products whose available quantity is equal to or below their reorder level.
  - **Category-Wise Report:** Shows total products, available quantity, total stock value, and average price for each category.

- **Error Handling & Configuration**
  - Uses centralized error-handling middleware.
  - Keeps environment variables separate using `dotenv`.

## Tech Stack

- **Runtime:** Node.js
- **Backend Framework:** Express.js
- **Database:** MongoDB
- **ODM:** Mongoose
- **Environment Variables:** dotenv

## Project Structure

```text
Inventory-Management-System/
├── models/
│   └── Product.js
├── routes/
│   └── productRoutes.js
├── .env
├── .gitignore
├── package.json
└── server.js
```