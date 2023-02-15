# dbt-learning

setting up dbt-core on windows :

1. Install python3.7+ version 
2. Install git 
3. create a venv in python using : "python3 -m venv dbt-env"
4. activate the venv using : "dbt-env\Scripts\activate"
5. to install dbt-core using pip :
	pip install  dbt-core  dbt-postgres  dbt-redshift  dbt-snowflake  dbt-bigquery


dbt CLI:
	The target/compiled/ directory for compiled select statements
	The target/run/ directory for compiled create statements
	The logs/dbt.log file for verbose logging.

profiles.yml:
	this file contains all configuration of sources and destnations (i.e.BQ/Snowflake/Redshift/postgres)
	this file is located at  C:/Users/<your_username>/.dbt/profiels.yml

Seed are useful for loading country codes, employee emails, or employee account IDs
      

DBT Job steps :
	Clone Git Repository with deployment code
	Create Profile from Connection BigQuery
	Invoke dbt deps :Pull the most recent version of the dependencies listed in packages.yml
	Invoke dbt source snapshot-freshness : Checks the freshness of source tables without breaking the job
	Invoke dbt build : Run all Seeds, Models, Snapshots, and tests in DAG order


Most dbt commands (and corresponding RPC methods) produce artifacts:
	manifest: produced by build, compile, run, test, docs generate, ls
	run results: produced by build, run, test, seed, snapshot, docs generate
	catalog: produced by docs generate
	sources: produced by source freshness

