## Project overview

This project is an ETL data engineering pipeline designed to automate the process of ingesting, transforming, and analyzing data from our internal provider. It consists of a Lakeflow pipeline built using Python, with the primary components being individual .py scripts that handle different stages of the ETL process, Databricks notebooks for exploratory data analysis, a dashboard for data reporting, and a Lakeflow job to orchestrate and schedule the entire process. The release management is automated in our CI/CD system. 


## Project Structure

```plaintext
.
├── Pipelines/
│   ├── ingestion_pipeline.yml   # Ingests data from source 1
│   ├── ingest_data_source_1.py  # Ingests data from source 1
│   ├── ingest_data_source_2.py  # Ingests data from source 2
│   ├── transform_data_step_1.py # First step of data transformation
│   ├── transform_data_step_2.py # Second step of data transformation
│   ├── load_data.py             # Loads the transformed data into the target database
│   └── utils.py                 # Utility functions for the pipeline
├── Notebooks/
│   ├── data_exploration_1.ipynb # Exploratory data analysis for source 1
│   ├── data_exploration_2.ipynb # Exploratory data analysis for source 2
│   └── data_quality_check.ipynb # Data quality checks and validation
├── Dashboards/
│   ├── dashboard_name
├── Jobs/
│   ├── schedule_workflow.job.yml      # Workflow scheduling script
│   └── config.yaml               # Configuration file for the scheduler
├── README.md                     # Project README file
└── requirements.txt              # List of dependencies


