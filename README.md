# Java-Nimap-Task-
Set up the Database Configuration:
Update the "application.properties" file with your relational database (RDB) connection details, such as URL, username, and password.
Run the Application:  
mvn spring-boot:run  
my application will be accessible: http://localhost:8080
How to Run the Machine Test:
Run the APIs Using Postman:
Below are the endpoints for testing:
Category APIs:
GET: http://localhost:8080/api/categories?page=3
POST: http://localhost:8080/api/categories
GET: http://localhost:8080/api/categories/{id}
PUT: http://localhost:8080/api/categories/{id}
DELETE: http://localhost:8080/api/categories/{id}
Product APIs:
GET: http://localhost:8080/api/products?page=2
POST: http://localhost:8080/api/products
GET: http://localhost:8080/api/products/{id}
PUT: http://localhost:8080/api/products/{id}
DELETE: http://localhost:8080/api/products/{id}
Server-Side Pagination:
Pagination is implemented for both categories and products. we can test it using the page query parameter.
Fetch Product with Category Details:
When fetching a single product, the response includes its respective category details.
Database Design
Category Table:
Id Column:
Data Type: Long
It is the unique identifier for each category in the table.
Constraints:
Primary Key: This means every value in this column must be unique and is used to identify rows.
Auto-Increment: The database automatically generates the value.
Category Name Column:
Data Type: String
It holds the name of the category
Product Table:
The relationship between Category and Product is modeled as one-to-many using JPA annotations.
Id Column:
Data Type: Long
It serves as the unique identifier for each product in the table.
Constraints:
Primary Key: Ensures each product has a unique id.
Auto-Increment: Automatically generates a unique number for each new product.
Name Column:
Data Type: String.
Stores the name of the product.
Constraints:
Not Null: Ensures the product must have a name
Price Column:
Data Type: Double
Stores the price of the product.
Ensures every product has a price.
Catgory_Id Column:
Data Type: Long
It acts as a reference to the Category Table to specify the category a product belongs to.
Constraints:
Foreign Key: Links to the id column in the Category Table. This ensures the product’s category exists in the Category Table.
Database images
![Screenshot (46)](https://github.com/user-attachments/assets/35f8b942-8d1b-4a5d-ac44-03c618353156)
![Screenshot (47)](https://github.com/user-attachments/assets/5f88c86f-2f92-4a16-ba68-d894300f6552)


