# Setup Guide

## Docker Setup
1. Ensure you have Docker installed on your machine.
2. Clone the repository:
   ```bash
   git clone https://github.com/amanji0/campus-social.git
   cd campus-social
   ```
3. Build the Docker images:
   ```bash
   docker-compose build
   ```
4. Start the Docker containers:
   ```bash
   docker-compose up
   ```

## Database Migrations
1. Migrate your database:
   ```bash
   docker-compose run web python manage.py migrate
   ```
   Replace `web` with your service name if different.
2. Create a superuser (optional):
   ```bash
   docker-compose run web python manage.py createsuperuser
   ```

## Development Server Startup Instructions
1. To start the development server, run:
   ```bash
   docker-compose run web python manage.py runserver 0.0.0.0:8000
   ```
2. Access the application in your browser at `http://localhost:8000`.

3. For hot reloading, make sure you have the appropriate configuration set up in your Dockerfile according to your development needs.

---

This guide will help you to set up the project locally using Docker. If you encounter any issues, consult the project's documentation or reach out to the maintainers.