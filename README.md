# SQL Examples


the list of CITY names from STATION that do start with vowels.

```sql
SELECT city FROM station WHERE city REGEXP '^([aeiou]{1,1}).*$';
```

the list of CITY names from STATION that do not start with vowels and contains not duplicates.

```sql
SELECT DISTINCT city FROM station WHERE city REGEXP '^([aeiou]{1,1}).*$' = 0; 
```
