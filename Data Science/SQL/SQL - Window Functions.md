*Window functions are a bit like GROUP BY, but they don’t aggregate the data of the group into a single row. This allows for aggregate calculations, like sums, averages, and rankings, while keeping the data's granularity intact.*

Say you are comparing salaries to the average by department. You could use a CTE to GROUP BY department and AVG() by salary, then join this with the original table, but with a window function, it's one step:

```
 SELECT
   employee, department,
   salary,
   AVG() OVER (PARTITION BY department) AS avg_salary
   FROM
  employees
```

#### Parts of Window Functions

`function over (partition by column_name) order by column_name [window frame]`

`FUNCTION` can be:
* an aggregation
	* SUM(), AVG()
* a ranking function
	* ROW_NUMBER()
* a function that returns values from other rows without requiring a self-join
	* LEAD(), LAG()

`OVER`
* This tells the DB engine what group of rows to apply the function. It often includes one or both of the parts below.

(Optional)
`PARTITION BY:`
* works like a GROUP BY within the window, dividing the data into groups.

`ORDER BY:`
* organizes the data within the window

`Window Frame`
* `MODE between [frame_start] AND [frame_end] (frame_exclusion)`

* restricts the rows that will be considered in the function’s calculation.

* `ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW: `
	* All rows from the start of the partition up to the current row.
* `ROWS BETWEEN 3 PRECEDING AND 1 FOLLOWING:`
	* Three preceding rows, the current row, and the next row.
* `RANGE BETWEEN INTERVAL '30' DAY PRECEDING AND CURRENT ROW:`
	* Limits the calculation to the 30 days preceding the current row.





E.g.

```
SELECT
 f.id, f.release_year, f.rating,
 AVG(rating) OVER (PARTITION BY release_year) AS year_avg
   FROM films f ORDER BY release_year, rating;
```

**![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcL0GKtr5oXKq7crGOlVhYqmYceolJTHw5vEdTHfkY4Kw0_S7YPTuVYnTqham318lynyoGiYkRKxu5beYjgVBQ4v8XYd0eXJMMRZwTvH3Qf1kDHlm1e87nXczqCt16QzCH7sWoiug?key=mVF1W1TrBFF1vodp-5EllQ)**

