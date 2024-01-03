### [PostgreSQL](https://www.postgresql.org/) commands

#### General
- Access the PostgreSQL
````bash
psql -U [username]
````
````bash
psql -h [host] -p [port] -U [username] [database]
````

- Connect to a specific database
````bash
\c [database_name]
````

- List all databases
````bash
\l
````

- List schemas
````bash
\dn
````

- List all schemas
````bash
\dn *.*
````

- List all schemas to get more information
````bash
\dn+
````

- List all tables
````bash
\dt
````

- List all tables from a schema
````bash
\dt [schema].*
````

- List all tables to get more information
````bash
\dt+
````

- Get detailed information on a table 
````bash
\d+ [table_name]
````

- List all users
````bash
\du
````

- Run sql file
````bash
\i [file_path.sql]
````

- List tables in lock
````bash
SELECT
  l.locktype,
  t.relname,
  l.page,
  l.virtualtransaction,
  l.pid,
  l.mode,
  l.granted
FROM pg_locks l,
     pg_stat_all_tables t
WHERE l.relation = t.relid
AND t.relname NOT IN ('pg_class', 'pg_index', 'pg_namespace')
ORDER BY relation ASC;
````

- Stop/Kill a query
   - This basically "starts" a request to terminate gracefully, which may be satisfied after some time, though the query comes back immediately.
````bash
SELECT pg_cancel_backend([pid of the process])
````
   - If the process cannot be killed, try:
````bash
SELECT pg_terminate_backend([pid of the process])
````



