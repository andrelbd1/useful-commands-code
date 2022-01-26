### [PostgreSQL](https://www.postgresql.org/) commands

#### General
- Access the PostgreSQL
````bash
psql -U [username]
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
