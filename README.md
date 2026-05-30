[sqll.txt](https://github.com/user-attachments/files/28417460/sqll.txt)
# vivekl5221CREATE DATABASE IF NOT EXISTS company_db;

-- Explicitly target the database for subsequent operations
USE company_db;

-- Create an optimized table with primary keys, constraints, and standard data types
CREATE TABLE IF NOT EXISTS employees (
    employee_id INT AUTO_INCREMENT PRIMARY KEY,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    hire_date DATE DEFAULT (CURRENT_DATE),
    salary DECIMAL(10, 2) CHECK (salary > 0),
    department_id INT
);
