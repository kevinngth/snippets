# sql-snippets
Collection of SQL snippets

```SQL
DECLARE @variable VARCHAR(32)
INSERT INTO comment (column) values ('comment')
SET @variable = SCOPE_IDENTITY()
UPDATE article SET comment_id=@variable WHERE article.id = 123;
```

```SQL
CAST('2020-12-31' AS DATETIME)
CONVERT(date, '20190509', 112)
```

```SQL
GETDATE()
```

## WIP
```SQL
UPDATE target
SET target.comment_id = origin.comment_id
FROM target
INNER JOIN (
SELECT *
FROM ??? 
WHERE as_of = convert(date, '20190509', 112)
) origin on (origin.id = target.id)
where target.comment_id is null
and target.status != 2;
```
