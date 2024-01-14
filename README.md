
# Kaiburr Task 4 CI/CD Pipeline for Spring Boot API

This repository contains the CI/CD pipeline configuration for building and deploying a Spring Boot API (created in Task 1) using GitHub Actions.

## Workflow

The CI/CD workflow consists of two jobs: `build` and `docker`. The `code` job builds the Spring Boot application with Maven, and the `docker` job builds and pushes a Docker image to Docker Hub.

### Build Job

- **Set Up JDK:** Uses the `actions/setup-java` action to set up Java 21.
- **Build with Maven:** Builds the Spring Boot application using Maven.

### Docker Job

- **Login to Docker Hub:** Uses the `docker/login-action` action to log in to Docker Hub using the provided credentials.
- **Extraction of metadata (tags, labels) for Docker:** Uses the `docker/metadata-action` action to extract metadata for the Docker image.
- **Build and push Docker image:** Uses the `docker/build-push-action` action to build and push the Docker image to Docker Hub.

##My Screenshots
1. Pushing to repository


2. Workflow in progress


3. Workflow completed and Docker Image has been pushed to Docker Hub


## How to Use

1. Fork this repository.
2. Update the Spring Boot API code if needed.
3. Configure the Dockerfile for the Spring Boot application if needed..
4. Update the workflow file (`.github/workflows/maven.yml`) if needed.
5. Add the necessary secrets to your GitHub repository.
6. Trigger the workflow by pushing changes to the `main` branch.

### Secrets
Make sure to add the following secrets to your GitHub repository:

- `DOCKER_USERNAME`: Your Docker Hub username.
- `DOCKER_PASSWORD`: Your Docker Hub password.

