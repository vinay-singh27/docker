# Docker and Kubernetes Code Examples

This repository contains code examples and tutorials related to Docker and Kubernetes. It aims to help you understand and practice containerization and orchestration techniques using these powerful tools.<br>

## Content
1. A simple web application build using Docker
2. Visit counter application using Docker


## Docker Notes

### Basic Commands

| Command  | Description      |
|----------|------------------------------------------|
| `docker run image_name`           | This command creates an image with the specified image name. It also creates a container which runs the image with the default command.                         |
| `docker run image_name echo hi`   | This will replace the basic command and will run the `echo hi` command in the container.    |
| `docker create image_name`        | Creates a container for the specified image.                                              |
| `docker start -a image_id`        | Start the image ID.                                                                         |
| `docker ps`                       | List of all the active containers.                                                         |
| `docker system prune`             | Delete all containers and images.                                                           |
| `docker stop image_id`            | Stop the image. Gives it 10 seconds to stop.                                               |
| `docker kill image_id`            | Stops the image instantaneously.                                                            |
| `docker exec -it container_id {command}` | Access the command prompt of the Docker container.                                   |


### Docker Build

- Docker build is used to create custom docker images using the base images
- Format of the Dockerfile
    - Specify the base image  → FROM
    - Set the working directory → WORKDIR
    - Copy the file → COPY . .
    - Run the installation commands → RUN npm install
    - Specify the startup command → CMD [”python”, “main.py”]
- Command
    - docker build -t image_tag_name .
- Port Mapping → To map any outside traffic into docker we need to map the ports
    - e.g., docker run -p 8080:8080 -t vinaysin/simpleapp .
    - Ensure that the same folder has the dockerfile
- Running using different dockerfile name
    - e.g., docker build -f Dockerfile.dev


### Docker Compose

- To run multiple services, we can use docker compose
- Format of the docker-compose.yml file
    - version: “3”
    - services :
        - app_name



| Command  | Description      |
|----------|------------------------------------------|
| `docker-compose up` | This command creates an image with the specified image name. It also creates a container which runs the image with the default command.  |
| `docker-compose down` | This will replace the basic command and will run the `echo hi` command in the container.  |


