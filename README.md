# Jenkins with Docker-in-Docker Configuration
This Docker Compose configuration establishes a comprehensive DevOps environment by integrating Jenkins with Docker-in-Docker (DinD). The setup enables Jenkins to seamlessly build and deploy Docker containers as part of continuous integration and deployment workflows.
## Usage Instructions
Clone Repository:
`git clone https://github.com/dahalapaar/Project2-Compose.git`
`cd Project2-Compose`

## Start Services:
`docker-compose up -d`

## Configuration Details
### Services:
dind: Docker-in-Docker service providing a Docker daemon for Jenkins.

jenkins: Jenkins service with Docker client configured to communicate with the Docker daemon in 'dind'.

### Volumes:
jenkins-data: Volume for persistent Jenkins data.

docker-certs-ca: Volume for Docker CA certificates.

docker-certs-client: Volume for Docker client certificates.

### Networks:
jenkins: Custom bridge network facilitating communication between services.

### Environment Variables:
DOCKER_HOST: Specifies the Docker daemon host for the Jenkins service.

DOCKER_CERT_PATH: Path to Docker client certificates.

DOCKER_TLS_VERIFY: Enables Docker TLS verification.







