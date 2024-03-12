### SQL Island

1
```sql
SELECT * FROM inhabitant
```

2
```sql
SELECT * FROM inhabitant WHERE state='friendly';
```

3
```sql
 SELECT * FROM inhabitant WHERE state='friendly' AND job='weaponsmith';
```

4
```sql
SELECT * 
FROM inhabitant
WHERE state = "friendly"
AND job LIKE "%smith";
```

5
```sql
SELECT personid FROM inhabitant WHERE name='Stranger';
```

6
```sql
SELECT gold FROM inhabitant WHERE name='Stranger';
```

7
```sql
SELECT * FROM item WHERE owner IS NULL;
```

8
```sql
UPDATE item 
SET owner = 20 
WHERE owner IS NULL;
```

9
```sql
SELECT * 
FROM ITEM 
WHERE owner = 20
```

10
```sql
SELECT * 
FROM INHABITANT 
WHERE state = "friendly" 
AND job = "dealer" 
OR job = "merchant";
```

11
```sql
UPDATE item 
SET owner = 15 
WHERE item = "ring"
OR item = "teapot";
```

12
```sql
UPDATE inhabitant 
SET name = "Kai" 
WHERE personid = 20
```

13
```sql
SELECT * 
FROM inhabitant 
WHERE job = "baker" 
ORDER BY gold DESC
```
