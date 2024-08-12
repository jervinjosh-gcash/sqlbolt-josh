# sqlbolt-josh

#### SQL Review 1 

Query 1
```
SELECT city, population FROM north_american_cities
WHERE country LIKE "Canada";
```

Query 2
```
SELECT * FROM north_american_cities
WHERE country LIKE "United States"
ORDER BY latitude DESC ;
```

Query 3
```
SELECT * FROM north_american_cities
WHERE longitude < -87.629798
ORDER BY longitude DESC;
```

Query 4
```
SELECT * FROM north_american_cities
WHERE country LIKE "mexico"
ORDER BY population DESC
LIMIT 2;
```

Query 5
```
SELECT * FROM north_american_cities
WHERE country LIKE "United States"
ORDER BY population DESC
LIMIT 2 OFFSET 2;
```
