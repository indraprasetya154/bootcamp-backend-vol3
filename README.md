#  Docker Setup Guide
This guide covers three cases for setting up and running various Docker configurations. Follow the instructions based on the case that applies to your setup.

---

##  Case 1: Golang Docker
This case demonstrates how to build a Golang Docker image.

1. Navigate to the `1-dockerfile/` directory:

```bash

cd 1-dockerfile/

```

2. Build the Docker image:

```bash

docker build -t golang-docker -f .docker/Dockerfile .

```

3. Optional: For a smaller file size, use the multi-stage distroless build:

```bash

docker build -t golang-docker -f .docker/Dockerfile.multistage-distroless . --no-cache

```

---

##  Case 2: Docker Compose with MinIO
This case sets up a Docker Compose configuration with MinIO.

1. Navigate to the `2-docker-compose-minio/` directory:

```bash

cd 2-docker-compose-minio/

```

2. Start the services using Docker Compose:

```bash

docker compose up -d

```

3. To stop the services, use one of the following commands:

```bash

docker compose stop

```

or

```bash

docker compose down

```
 --- 

##  Case 3: Docker Compose with App and MySQL

This case configures Docker Compose for an application with a MySQL database.

  

1. Navigate to the `3-docker-compose-app-mysql/` directory:

```bash

cd 3-docker-compose-app-mysql/

```

2. Copy the example environment file:

```bash

cp .env.example .env

```

3. Start the services with Docker Compose:

```bash

docker compose up -d

```

4. To stop the services, use one of the following commands:

```bash

docker compose stop

```

or

```bash

docker compose down
