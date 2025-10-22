Limited notes here due to existing SQL knowledge.

SELECT *, A,B,C FROM E,F WHERE x BETWEEN y AND 

LIKE

ORDER BY 

DSC

BETWEEN

AND

OR

NOT operator negates a condition. This means that SQL returns all records that don’t match the condition specified in the query. Note: WHERE country <> 'USA' and WHERE country != 'USA' are the same filters as WHERE NOT country = 'USA'. 

Operator: <, >, =, !, <=, >=, <>, 

Note:Use quotation mark for string, but not for number

  ## Join
INNER JOIN returns rows matching on a specified column that exists in more than one table. Ex: SELECT * FROM employees INNER JOIN machines ON employees.device_id = machines.device_id;
LEFT JOIN returns all the records of the first table, but only returns rows of the second table that match on a specified column. Ex: SELECT * FROM employees LEFT JOIN machines ON employees.device_id = machines.device_id;
RIGHT JOIN returns all of the records of the second table, but only returns rows from the first table that match on a specified column. 
FULL OUTER JOIN returns all records from both tables. You can think of it as a way of completely merging two tables.
Note: Similar to INNER JOIN, the order of tables does not change the results of the query.

## Aggregate functions 
 perform a calculation over multiple data points and return the result 
COUNT returns a single number that represents the number of rows returned from your query.
AVG returns a single number that represents the average of the numerical data in a column.
SUM returns a single number that represents the sum of the numerical data in a column. 
Ex: SELECT COUNT(firstname) FROM customers WHERE country = 'USA';

## Numeric data:
- the number of login attempts
- the count of a specific type of log entry
- the volume of data being sent from a source
- the volume of data being sent to a destination
## Date & times data:
- Login dates, login times, dates for patches, the duration of a connection

## Example wildcard filters
Use with LIKE instead of = 
- `a%`: apple123, art, a
- `a_`: as, an, a7
- `a__`: ant, add, a1c
- `%a`: pizza, Z6ra, a
- `_a`: ma, 1a, Ha
- `%a%`: Again, back, a
- `_a_`: Car, ban, ea7
