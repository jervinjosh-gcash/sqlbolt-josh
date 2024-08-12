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

#### SQL PD Task 1

Case 1
```
SELECT * 
FROM mailing_list;
```

Case 2
```
SELECT * 
FROM mailing_list;
```

Case 3:
An illegal site's servers were seized in a recent operation. Please submit all users first names, number of downloads and access times' details.

```
SELECT FirstName, NumberOfDownloads, AccessTime
FROM users;
```

Case 4:
An illegal site's servers were seized in a recent operation. Please submit all users access times and number of posts' details.
```
SELECT AccessTime, Posts
FROM users;
```

Case 5:
A hacked site members' details have surfaced on a darknet forum. Please submit all members addresses' details. Please make sure there are no duplicates.
```
SELECT DISTINCT Address
FROM members;
```

Case 6:
A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit all entries' details sorted by join dates in ascending order.
```
SELECT *
FROM mailing_list
ORDER BY JoinDate ASC;
```

Case 7:
A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit all entries' details sorted by last names in descending order.
```
SELECT * 
FROM mailing_list
ORDER BY LastName DESC;
```

Case 8:
A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit all entries emails, given names and number of promotions sent' details sorted by given names in descending order. Please make sure there are no duplicates.
```
SELECT DISTINCT Email, GivenName, Promotions
FROM mailing_list
ORDER BY GivenName DESC;
```

Case 9:
An illegal site's servers were seized in a recent operation. Please submit all users number of downloads and emails' details sorted by number of downloads in descending order and then by emails in descending order.
```
SELECT Downloads, Email
FROM users
ORDER BY Downloads DESC, Email DESC;
```

Case 10:
White hat hacker has sent SQLPD exposed members' details of a shady site connected to various persons of interest. Please submit the top 3 members' details when sorted by number of purchases in descending order and then by mailing addresses in descending order.
```
SELECT *
FROM members
ORDER BY Purchases DESC, MailingAddress DESC
LIMIT 3;
```

Case 11:
A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit the top 3 entries first names, surnames and join dates' details when sorted by join dates in descending order and then by first names in ascending order. Please make sure there are no duplicates.
```
SELECT DISTINCT FirstName, Surname, Joined
FROM mailing_list
ORDER BY Joined DESC, FirstName ASC
LIMIT 3;
```