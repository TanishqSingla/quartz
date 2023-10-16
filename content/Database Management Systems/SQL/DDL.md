DDL is data definition language, it is used to create and edit [[Schema|schema]].

E.g - Consider the following database with following [[Relations (Tables)|relations]]
## Sailors
| sid | sname | rating | age |
| --- | ------- | ------- | --- |
| 1 | Fred | 7 | 22
| 2  | Jim | 2 | 39
| 3 | Nancy | 8 | 27

### Boats
| bid | bname | color |
| ---- | ------- | ------ |
| 101 | Nina | red |
| 102 | Pinta | blue |
| 103 | Santa Maria | red |

## Reserves
| sid | bid | day |
| --- | --- | --- |
| 1 | 102 | 9/12/2015 |
| 2 | 102 | 9/13/2015 |

**To create the Sailors table the query would look like this**
```sql
CREATE TABLE Sailors (
	sid INTEGER
	sname CHAR(20)
	rating INTEGER
	age FLOAT
	PRIMARY KEY (sid)
);
```

```sql
CREATE TABLE Boats (
	bid INTEGER
	bname CHAR(20)
	color CHAR(10)
	PRIMARY KEY (bid)
);
```

```sql
CREATE TABLE Reserves (
	sid INTEGER
	bid INTEGER
	day DATE
	PRIMARY KEY (sid, bid, day)
	FOREIGN KEY (sid)
		REFRENCES Sailors
)
```

## Primary keys
Primary keys are unique "lookup key" for the [[Relations (Tables)|relation]]. A primary key cannot have duplicate values and can be made up of >1 column (e.g (firstname, lastname))

## Foreign Keys
Foreign key references a table via the primary key of that table. Foreign key doesn't have to share the name of the reference primary key.