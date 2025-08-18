### [DBT](https://www.python.org/) commands

#### DBT General
- Initing a project
```sh
    dbt init <project-name>
    dbt init dbtlearn
```

- Check id the connections works
```sh
    dbt debug
```

- Run dbt models
```sh
    dbt run
```

- Run dbt models selecting a model
```sh
    dbt run --select <model_name>
```

- Run dbt models and force regenerate whole the table
```sh
    dbt run --select <model_name> --full-refresh 
```

- Run dbt models, select a target and profiles-dir, and force regenerate whole the table
```sh
    dbt run --select <model_name> --target <target_name> --profiles-dir .  --full-refresh 
    dbt run --select product --target dev --profiles-dir .  --full-refresh 
```

- Run with var
```sh
    dbt run --select <model> --vars <vars>
    dbt run --select fct_reviews --vars '{start_date: "2024-02-15 00:00:00", end_date: "2024-03-15 23:59:59"}'
```

- Run seed (load csv data in seeds folder)
```sh
    dbt seed
```

- Run compile to make source link
```sh
    dbt compile
```

- Run tests
```sh
    dbt test
    dbt test --select <model_name>
```

- Run build (combine dbt run and dbt test). If some test fails, the running is aborted.
```sh
    dbt build
```
- Run deps to install dependencies and packages (e.g., [dbt-labs](https://hub.getdbt.com/dbt-labs), [calogica](https://github.com/calogica/dbt-expectations))
```sh
    dbt deps
```

- Generate documentation
```sh
    dbt docs generate
```

- See documentation
```sh
    dbt docs serve
    dbt docs serve --port 8081
```

- Run macros
```sh
    dbt run-operation <macro>
    dbt run-operation learn_logging
    dbt run-operation learn_variables
```

