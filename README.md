# SQL-Intern-task-2-
The table employees will be created.

Several rows will be added.

Some rows will be updated cleanly (filling NULLs, adjusting values).

Some records will be deleted using conditions.

The data will be clean and consistent.

CREATE TABLE employees (
    emp_id INTEGER PRIMARY KEY,
    name TEXT NOT NULL,
    department TEXT,
    salary REAL DEFAULT 30000,
    email TEXT
);
 In SQLite, TEXT and VARCHAR(n) are both valid types — but there’s a key difference to understand:
 **TEXT**: This is the preferred standard, and it stores variable-length strings with no character limit.
**VARCHAR(n)**: SQLite ignores the length n — so VARCHAR(50) and TEXT behave the same.

CREATE TABLE employees (
    emp_id INTEGER PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    department VARCHAR(50),
    salary REAL DEFAULT 30000,
    email VARCHAR(100)
);
In other databases like MySQL or PostgreSQL, VARCHAR(n) does enforce the limit. But not in SQLite.
