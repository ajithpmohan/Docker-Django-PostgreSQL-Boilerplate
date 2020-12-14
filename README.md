# Dockerized Django PostgreSQL Boilerplate

## System Requirements

You need **Docker Engine** and **Docker Compose**. Install it from [Docker Website](https://docs.docker.com/)

## Usage

Download the repository:

    git clone git@github.com:ajithpmohan/docker-django-postgresql-boilerplate.git

## Permission Required

Before building the services update the file permission of `backend/entrypoint.sh`

    chmod +x backend/entrypoint.sh

## Project Setup

Run the following line would build the services and create the project.

    docker-compose run backend django-admin startproject <PROJECT_NAME> .

Change database connection from sqlite to [postgres](https://docs.djangoproject.com/en/3.1/ref/settings/#std:setting-DATABASES)

## Python Environment Setup

Try [python-decouple](https://simpleisbetterthancomplex.com/2015/11/26/package-of-the-week-python-decouple.html) library for handling environment variables.

## Starting App

    docker-compose up -d

## Access the service in the development mode.

Open [http://localhost:7100/](http://localhost:7100/) to access `backend` service in the browser.

## Run Python Code Linter & Formatter

    docker-compose -f pre-commit.yml up --build