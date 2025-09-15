
# Employee Management System

A simple Java application that manages employee data using JDBC and MySQL database.

## Features

- **Insert** new employee records
- **Update** existing employee information
- **Delete** employee records
- **Fetch** and display employee data

## Prerequisites

Before running this application, make sure you have:

- Java Development Kit (JDK) installed
- MySQL Server running
- MySQL JDBC Driver (Connector/J)
- A database named `myjdbcdb1`
- An `employee` table with the following structure:

```sql
CREATE TABLE employee (
    emp_id INT PRIMARY KEY,
    name VARCHAR(50),
    salary INT
);
```

## Database Setup

1. Start your MySQL server
2. Create the database:
   ```sql
   CREATE DATABASE myjdbcdb1;
   ```
3. Use the database:
   ```sql
   USE myjdbcdb1;
   ```
4. Create the employee table:
   ```sql
   CREATE TABLE employee (
       emp_id INT PRIMARY KEY,
       name VARCHAR(50),
       salary INT
   );
   ```

## Configuration

Update the database connection details in the code:

```java
String url = "jdbc:mysql://localhost:3306/myjdbcdb1";
String username = "root";
String password = "your_password_here";  // Change this to your MySQL password
```

## How to Run

1. Compile the Java file:
   ```bash
   javac Fetch_Employee_data_1.java
   ```

2. Run the application:
   ```bash
   java jdbc_fetch_sql_1.Fetch_Employee_data_1
   ```

3. Choose an option from the menu:
   - **1** - Insert new employee
   - **2** - Update employee name
   - **3** - Delete employee
   - **4** - Fetch employee data

## Usage Examples

### Insert Employee
- Choose option 1
- Enter employee ID, name, and salary when prompted

### Update Employee
- Choose option 2
- Enter new name and employee ID to update

### Delete Employee
- Choose option 3
- Enter employee ID to delete

### Fetch Employee Data
- Choose option 4
- Enter employee ID to view details

## File Structure

```
project/
├── Fetch_Employee_data_1.java
└── README.md
```

## Notes

- Make sure MySQL server is running before executing the program
- The application uses PreparedStatement to prevent SQL injection
- After insert, update, and delete operations, the program automatically displays the updated data
- Replace the password in the code with your actual MySQL root password

## Common Issues

1. **Connection failed**: Check if MySQL server is running and credentials are correct
2. **Table doesn't exist**: Make sure you've created the `employee` table
3. **ClassNotFoundException**: Ensure MySQL JDBC driver is in your classpath
