
A query within a query.

A subquery is used to return data that will be used in the main query (aka outer query) as condition to specify the data that we want retrieved.

Subqueries are just smaller pieces of code that return “intermediate” results that you need to calculate before doing your final magic. 

---
#### Subquery in the WITH clause -- common table expression (CTE)

---
#### Subquery in the SELECT clause -- scalar subquery

** Scalar subqueries = return only one row consisting of only one column



---
#### Subquery in the FROM clause -- derived table

A query result consists of rows and columns -- in other words a query produces a table.

So wherever you can have a table in SQL, e.g. in the FROM clause, you can have a derived table, which is another word for a subquery.

**![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcA7ssyfX79ihoeVd-ITHyn4DtsLRgclt9neFIuQBPRnFV1khs7DsX9G7nMy49_IuOkUD19XjsSK0xjrxL7cJjO5wSvlOiLu2ebVrDEMDgwT-zjQq8cJEQMDwB63ChqoX3IcPrwPQ?key=lmMIaaazc2xvHm5itL-m6b7k)**

The subquery derives a table which the outer query can pick and choose from.

Note: CTEs and/or temp tables are often more preferred over this. Not very recommended.

---
#### Subquery in the WHERE or HAVING clause -- can be either scalar or derived



---

