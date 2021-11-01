# Isaak's Project Flows

This repo contains the data pipelines or other recurring jobs that support any of my personal projects! 

A lot of these jobs will be set up as Airflow DAGs. If you're considering doing something like this yourself, understand that **Airflow as a tool is overkill for pretty much ALL of my (and likely all of your) usecases**. I'm using it because it's good practice as a data engineer, and I can run it in pseudo-deployment on my personal machine to support the data needs of my projects. 

tl;dr - probably just throw your recurring jobs in **cron**. 

## What jobs are in here, anyway?

- Law school data processing for the [Law School Debt Calculator](lsdebt.com)

## Running Locally

### Spinning up Airflow 2.2.0

This repo uses **Airflow 2.2.0** running in Docker Compose.

First build the airflow image, 
```bash
docker-compose build
docker-compose up airflow-init
```
This builds an image from the local Dockerfile, then initializes the Airflow DB and creates a default user. 

Finally, run this to start up airflow:
```bash
docker-compose up
```

This should make the Airflow UI available at <http://localhost:8080/>. 
