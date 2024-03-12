### SQL Island

```sql
SELECT * FROM inhabitant
```

```sql
SELECT * FROM inhabitant WHERE state='friendly';
```

```sql
 SELECT * FROM inhabitant WHERE state='friendly' AND job='weaponsmith';
```

```sql
SELECT * 
FROM inhabitant
WHERE state = "friendly"
AND job LIKE "%smith";
```

```sql
SELECT personid FROM inhabitant WHERE name='Stranger';
```

```sql
SELECT gold FROM inhabitant WHERE name='Stranger';
```

```sql
SELECT * FROM item WHERE owner IS NULL;
```

```sql
UPDATE item 
SET owner = 20 
WHERE owner IS NULL;
```

```sql
SELECT * 
FROM ITEM 
WHERE owner = 20
```

```sql
SELECT * 
FROM INHABITANT 
WHERE state = "friendly" 
AND job = "dealer" 
OR job = "merchant";
```
```sql
UPDATE item 
SET owner = 15 
WHERE item = "ring"
OR item = "teapot";
```

```sql
UPDATE inhabitant 
SET name = "Kai" 
WHERE personid = 20
```

```sql
SELECT * 
FROM inhabitant 
WHERE job = "baker" 
ORDER BY gold DESC
```
