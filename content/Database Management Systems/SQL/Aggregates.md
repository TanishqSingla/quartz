SQL provides a way to compute an aggregate function on a single table ([[Relations (Tables)|relation]]).

E.g
```sql
SELECT AVG(S.gpa)
FROM Students S
WHERE S.dept = 'CS'
```

The above expression does the following:
- Compute the summary (a.k.a an aggregate) of some arithmetic expression.
- Produces 1 row of output
	- with one column in this case


## Aggregate functions
Some common aggregate functions common across SQL are

## AVG
Computes average in a table.

### SUM 
Computes sum in a table.

### MIN
Computes the minimum value in a table.

### MAX
Computes the maximum value in a table

### COUNT
Counts the number of occurrence of a given value in a table. 