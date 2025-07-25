### Select query with constraints
```
SELECT column, another_column, …
FROM mytable
WHERE condition
    AND/OR another_condition
    AND/OR …;
```
| Operator               | Condition                                     | SQL Example                        |
|------------------------|-----------------------------------------------|------------------------------------|
| =, !=, <, <=, >, >=    | Standard numerical operators                   | `col_name != 4`                    |
| BETWEEN … AND …        | Number is within range of two values (inclusive) | `col_name BETWEEN 1.5 AND 10.5`    |
| NOT BETWEEN … AND …    | Number is not within range of two values (inclusive) | `col_name NOT BETWEEN 1 AND 10` |
| IN (…)                 | Number exists in a list                        | `col_name IN (2, 4, 6)`            |
| NOT IN (…)             | Number does not exist in a list                | `col_name NOT IN (1, 3, 5)`        |
| =              | Case sensitive exact string comparison (notice the single equals) | `col_name = "abc"`                   |
| != or <>       | Case sensitive exact string inequality comparison                | `col_name != "abcd"`                 |
| LIKE           | Case insensitive exact string comparison                         | `col_name LIKE "ABC"`                |
| NOT LIKE       | Case insensitive exact string inequality comparison              | `col_name NOT LIKE "ABCD"`           |
| %              | Match any sequence of characters (with LIKE or NOT LIKE)         | `col_name LIKE "%AT%"` (matches "AT", "ATTIC", "CAT", "BATS") |
| _              | Match a single character (with LIKE or NOT LIKE)                 | `col_name LIKE "AN_"` (matches "AND", not "AN") |
| IN (…)         | String exists in a list                                          | `col_name IN ("A", "B", "C")`        |
| NOT IN (…)     | String does not exist in a list                                  | `col_name NOT IN ("D", "E", "F")`    |

