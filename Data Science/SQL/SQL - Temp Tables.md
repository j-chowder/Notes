
Temporary tables. 

```
CREATE TABLE #temptable  (
	table data
	table data
	table data
)	
```

Note that what differentiates the syntax in temp tables from tables is the `#`.

You can:

> Manually insert individual values

i.e. 
```
Insert INTO #temptable VALUES (
	data, data, data
)	
```

> Import data from another table.
* Take subsets from a large table and sticking that into a temp table.
i.e.

```
INSERT INTO #temptable
SELECT *
FROM othertable
```

---
**Benefits / Why you want to use it**

Performance / Speed.
* To insert specific data that you want to use -- presumably several times -- from an otherwise large parent table. This prevents the query having to read through all the shiz from the large table.

==Reusability==
* Use a temp table if you are referring to a large set of data and/or need to use it several times in your query.
* Say you need to join two different tables to get specific data. Instead of having to run that query and process the joining each and every time, you can just do it once in the temp table then select from the temp table in the future. 
* I.e. Methods in coding.
	* This is the main differentiator between CTEs and temp tables.
