# SQL Fill-Up and Fill-Down
You can use the following SQL to update null values in a column based on actual values in the same column (fill-up):

```
UPDATE table_name
SET column_name = (
    SELECT column_name
    FROM table_name t2
    WHERE t2.id = (
        SELECT MIN(t3.id) -- MAX for fill-down
        FROM table_name t3
        WHERE t3.id > table_name.id -- < for fill-down
        AND t3.column_name IS NOT NULL
    )
)
WHERE column_name IS NULL;
```

This will update the values in `column_name` with the first non-null value found in the `column_name` column for subsequent rows.