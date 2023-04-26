# Databases 1
The goal of this project is to create and manage a simple database. The scripts were written using MySQL syntax, and can be used in any environment that supports MySQL databases.

## Prerequisites
To use the files in this repository, you will need the following:
1. [MySQL](https://www.mysql.com/) or a compatible database management system.

## Getting Started
To get started with this project, follow these steps:
1. Clone this repository to your local machine.
2. Open your preferred MySQL client and connect to your local or remote database server.
3. Run the scripts to create and populate the database tables.

## Contents
This repository contains the following files:
1. SQL-script-1.txt
2. SQL-script-2.txt
3. SQL-script-3.txt
4. SQL-script-4.txt
5. SQL-script-5.txt
6. SQL-script-6.1.txt
7. SQL-script-6.2.txt
8. SQL-script-7.txt
9. SQL-script-8.txt
10. SQL-script-9.txt
11. SQL-script-10.txt

## Specifications

### Functionality

### SQL-script-1 
Creates a database called "pappas" with tables named "DEPT" and "EMP", populates them with data, and specifies the data types and sizes for each column.

### SQL-script-2
Creates a database called "new_personnel" with tables named "EMP" and "DEPT", populates them with data, and describes their structure using the "DESCRIBE" command. The "EMP" table has columns for employee number, employee name, job title, hire date, manager's employee number, salary, commission, and department number. The "DEPT" table has columns for department number, department name, and location. The program then populates both tables with data, and finally displays the contents of each table using the "SELECT" command.

### SQL-script-3
Creates a database called "personnel" with tables named "DEPT" and "EMP", populates them with data, and defines primary and foreign keys. The "DEPT" table has columns for department number, department name, and location, with department number as the primary key. The "EMP" table has columns for employee number, employee name, job title, hire date, manager's employee number, salary, commission, and department number, with employee number as the primary key and department number as a foreign key referencing the "DEPT" table. The program then performs various SQL queries, including calculating the average, minimum, maximum, and sum of salaries, counting the number of employees with and without commissions for the job title "ANALYST", selecting distinct job titles for each department, and selecting employee names, job titles, and salaries for employees with job titles "ANALYST" or "PROGRAMMER" with salaries between 1000 and 7000.

### SQL-script-4
Creates a new database called "new_personnel", creates three tables: DEPT, EMP, and PROJ, inserts data into them, and creates a foreign key constraint between the EMP and DEPT tables, and between the ASSIGN and EMP tables. It also inserts data into the ASSIGN table.

### SQL-script-5
The first query selects the names, salaries, commissions, and commission percentages of all employees in the EMP table. The second query selects the names, monthly earnings, and years of experience of employees whose years of experience exceed 20 years. The third query selects the names, job titles, and hire dates of employees hired as analysts or salesmen whose hire dates are in the first five days of any month.

### SQL-script-6.1
This is a SQL code that creates a database called "new_personnel" and three tables: "DEPT", "EMP", and "PROJ". The "DEPT" table has columns "DEPTNO", "DNAME", and "LOC". The "EMP" table has columns "EMPNO", "ENAME", "JOB", "HIREDATE", "MGR", "SAL", "COMM", and "DEPTNO". The "PROJ" table has columns "PROJ_CODE", "PNAME", and "BUDGET".
The code also inserts data into these tables and creates a new table called "ASSIGN" with columns "EMPNO", "PROJ_CODE", and "PTIME". It inserts data into the "ASSIGN" table as well, linking employees with projects they work on and the time they spend on each project.

### SQL-script-6.2
The first query selects the names of employees from the EMP table whose job is the same as those in the Accounting department. The second query retrieves the names and total monthly earnings of employees from the EMP table who have the highest total monthly earnings within their respective departments. The third query returns the names and salaries of employees from the EMP table who work in the Accounting department and earn less than the highest-paid employee in the Research department.

### SQL-script-7
The first query selects the names and salaries of all employees in the Accounting department (DEPTNO 10) and orders them by salary in ascending order. The results show that ELMASRI has the lowest salary, followed by DATE and then CODD with the highest salary.
The second query selects the names, job titles, and salaries of all employees and orders them by job title in ascending order and salary in descending order. The results show that CODD has the highest salary among analysts, NAVATHE has the highest salary among salesmen, DATE has the highest salary among programmers, and ELMASRI has the lowest salary among analysts.
The third query selects the names and department numbers of all employees in the Accounting department (DEPTNO 10) and orders them by commission in ascending order. If an employee does not have a commission, their commission is treated as 0. The results show that CODD, ELMASRI, and DATE all belong to the Accounting department with no commission listed.

### SQL-script-8
In the first query, the average salary and department number are selected from the EMP table and grouped by department number. The HAVING clause is used to filter out departments with less than one employee.
In the second query, the department number and average employee experience in years are selected from the EMP table and grouped by department number. The AVG function is used to calculate the average number of years between the current date and the HIREDATE column for each department. The result is formatted to one decimal place.

### SQL-script-9
The first query selects the project name, the employee name, and the job title for each assignment where the employee is working on the project. It joins the ASSIGN, EMP, and PROJ tables using the EMPNO and PROJNO keys and filters the results based on the employee and project numbers. The results are then sorted by project name and job title.
The second query selects the department name, the manager's name, and the employee's name for each department where the manager is also an employee in that department. It joins the EMP and DEPT tables twice, using the DEPTNO key for both joins, and filters the results based on the department number. The results are then sorted by department name and manager's name.
The third query selects the employee's name, job title, and department location for each employee working in the research department. It joins the EMP and DEPT tables using the DEPTNO key and filters the results based on the department name.
The fourth query selects the employee names for each assignment where the project name is "PAYROLL" and the time spent on the project is greater than 50. It joins the EMP and PROJ tables using the EMPNO and PROJNO keys and filters the results based on the project name and time spent.

### SQL-script-10
The first section of the code creates a new database called "PERSONNEL" and then creates three tables within that database: DEPT, JOB, and EMP.
The DEPT table has two columns: DEPTNO and DNAME. DEPTNO is an integer type and is set as the primary key for the table. DNAME is a variable character type with a maximum length of 15.
The JOB table has three columns: JOBNO, JOB, and SAL. JOBNO is an integer type and is set as the primary key for the table. JOB is a variable character type with a maximum length of 15. SAL is a float type with a precision of 7 and a scale of 2.
The EMP table has four columns: EMPNO, ENAME, JOBCODE, and DEPTNO. EMPNO is an integer type and is set as the primary key for the table. ENAME is a variable character type with a maximum length of 10. JOBCODE is an integer type and is a foreign key referencing the JOB table. DEPTNO is an integer type and is a foreign key referencing the DEPT table.
The following sections of code insert data into the three tables and then execute several SELECT statements to retrieve and display data from those tables. The SELECT statements use various forms of joins and WHERE clauses to filter and display the desired data.

## Contributing

This is a university project so you can not contribute.

## Authors

* **[University of West Attica]** - *Provided the exersice*
* **[Achilleas Pappas]** - *Wrote the code*

## License

This project is licensed by University of West Attica as is a part of a university course. Do not redistribute.

## Acknowledgments

Thank you to **University of West Attica** and my professors for providing the resources and knowledge to complete this project.
