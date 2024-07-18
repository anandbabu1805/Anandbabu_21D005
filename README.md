Billing System Project
Overview
This project is a billing system designed to manage and track sales transactions in a retail environment. It uses a MySQL database to store information about customers, products, and sales. The system is divided into several modules, each responsible for different aspects of the billing process.

Modules
1. Customer Management
This module handles the creation, updating, and deletion of customer records. It ensures that each customer is uniquely identifiable by their customer ID (CID).

2. Product Management
This module manages the product inventory, including adding new products, updating product details, and tracking stock levels.

3. Billing and Invoice Management
This module is responsible for generating bills and invoices. It records the details of each sale, including the products purchased, quantities, total price, and payment status.

4. Reporting
This module provides various reports, such as sales reports, stock reports, and customer purchase history.

Database Structure
The database consists of the following tables:

bill_details
This table contains the information of every bill generated.

Attributes:
Invoice_number: (int, primary key, auto_increment) - A unique invoice number for each bill.
Item: (varchar(150)) - Stores the product IDs of all purchased products in a comma-separated format. For example: "2,3,41" means products with product IDs 2, 3, and 41 were purchased.
Quantity: (varchar(150)) - Contains the quantity of each purchased product in a comma-separated format.
Cid: (int) - Represents the customer involved in the purchase.
Price: (float) - Stores the total cost of the purchase.
Payment_Status: (char(1)) - Indicates whether the purchase has been paid ('P') or not ('U').
product_details
This table contains the basic details of each product, such as price, available stock, and total stock sold.

Attributes:
pid: (int, primary key) - A unique identifier for each product.
product_name: (varchar(20)) - The name of the product.
Quantity_sold: (float, default 0) - The total quantity of the product sold.
price_per_unit: (float) - The price per unit of the product.
stock_available: (float) - The available stock of the product.
customer_details
This table stores the phone number and name of each customer, along with a unique customer ID.

Attributes:
cid: (int, primary key) - A unique identifier for each customer.
name: (char(20)) - The name of the customer.
phone_no: (char(20)) - The phone number of the customer.
billing
This table is used to temporarily store the product ID and the quantity of the product purchased.

Attributes:
pid: (int) - The ID of the product.
quantity_purchased: (float) - The quantity of the product purchased.
How to Use
Customer Management: Use the customer management module to add, update, or delete customer information.
Product Management: Use the product management module to add new products, update product details, and manage inventory.
Billing: Use the billing module to generate new bills, specifying the products purchased, quantities, and payment status.
Reporting: Generate various reports to analyze sales, inventory levels, and customer purchase history.
Setup
Clone the repository.
Import the MySQL database schema from the provided SQL file.
Configure the database connection settings in the application.
Run the application.
Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your changes.

License
This project is licensed under the MIT License.
