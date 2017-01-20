# SQL Examples


the list of CITY names from station that do start with vowels.

```sql
SELECT city FROM station WHERE city regexp '^([aeiou]{1,1}).*$';
```

the list of CITY names from station that do not start with vowels and contains not duplicates.

```sql
SELECT DISTINCT city FROM station WHERE city regexp '^([aeiou]{1,1}).*$' = 0; 
```

the Name of any student in students who scored higher than  Marks. Order your output by the last three characters of each name. If two or more students both have names ending in the same last three characters (i.e.: Bobby, Robby, etc.), secondary sort them by ascending ID.

```sql
select name from students where marks > 75 order by right(name, 3), id asc
```

Check if the age of people in a case statment
```sql
select 
  case 
       when age < 21 then 'Not ok'  
       when age >= 21 then 'ok' 
  end 
from people;
```
the number of ocurrences of each occupation in OCCUPATIONS. 
```sql
SELECT "There are total", COUNT(OCCUPATION), concat(LOWER(OCCUPATION),"s.") FROM OCCUPATIONS GROUP BY OCCUPATION ORDER BY COUNT(OCCUPATION) ASC, OCCUPATION ASC;
```
