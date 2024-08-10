# airflow_tutorial

## Instalación usando Astro CLI

Es necesario instalar docker y [Astro CLI](https://www.astronomer.io/docs/astro/cli/install-cli?tab=linux#upgrade-the-cli).


```bash
# Iniciar el proyecto
astro dev start

# Arrancar astro con Docker
astro dev start

# Reiniciar
astro dev restart

```

## Comandos de la terminal

Para entrar en la terminal de Docker con Astro:

```bash
sudo astro dev bash
```

Comandos con la base de datos:
```bash
# Check if the metadata database can be reached
airflow db check

# Purge old records in database tables in archive tables
airflow db clean

# Export archived data from the archive table (defaul csv)
airflow db export-archived

# Initialize the database
airflow db init
```

Comandos para dags:
```bash
# Run subsections of a DAG for a specified date range
airflow dags backfill my_dag --reset-dagrun --rerun-failed-tasks --run-backwards -s 2024-01-01 -e 2024-01-10

# Re-sync DAGs
airflow dags reserialize

# List all the DAGs
airflow dags list

``` 

Comandos para tasks:
```bash
# Test a task instance
airflow tasks test my_dag my_task 2024-01-01
```

Para una lisa de todos los comandos:
```bash
airflow cheat-sheet
```