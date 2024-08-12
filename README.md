# sqlbolt-josh

## SQL Review 1 


### No. 1
SELECT city, population FROM north_american_cities
WHERE country LIKE "Canada";

### No. 2
SELECT * FROM north_american_cities
WHERE country LIKE "United States"
ORDER BY latitude DESC ;

### No. 3
SELECT * FROM north_american_cities
WHERE longitude < -87.629798
ORDER BY longitude DESC;

### No. 4
SELECT * FROM north_american_cities
WHERE country LIKE "mexico"
ORDER BY population DESC
LIMIT 2;

### No. 5
SELECT * FROM north_american_cities
WHERE country LIKE "United States"
ORDER BY population DESC
LIMIT 2 OFFSET 2;
