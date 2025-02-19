
*Common Table Expression* -- just a way of **structuring** your queries to make them easier to read and manage.

Only exists within the scope of the statement...
* Only created in `memory` rather than `tempdb` file. (which differs from temp table)
* Because the CTE is never created, it is never saved anywhere and thus must be executed each time for the query.

```
WITH CTE as 
	(Subquery)
SELECT (blah blah blah) 
FROM CTE
```

> SELECT statement must come directly after the CTE expression in order to work.

**Benefits / Why you want to use it**
* Readability (say, over a subquery statement)
* Repeatablity (to a certain extent)
	* If you are copy-pasting the same complex subquery in several places, it's nicer to use a CTE (except when it kills performance and you should be using a temp table).
	* Use a CTE if you only need the information from the CTE a **few** times in a query.
* Recursive Queries ()

