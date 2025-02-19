
A correlated subquery works like a nested loop: the **subquery** only has access to rows related to a single record at a time in the **outer** query.

A matching subquery is a subquery that uses **values ​​from an external query.** 

> One way to interpret the line in the **WHERE** clause that references the two table is _“… where the correlated values are the same”_.

```
SELECT column1, column2, ....
FROM table1 outer
WHERE column1 operator
                    (SELECT column1, column2
                     FROM table2
                     WHERE expr1 = 
                               outer.expr2);
```

E.g.
```
SELECT continent, name, population FROM world x
  WHERE population >= ALL
    (SELECT population FROM world y
        WHERE y.continent=x.continent
          AND population>0)
```

“select the country details from world where the population is greater than or equal to the population of all countries where the continent is the same”.

```
SELECT last_name, salary, department_id
 FROM employees outer
 WHERE salary >
                (SELECT AVG(salary)
                 FROM employees
                 WHERE department_id =
                        outer.department_id group by department_id);
```

This retrieves the **last name, salary, and department_id** of every employee whose salary is more than the average salary of their corresponding department. 

