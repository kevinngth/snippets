# Code snippets

This is a collection of some of the code that I use daily, so instead of constantly googling the syntax, I can just refer to this page and copy over to my code. 

## CLI snippets

### [gyp: No Xcode or CLT version detected!](https://gist.github.com/kevinngth/5e4098deaf7d2c89a3266075d0d764f7)

## Java snippets

### Stopwatch
```java
System.out.println("start stopwatch");
long t = System.currentTimeMillis();
// code to be tested for speed
System.out.println("code took " + (System.currentTimeMillis() - t) + "ms to run"); 

```

## SQL snippets
Collection of SQL snippets

```SQL
CREATE INDEX user_username_asc ON user(username ASC);
```

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
