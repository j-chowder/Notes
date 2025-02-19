
`Group by X` means "put all those with the same value for X in the one group."

`Group By X, Y` means "put all those with the same values for both X and Y in the one group."

i.e.

```
Table: Subject_Selection

+---------+----------+----------+
| Subject | Semester | Attendee |
+---------+----------+----------+
| ITB001  |        1 | John     |
| ITB001  |        1 | Bob      |
| ITB001  |        1 | Mickey   |
| ITB001  |        2 | Jenny    |
| ITB001  |        2 | James    |
| MKB114  |        1 | John     |
| MKB114  |        1 | Erica    |
+---------+----------+----------+
```

`Group by X`:

Input: 

```
SELECT Subject, Count(*)
FROM Subject_Selection
GROUP BY Subject
```

Output:

```
+---------+-------+
| Subject | Count |
+---------+-------+
| ITB001  |     5 |
| MKB114  |     2 |
+---------+-------+
```

(5 entries for ITB001, and 2 for MKB114)

`Group by X, Y`

Input:

```
SELECT Subject, Semester, Count(*)
FROM Subject_Selection
GROUP BY Subject, Semester
```

Output:

```
+---------+----------+-------+
| Subject | Semester | Count |
+---------+----------+-------+
| ITB001  |        1 |     3 |
| ITB001  |        2 |     2 |
| MKB114  |        1 |     2 |
+---------+----------+-------+
```

"Group them so that all of those with the same Subject and Semester are in the same group, and then calculate all the aggregate functions for each of those groups"

(there are three people doing ITB001 in semester 1, and two doing it in semester 2. Both of the people doing MKB114 are in semester 1, so there is no row for semester 2)

---

The GROUP BY clause is used in conjunction with the aggregate functions to group the result-set by one or more columns.


