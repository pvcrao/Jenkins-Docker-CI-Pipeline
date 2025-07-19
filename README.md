# Jenkins Docker CI/CD Pipeline

This project demonstrates a basic CI/CD pipeline using Jenkins that:
- Clones a GitHub repository
- Builds a Docker image
- Pushes the image to Docker Hub
- (Optional) Deploys to a remote server

## Project Structure

- `Dockerfile`: Defines the Docker image using Nginx to serve a simple HTML app.
- `Jenkinsfile`: Jenkins pipeline script to automate the CI/CD process.
- `app/`: Contains a sample HTML file.
- `scripts/deploy.sh`: Placeholder for remote deployment logic.

## How to Use

1. Set up Jenkins with Docker and required credentials.
2. Create a pipeline pointing to this repository.
3. Watch the pipeline clone, build, push, and deploy your app!

## Author

Vishnu Polisetti
