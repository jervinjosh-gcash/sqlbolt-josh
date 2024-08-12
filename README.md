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
ORDER BY longitude ASC;
```

Query 4
```
SELECT city, population FROM north_american_cities
WHERE country LIKE "mexico"
ORDER BY population DESC
LIMIT 2;
```

Query 5
```
SELECT city, population FROM north_american_cities
WHERE country LIKE "United States"
ORDER BY population DESC
LIMIT 2 OFFSET 2;
```

#### SQL Review 2 (Lesson 12)

Query 1
```
SELECT director, COUNT() FROM movies
GROUP BY director;
```

Query 2
```
SELECT director, (SUM(domestic_sales) + SUM(international_sales)) AS Total_Director_Sales FROM movies
LEFT JOIN boxoffice
    ON movies.id = boxoffice.movie_id
GROUP BY director;
```
