# OKINA

ŌKINA is a comprehensive online retail solution that offers a fully functional backend and a minimalistic front end, providing all the capabilities needed for a seamless online shopping experience. With a focus on simplicity and efficiency it can be scaled to empower businesses
![ER Diagram](ŌKINA.png)

## Database Schema:
A total of 23 tables (or relations) are created using standard SQL
commands. These include tables for strong entities, weak entities,
relationships and multi-valued attributes. An SQL file - tables.sql contains
all the queries used in the process.

## Integrity constraints:
All the necessary constraints in DDL are added to the aforementioned
tables. These constraints include but are not limited to primary key, foreign
key, not null, unique and check.

## Data population:
Data population was achieved via an online bulk data generator i.e.
https://www.mockaroo.com/.
The data was carefully generated in accordance with the integrity
constraints.
The individual data set generated for each table is submitted within the
folder named **table_data**.

***A complete structure and data dump of the created database in also
submitted in an SQL file named **"database.sql"**.***

## **Interface Guide**
We have divided the entire application into 3 separate CLIs - CLI_User, CLI_Admin and
CLI_Employee.
As suggested by their names, each CLI is supposed to be used by a speciﬁc entity.
While User and Admin are separate entities, Employee is to be used by both employees
involved in assistance and delivery.
User_CLI has the following features:
- View all products
- Search for products by attributes
    - Adding them to cart
- View cart
    - Check out
        - Payment options
    - Edit cart
        - Remove product
        - Edit quantity for a product
    - Empty cart
- View wishlist
    - Add product to cart
    - Add complete wishlist to cart
    - Remove products from wishlist
- Add a particular product to cart
- View offers available
- View order history
    - View active orders
    - View past orders
        - View details for an order
- Raise a query for the order
- View queries
    - View resolved queries
    - View unresolved queries
- View current account information
    - Change username
    - Edit contact information
        - Add a new contact
        - Delete an existing contact
    - Edit addresses
        - Add a new address
        - Delete a previous address

Apart from all these features, the application contains exception handling on multiple
levels to provide a more robust end application.
The options are designed in a way to ensure a smooth user experience even with the
handicap of a command line interface, connecting all options in a way that allows absolute
connectivity between them. Sub-options provided within each option are provided considering
the scope of that option and the overall application so that no critical functionality is lost.
The following features are available to admin:
- Show all current users
    - Display a list of all current users registered on the platform, including their
usernames, email addresses, and roles.
    - Allow the admin to ﬁlter the list based on speciﬁc criteria such as role or registration
date.
- Show total revenue generated in the past month
    - Display the total revenue generated by the platform in the past month.
    - Allow the admin to ﬁlter the revenue data based on speciﬁc criteria such as product
category or payment method.
- Show the best selling product
    - Display the product that has the highest sales on the platform.
    - Allow the admin to ﬁlter the data based on speciﬁc criteria such as product category
or time frame.
- Show combination of sales according to date
    - Display a graph or chart showing the combination of sales made on the platform
according to date.
    - Allow the admin to ﬁlter the data based on speciﬁc criteria such as product category
or time frame.
- Search any custom query
    - Allow the admin to enter a custom query or search term.
    - Display the search results based on the query entered by the admin.
- Review merchant applications (if there are any)
    - Display a list of all pending merchant applications.
    - Allow the admin to review each application and approve or reject it.
- Review delivery executive applications (if there are any)
    - Display a list of all pending delivery executive applications.
    - Allow the admin to review each application and approve or reject it.
- Review technical assister applications (if there are any)
    - Display a list of all pending technical assister applications.
    - Allow the admin to review each application and approve or reject it.
- Exit to the main menu
    - Allow the admin to return to the main menu to access other options.
The admin can run any query since there is no encapsulation for the admin. The admin has
notiﬁcations for whenever a new employee is added, all admins have the same discretion.
The employee.py has the menu driven for 3 types of employee interface needed for the
functioning of the retail store.
- **Merchant**
    - View all your products: Displays all the products associated with the merchant's ID.
    - View the total proﬁt generated by your products in the past month: Shows the total proﬁt
generated by the merchant's products in the last month.
    - View your best selling product: Shows the merchant's best-selling product based on the
proﬁt generated from sales.
    - Search your product by product id: Allows the merchant to search for a speciﬁc product
by its ID.
    - Update your product stock by product id: Allows the merchant to update the stock of a
speciﬁc product by its ID.
    - View products out of stock: Displays the products that are currently out of stock and
allows the merchant to update their stock.
- **Delivery Executive**
    - view your proﬁle: This option allows the delivery executive to view their proﬁle details
    - view all your assigned deliveries: This option allows the delivery executive to view all the
deliveries assigned to them.
    - update the status of a delivery by delivery ID: This option allows the delivery executive to
update the status of a delivery by entering the delivery ID and the new status.
- **Assistance resolution**
    - View all the orders assigned to the assistant
    - View details of a particular order assigned to the assistant
    - View all customers and their details
    - Search for a customer by ID
    - View all the products and their details
    - Search for a product by ID
    - Update the status of an order assigned to the assistant
The employee interface also allows to employees(above 3 types) to register which they can log
into after approval from the admin.

### Contributions
- [@Lakshya Goel](https://github.com/lakshya-goel)
- [@N Narotam](https://github.com/greasyfinger)
