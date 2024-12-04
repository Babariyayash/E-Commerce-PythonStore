# Python E-Commerce Store

This is a Python-based console application simulating an e-commerce store. It allows administrators to manage products and customer data while enabling customers to browse products, filter them, add items to a cart, and proceed with purchases. The application uses **MySQL** for database management and **PrettyTable** for tabular data display.

---

## Features

### **Admin Functionalities**
- **Manage Products**:
  - Display all products in the inventory.
  - Add new products with details such as name, company, type, color, rating, price, and quantity.
  - Update existing product details.
  - Delete products from the inventory.
  - Search for a specific product by its ID.
- **Manage Customers**:
  - Display all customer records.
  - Update customer details such as name, contact number, and address.
  - Delete customer records.
  - Search for a customer by ID.

### **Customer Functionalities**
- **Browse Products**:
  - View all available products.
  - Apply filters to search for products based on:
    - Product type
    - Company name
    - Price range
- **Add to Cart and Purchase**:
  - Add products to the cart with a specified quantity.
  - View the cart with a breakdown of product details, including total cost.
  - Proceed to checkout by filling in customer details.
  - Generate and display a bill for the purchase.
  - Save customer information in the database.
- **Cancel Cart**:
  - Option to cancel the cart and exit without making a purchase.

---

## Prerequisites

- **Python 3.7+**
- **MySQL Database**
- **PrettyTable Library**:
  ```bash
  pip install prettytable
  ```
- **MySQL Connector for Python**:
  ```bash
  pip install mysql-connector-python
  ```

---

## Database Setup

The application uses the MySQL database with the following structure:

### **Tables**
1. **Product_Data**:
   - `Product_ID` (Primary Key, Integer)
   - `Product` (Product Name, String)
   - `Company` (Product's Manufacturer, String)
   - `Product_Type` (Product Category, String)
   - `Product_Colour` (Color, String)
   - `5_Star_Ratings` (Ratings, Integer)
   - `Price` (Price, Integer)
   - `Quantity` (Stock Quantity, Integer)

2. **Cust_Data**:
   - `Cust_ID` (Primary Key, Integer)
   - `Customer_Name` (Customer's Name, String)
   - `Contact_No` (Contact Number, Integer)
   - `Address` (Customer's Address, String)

---

## Installation

1. **Clone this Repository**:
   ```bash
   git clone https://github.com/Babariyayash/E-Commerce-PythonStore.git
   cd ecommerce-store
   ```

2. **Set Up MySQL Database**:
   - Update the database connection details in the script:
     ```python
     mycon = con.connect(
         host="localhost",
         username="root",
         password="YourPassword"
     )
     ```
   - Run the script to create the necessary database and tables automatically.

3. **Run the Application**:
   ```bash
   python ecommerce_store.py
   ```

---

## Usage

### **Admin Access**
- Login as "Admin" to manage the product and customer databases.
- Choose from various options to add, update, delete, or search for product and customer details.

### **Customer Access**
- Login as "Customer" to browse products, filter results, add items to the cart, and proceed to checkout.
- The application generates a bill with customer and product details upon successful purchase.

---

## Sample Flow

### **Admin Interface**
1. Choose Admin mode.
2. Modify product or customer data:
   - Add new products.
   - Update product attributes (e.g., price, quantity).
   - Remove products no longer available.

### **Customer Interface**
1. Choose Customer mode.
2. Browse products:
   - Filter by type, company, or price range.
3. Add products to the cart.
4. Proceed to payment:
   - Fill in customer details.
   - View a detailed bill with purchase summary.

---

## Features in Action

- **Product Management**:
  Easily manage an inventory of products with CRUD operations.
- **Customer Purchase**:
  Simulate an e-commerce shopping experience with cart functionality and bill generation.

---

## Dependencies

- **Python Libraries**:
  - `mysql.connector`
  - `prettytable`
  - `random`
  - `datetime`

- **Database**:
  - MySQL

---



Enjoy exploring the E-commerce Python Store!
