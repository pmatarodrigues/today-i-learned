# Convert a value into a different length or datatype

## Why did I learn this

When executing a `SELECT` query to a SQL Server Database through a script, result was returning NULL on a Varchar value, but when the query was directly executed through SQL Server Management Studio everything was fine.

Turns out, there was some kind of encoding made on the SQLServer wrapper that made the value longer on my code than the allowed size on the DB.

## Example

- On SQL Server DB: varchar(50)
- On code: DB table was mapped to receive the data, but as an encoding was made, string was bigger than allowed.

## Solution

Using SQL Server **CAST()** function
Cast value to be the size I wanted when received.
```sql
SELECT CAST(value as VARCHAR(200)) AS value
FROM table
```