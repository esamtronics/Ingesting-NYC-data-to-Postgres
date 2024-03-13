## Objective
This project utilizes Docker containers to create a portable development environment for analyzing NYC taxi trip data stored and managed in a PostgreSQL database. The data is ingested using Python scripts and can be further analyzed or visualized with tools like pgAdmin.

![image](https://github.com/esamtronics/Ingesting-NYC-data-to-Postgres/assets/107403255/f63ace8b-db0b-49f1-b25b-c25eeb11e2f8)

> The project is one of DataTalks.club projects

## The project involves the following processes:

1. Containerization with Docker:

    * Docker is used to containerize the application environment, allowing for easy deployment and scalability.
    * Containers are lightweight, portable, and isolated environments that package all necessary dependencies, libraries, and configurations for the application to run consistently across different environments.

2. Setting up PostgreSQL Database:

    * A PostgreSQL database instance is deployed using a Docker container
    * Environment variables such as POSTGRES_USER, POSTGRES_PASSWORD, and POSTGRES_DB are set to configure the PostgreSQL instance.
    * Volume mounts are used to persist data, ensuring that database changes persist even if the container is stopped or restarted.
    * Port mappings are configured to expose the PostgreSQL service to the host machine.

3. Data Ingestion:

    * Data ingestion involves acquiring datasets and loading them into the PostgreSQL database for analysis or processing.
    * The dataset is typically downloaded from a source, such as an online repository or cloud storage, using tools like wget or the AWS CLI.
    * Python scripts may be used to preprocess the data and ingest it into the database. This can involve connecting to the database, creating tables, and inserting data rows.
    * Docker containers may be utilized to run these data ingestion scripts, ensuring consistency and reproducibility of the data loading process.

4. Data Analysis and Processing:

    * Once the data is ingested into the PostgreSQL database, it can be analyzed and processed using SQL queries or other database operations.
    * Tools like pgcli provide a command-line interface for interacting with the PostgreSQL database, allowing users to execute SQL queries, view database schemas, and perform administrative tasks.
    * SQL queries can be used to retrieve specific subsets of data, aggregate data, join multiple tables, or perform complex calculations.

5. Visualization and Administration with pgAdmin:

    * pgAdmin is used as a web-based administration tool for managing the PostgreSQL database.
    * It provides a graphical user interface for visualizing database schemas, executing SQL queries, and performing administrative tasks such as user management and database backups.
    * pgAdmin is deployed as a Docker container, allowing it to be easily managed and accessed through a web browser.

6. Automation with Docker Compose:

    * Docker Compose is used to define and manage multi-container Docker applications.
    It simplifies the process of managing dependencies between Docker containers, configuring their environments, and orchestrating their deployment.
    • With Docker Compose, the entire application stack, including the PostgreSQL database, pgAdmin, and any other services, can be defined in a single docker-compose.yml file and deployed with a single command.
