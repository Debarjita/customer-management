# Employee Management System

This Python-based Employee Management System provides basic functionalities for managing employee records. The application uses MySQL as the database to store information, allowing users to add, promote, remove, and display employee details.

## Features
- **Add Employee**: Insert a new employee record.
- **Remove Employee**: Delete an employee record by ID.
- **Promote Employee**: Increase the salary of an existing employee.
- **Display Employees**: View all employee records stored in the database.

## Prerequisites
- **Python 3.x**
- **MySQL database**
- **mysql-connector-python**: Install it via pip
   ```bash
   pip install mysql-connector-python
  ```
### Database Setup
- Create a MySQL Database: Create a database called emp.
- Create a Table:
```sql
Copy code
CREATE TABLE empd (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    post VARCHAR(50),
    salary INT
);
```
- Update Database Credentials: Update your MySQL connection details in the Python code:
```python
con = mysql.connector.connect(
    host="localhost",
    user="root",
    password="your_password",
    database="emp"
)
```
### Code Structure
- Add_Employ: Adds a new employee to the database if an employee with the same ID does not already exist.
- Remove_Employ: Removes an employee record by ID if the employee exists in the database.
- Promote_Employee: Increases an employee’s salary by a specified amount.
- Display_Employees: Displays details of all employees stored in the database.
- check_employee: Checks if an employee with the specified ID exists in the database.
- menu: Displays the menu options and calls appropriate functions based on user input.
### Usage
Run the Application:

```bash
python employee_management.py
```
### Menu Options:

- 1:Add Employee - Enter Employee ID, Name, Post, and Salary to add a new employee.
- 2:Remove Employee - Enter Employee ID to delete an employee record.
- 3:Promote Employee - Enter Employee ID and increase in salary to update an employee's salary.
- 4:Display Employees - View all employee records.
- 5:Exit - Exit the application.
### Sample Output
```css

Welcome to Employee Management Record
Press 
1 to Add Employee
2 to Remove Employee 
3 to Promote Employee
4 to Display Employees
5 to Exit
Enter your Choice: 1
```

### Contributing
- Pull requests are welcome. For significant changes, please open an issue first to discuss what you would like to change.

