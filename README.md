# Simple Employee Database Project

This project demonstrates a simple relational database system for managing employee data using PostgreSQL. It includes tables for `Employees`, `Departments`, and `Salaries`, along with basic CRUD operations. The goal of this project is to showcase database management skills, SQL queries, and proper organization of data.

## Project Overview

- **Database Name**: `employee_db`
- **Tables**:
  - `Employees`
  - `Departments`
  - `Salaries`
- **Technologies**: PostgreSQL, SQL
- **Features**: Basic CRUD operations (Create, Read, Update, Delete) for managing employees, their departments, and their salaries.

## Project Structure

```
Employee-Database-Project/
│
├── SQL/
│   |
│   └── employee_db.sql           # Exported SQL dump of the database
│
├── Data/
│   ├── employees.csv             # CSV file with sample employee data
│   ├── departments.csv           # CSV file with sample department data
│   └── salaries.csv              # CSV file with sample salary data
│
├── Screenshots/
│   └── query_results.png         # Screenshot of query results
│
└── README.md                     # Project documentation
```

## Database Tables

- **Employees**: Contains information about employees, including their first and last names, the department they work in, and their hire date.
- **Departments**: Contains the names of various departments within the company.
- **Salaries**: Contains salary information for each employee, along with the effective date of their salary.

## Setup Instructions

### 1. Install PostgreSQL

If you don’t have PostgreSQL installed, you can download it from [here](https://www.postgresql.org/download/).

### 2. Create the Database

Once PostgreSQL is installed and running, create the database by running the following SQL command or by using the SQL scripts provided.

```bash
psql -U postgres
CREATE DATABASE employee_db;
\q
```

### 3. Create the Tables

Navigate to the project directory and use the provided SQL script to create the necessary tables:

```bash
psql -U postgres -d employee_db -f SQL/create_tables.sql
```

### 4. Insert Sample Data (Optional)

You can insert sample data into the tables by running:

```bash
psql -U postgres -d employee_db -f SQL/crud_operations.sql
```

Alternatively, you can import the sample CSV files located in the `Data/` folder.

### 5. Import the SQL Dump (Optional)

If you want to recreate the database with existing data, you can use the provided SQL dump:

```bash
psql -U postgres -d employee_db -f SQL/employee_db.sql
```

### 6. View Data in CSV Format

If you don’t have PostgreSQL installed but would like to see the data, you can simply view the CSV files in the `Data/` folder:

- `employees.csv`
- `departments.csv`
- `salaries.csv`

## Basic CRUD Operations

### Example Queries

1. **Create a new employee**:

   ```sql
   INSERT INTO Employees (first_name, last_name, department_id, hire_date)
   VALUES ('Alice', 'Johnson', 1, '2023-01-01');
   ```

2. **View all employees**:

   ```sql
   SELECT * FROM Employees;
   ```

3. **Update an employee's salary**:

   ```sql
   UPDATE Salaries SET salary = 75000 WHERE employee_id = 1;
   ```

4. **Delete an employee**:
   ```sql
   DELETE FROM Employees WHERE employee_id = 1;
   ```

## Screenshots

Screenshots are provided.

## Contributing

Feel free to fork this repository, create your own features, and submit a pull request! All kinds of contributions, including improving documentation, are welcome.
