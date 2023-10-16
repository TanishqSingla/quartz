## Basic Single-Table Queries

```sql
SELECT [DISTINCT] <column expression list>
	FROM <single table>
WHERE <predicate>;
```

The above is the simplest version of  a query language that one would write
The above expression does the following
- Produce all [[Tuple (Row)|tuples]] in the table that satisfy the predicate
- Output the expressions in the SELECT list


1) SELECT DISTINCT

```sql
SELECT DISTINCT S.name, S.gpa
	FROM students S
WHERE S.dept = 'CS';
```

- DISTINCT Specifies removal of duplicate rows before output
- Can refer to the students table as "S", this is called an alias

2) ORDER BY

```sql
SELECT s.name, s.gpa, s.age*2 AS a2
	FROM students s
WHERE s.dept = 'CS'
ORDER BY s.gpa, s.name, a2;
```

- ORDER BY clause specifies output to be sorted, it follows Lexicographic ordering (i.e the first field is followed, and then the second for sorting the output)
- Obviously must refer to columns in the output
	- Note the AS clause for naming output columns

3) ORDER BY pt.2

```sql
SELECT s.name, s.gpa, s.age*2 AS a2
	FROM students s
WHERE s.dept = 'CS'
ORDER BY s.gpa DESC, s.name ASC, a2;
```

- Ascending order by default, but can be overridden 
	- DESC flag for descending, ASC flag for ascending
- Can mix and match, lexicographically

4) LIMIT

```sql
SELECT s.name, s.gpa, s.age*2 AS a2
FROM students s
WHERE s.dept = 'CS'
ORDER BY s.gpa DESC, s.name ASC, a2;
LIMIT 3;
```

- Only produces the first `integer` output rows
- Typically used with ORDER BY
	- Otherwise the output is non-deterministic
	- Not a "pure" declarative construct in that case - output set depends on algorithm for query processing.

5) GROUP BY

```sql
SELECT AVG(S.gpa), S.dept
FROM Students S
GROUP BY S.dept
```
- Partition table into groups with same `GROUP BY` column
	- Can group by a list of columns
- Produce an aggregate result as per group
	- Cardinality of output != number of distinct groups
- Note: can put grouping columns in `SELECT` list

6) HAVING
- The `HAVING` predicate filters groups
- `HAVING` is applied after grouping and [[Aggregates|aggregation]]
	- Hence can contain anything that could go in the `SELECT` list
	- i.e [[Aggregates|aggs]] or `GROUP BY` columns
- `HAVING` can only be used in [[Aggregates|aggregate]] queries.