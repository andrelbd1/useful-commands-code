### [Alembic](https://alembic.sqlalchemy.org/en/latest/index.html) commands

#### General
- Creating an environmnent
````bash
    alembic init alembic
````
- Create a migration script
````bash
    alembic revision -m "create account table"
````
````bash
    alembic revision --autogenerate -m "create account table"
````
- Running all migration scripts
````bash
    alembic upgrade head
````
- Running downgrade back to nothing
````bash
    alembic downgrade base
````
- Running until a specific migration script
````bash
    alembic upgrade [revision]
````
````bash
    alembic upgrade +2
````
````bash
    alembic downgrade -1
````
````bash
    alembic upgrade [revision]+2
````
- Getting information about the current revision
````bash
    alembic current
````
- Getting information about the head(s)
````bash
    alembic heads
````
- View full information about each revision
````bash
    alembic history --verbose
````
- View information about the revisions order
````bash
    alembic history
````
