# Pivoting in SQL
```
SELECT

  Customer,
  SUM(CASE WHEN Product = 'Product A' THEN Quantity ELSE 0 END) AS 'Product A Quantity',
  SUM(CASE WHEN Product = 'Product B' THEN Quantity ELSE 0 END) AS 'Product B Quantity',
  SUM(CASE WHEN Product = 'Product C' THEN Quantity ELSE 0 END) AS 'Product C Quantity',
  SUM(Quantity) AS 'Total Quantity'

FROM Sales

GROUP BY Customer
```