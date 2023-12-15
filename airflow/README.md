# Sparkify Data Pipelines

## Date Created
2023-12-14

## Description
This project is all about using Airflow DAGs to import data into Redshift

## How to use
simply let the DAG run , it should do all the work for you

#files used
1. udac_example_dag.py  : the definition of the DAG with all of its operators/tasks/...
				and also the dependencies between them
2. sql_queries.py (plugins/helpers) : all insert statements to fill fact and dim tables
3. load_fact.py (plugin/operators) : definition of the LoadFactOperator
4. load_dimension.py (plugin/operators) : definition of the LoadDimensionOperator
5. stage_redshift.py (plugin/operators) : definition of the StageToRedshiftOperator
6. data_quality.py (plugin/operators) : some tests to see if data is valid
7. create_tables : to run in the Redshift Warehouse before starting
8. README.md : what you're reading right now

# Data
we use JSON files to populate the staging tables.
they are located on 2 S3-buckets

## Credits
Udacity (who provided templates and data)
Harald Linseele (who completed the templates )