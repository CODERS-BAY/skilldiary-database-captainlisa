# Diary 04.06.2020

## Joins and other Curiosities

* by adding ```GROUP BY``` to a select statement, you can group several entries with the same condition (?) together. for example:
```sql
SELECT job_id, SUM(salary) FROM employees GROUP BY job_id ORDER BY SUM(salary) DESC;
``` 
groups all salaries with the same job_id together and shows the sum of these salaries.

* with ```AVG()``` and ```SUM()``` you can calculate the average and the sum of a number of entries

* for a join, you first list all the columns that you want to get and from what table they're from and what table you want to reference from. then you join the additional tables and connect them on the specific keys.
```sql
/* default example */
SELECT table1.column1, table2.column2
FROM table1
JOIN table2 ON table1.tableID = table2.tableID

/* from example with joins*/
SELECT employees.first_name, employees.last_name, departments.department_name
FROM employees
INNER JOIN departments ON employees.department_id = departments.department_id;
```

* a self join is when a table references itself. we basically pretend that we have two tables and name them 'a' and 'b' and then treat them like we would a normal join:
```sql
SELECT CONCAT(a.first_name, ' ', a.last_name) AS 'Manager', CONCAT(b.first_name, ' ', b.last_name) AS 'Employee'
FROM employees a, employees b
WHERE a.employee_id = b.manager_id;
```

* with ```CONCAT()``` you can concatenate two strings together as seen above.