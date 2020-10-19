# useful_sql
useful sql commands 

## Basics
#### Insert
```
INSERT INTO table (column_1, column_2, column_3)
VALUES (value_1, value_2, value_3);
```

#### Select
**Example with WHERE and AND condition.**
```
SELECT column_1, column_2, column_3
FROM table_name
WHERE *condition*
AND *condition*;
```
#### Update
**Example with WHERE and OR condition.**
```
UPDATE table_name
SET column_1 = value_1, column_2 = value_2
WHERE *condition*
OR *condition*;
```

#### Delete
**Example with WHERE condition.**
```
DELETE FROM table_name
WHERE *condition*;
```
---
### Databases
```
CREATE DATABASE db_name;

DROP DATABASE db_name;
```
---
### Tables
#### Create
**Example with PRIMARY KEY, VARCHAR and INT datatypes, NOT NULL and custom named UNIQUE constraint.**
```
CREATE TABLE table_name
(
id INT PRIMARY KEY,
column_name_1 VARCHAR(50) NOT NULL,
column_name_2 INT,
CONSTRAINT unique_constraint_name UNIQUE (column_name_2)
);
```
List of data types: http://www.tutorialspoint.com/sql/sql-data-types.htm

List of constraints: http://www.tutorialspoint.com/sql/sql-constraints.htm

#### Delete
`DROP TABLE table_name;`

#### Altering Tables

##### Add Column
```
ALTER TABLE table_name
ADD COLUMN column_name *datatype*;
```

##### Delete Column
```
ALTER TABLE table_name
DROP COLUMN column_name;
```

##### Modify Datatype
```
ALTER TABLE table_name
MODIFY COLUMN column_name *datatype*;
```

##### Adding Constraints
**Example using condition check.**
```
ALTER TABLE table_name
ADD CONSTRAINT constraintname CHECK column_1 < 50;
```
**Example with UNIQUE value constraint**
```
ALTER TABLE table_name
ADD CONSTRAINT constraintname UNIQUE (column_1, column_2, column_3);
```
**Example with PRIMARY KEY constraint**
```
ALTER TABLE table_name
ADD CONSTRAINT primarykeyname PRIMARY KEY (column_1);
```
##### Removing Constraints
```
ALTER TABLE table_name
DROP CONSTRAINT constraintname;
```
