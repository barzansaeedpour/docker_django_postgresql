
# Docker with Django and PostgreSQL

This repository demonstrates how to containerize a Django application with a PostgreSQL database using Docker. Docker allows you to package your application, its dependencies, and the database into separate containers, providing a consistent and portable environment for development and deployment.

## Prerequisites

Before getting started, make sure you have the following prerequisites installed on your machine:

- Docker: [Install Docker](https://docs.docker.com/get-docker/)
- Docker Compose: [Install Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

Follow the steps below to run the Django application with PostgreSQL using Docker:

1. Clone this repository:

   ```shell
   git clone https://github.com/barzansaeedpour/docker_django_postgresql.git
   cd docker_django_postgresql
   ```

2. Build the Docker images and start the containers:

   ```shell
   docker-compose up --build
   ```

   The `docker-compose.yml` file defines the services for the Django application and the PostgreSQL database. Running the command above will build the necessary Docker images and start the containers.

3. Access the Django application in your web browser:

   ```
   http://localhost:8000
   ```

4. Access the PostgreSQL database using a database client:

   - **Host**: `localhost`
   - **Port**: `5432`
   - **Username**: `postgres`
   - **Password**: `postgres`
   - **Database**: `postgres`

## Project Structure

The project structure is organized as follows:

```
.
├── docker-compose.yml
├── Dockerfile
├── README.md
├── testproject
│   ├── __init__.py
│   ├── settings.py
│   ├── asgi.py
│   ├── urls.py
│   └── wsgi.py
├── manage.py
└── requirements.txt
```

- `docker-compose.yml`: The Docker Compose configuration file that defines the services and their configurations, including the Django application and the PostgreSQL database.
- `Dockerfile`: The Dockerfile that describes how to build the Docker image for the Django application.
- `README.md`: This file, providing instructions and information about the project.
- `testproject/`: The Django application directory.
  - `settings.py`: The Django project settings file.
  - `urls.py`: The Django project URLs configuration.
  - `wsgi.py`: The WSGI application entry point.
- `manage.py`: The Django management script.
- `requirements.txt`: The Python dependencies file for the Django application.

## Customization

You can customize the Django application, the PostgreSQL configuration, or the Docker setup according to your project requirements. Here are some possible modifications:

- Update the Django application code inside the `djangoapp` directory.
- Modify the `docker-compose.yml` file to adjust service configurations, add environment variables, or mount volumes.
- Extend the `Dockerfile` to install additional dependencies or perform custom setup steps.
- Customize the PostgreSQL configuration by modifying the `docker-compose.yml` file.

## Contributing

If you have any suggestions, improvements, or bug fixes, please feel free to contribute to this repository. Fork the repository, make your changes, and submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).

---

Feel free to adjust and expand this `README.md` file to fit the specific needs and details of your Django project with PostgreSQL using Docker.