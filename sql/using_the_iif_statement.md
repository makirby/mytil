# Using the IIF statement

Instead of using the normal ```CASE WHEN``` statement you can make use of the ```IFF``` statement.

It works similar to the CASE WHEN statement i.e
```
SELECT IIF(Obsolete = 'N' OR InStock = 'Y', 1, 0) AS Salable, *
FROM Product
```

> Both IIF() and CASE resolve as expressions within a SQL Statement and can only be used in well defined places.

[Source](http://stackoverflow.com/questions/63447/how-to-perform-an-if-then-in-an-sql-select)

