# Spring Observability Playground

This project demonstrates a Spring Boot application with observability features using Prometheus and Grafana. It includes a simple REST API for managing users, and is configured for monitoring with Docker Compose.

## Features

- Spring Boot REST API (users CRUD)
- PostgreSQL database
- Prometheus metrics via Spring Actuator
- Grafana dashboards
- Docker Compose setup for all services

## Prerequisites

- Docker & Docker Compose
- Java 11+ and Maven (for building the app)

## Running the Project

1. **Build the Spring Boot application:**
   ```sh
   mvn clean package
   ```

2. **Start all services using Docker Compose:**
   ```sh
   docker-compose up --build
   ```

3. **Access the services:**
   - Spring Boot API: [http://localhost:8080/users](http://localhost:8080/users)
   - Prometheus: [http://localhost:9090](http://localhost:9090)
   - Grafana: [http://localhost:3000](http://localhost:3000)
     - Default login: `admin` / `admin`

## API Endpoints

- `GET /users` - List all users
- `POST /users` - Create a new user

## Monitoring

- Prometheus scrapes metrics from `/actuator/prometheus` endpoint.
- Grafana can be configured to visualize metrics from Prometheus.

## Configuration

- Database settings and service ports are defined in `docker-compose.yml`.
- Prometheus configuration is in `prometheus/prometheus.yml`.

## License

This project is for educational purposes.
