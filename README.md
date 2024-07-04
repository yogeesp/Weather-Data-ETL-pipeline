# Weather-Data-ETL-pipeline

Overview

This project demonstrates an ETL (Extract, Transform, Load) pipeline that extracts weather data from the OpenWeatherMap API, processes it using Apache Airflow, and stores it in AWS services. The project highlights the integration of various data engineering tools and platforms.
Key Components

    OpenWeatherMap API: Source of weather data.
    Apache Airflow: Orchestration tool to manage ETL workflow.
    AWS: Cloud storage and processing services (e.g., S3, Redshift).

Installation
Prerequisites

    Python 3.6 or higher
    Apache Airflow
    AWS Account
    OpenWeatherMap API Key

Installation Steps

    Clone the Repository

    sh

git clone https://github.com/YemiOla/data_engineering_project_openweathermap_api_airflow_etl_aws.git
cd data_engineering_project_openweathermap_api_airflow_etl_aws

Install Python Dependencies

sh

pip install -r requirements.txt

Set Up Apache Airflow

    Follow the official Airflow installation guide.
    Initialize the Airflow database:

    sh

    airflow db init

Configure AWS Credentials

    Ensure AWS CLI is configured with your AWS credentials:

    sh

    aws configure

Set Up Environment Variables

    Create a .env file in the project root directory and add the following variables:

    env

        OPENWEATHER_API_KEY=<your_openweather_api_key>
        AWS_ACCESS_KEY_ID=<your_aws_access_key_id>
        AWS_SECRET_ACCESS_KEY=<your_aws_secret_access_key>
        AWS_REGION=<your_aws_region>

Usage
Running the ETL Process

    Start the Airflow Web Server and Scheduler

    sh

    airflow webserver
    airflow scheduler

    Access the Airflow UI
        Navigate to http://localhost:8080 in your web browser.

    Trigger the ETL DAG
        In the Airflow UI, locate the DAG named weather_etl_dag and trigger it manually.

Interacting with APIs

    The project uses the OpenWeatherMap API to fetch weather data. Ensure your API key is set in the .env file.

Airflow Configuration

    The Airflow DAG (dags/weather_etl_dag.py) is configured to extract weather data, transform it, and load it into AWS services.

Configuration
Configuration Options

    OpenWeatherMap API Key: Set in the .env file.
    AWS Credentials: Set in the .env file.
    Airflow Variables: Configure any additional variables in the Airflow UI under Admin > Variables.

Contributing
Guidelines

    Fork the repository.
    Create a new branch for your feature or bug fix.
    Submit a pull request with a detailed description of your changes.

Reporting Issues

    Use the GitHub Issues page to report bugs or request features.
