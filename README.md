# Django-Patent-Analytics-API-using-Docker

## Problem Overview

This project involves developing a backend API that provides analytical insights on a patent dataset. The goal is to assess ability to work with data, design a functional API, and handle basic data queries and summary statistics. Additionally, the application is containerized using Docker-Compose.

### API Design
- Use Django as the backend framework to build the REST API.
- The API should allow users to:
  - Retrieve basic summary statistics of the dataset (`/summary`).
  - Query the dataset based on one or two parameters (e.g., `/query?patent_year=2020`).
- Implement at least two endpoints:
  - `/summary`: Returns summary statistics (mean, median, etc.) for numerical columns.
  - `/query`: Filters data based on provided query parameters (e.g., patent year, assignee).

### Docker-Compose
- Containerize the Django application using Docker.
- Use Docker-Compose to manage the services:
  - A web service (Django API).

## Requirements
- Django for building the API.
- Pandas and NumPy for data processing and analysis.
- Version control with Git and hosting on GitHub.
- Dockerfile for the Django project.
- `docker-compose.yml` to manage the services.

## Setup and Running the Project

### Prerequisites
- Docker and Docker-Compose installed on your machine.
- Git installed on your machine.

### Installation

1. **Clone the repository:**

   ```sh
   git clone https://github.com/01Prashant/Django-Patent-Analytics-API-using-Docker.git
   cd Django-Patent-Analytics-API-using-Docker

2. **Build and run the Docker containers:**

   ```sh
   docker-compose build
   docker-compose up

3. **Run migrations:**

   ```sh
   docker-compose exec web python manage.py makemigrations
   docker-compose exec web python manage.py migrate

   
4. **Run the data cleaning script:**

   ```sh
   docker-compose exec web python scripts/dataclean.py

5. **API Endpoints:**
- /summary: Returns summary statistics for numerical columns.
- /query: Filters data based on query parameters (e.g., patent year, assignee).

## Contributing
- Feel free to fork the repository and submit pull requests. Ensure that you follow the coding guidelines and include appropriate tests.
