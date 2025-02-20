# Nexus Repository Installation with Docker Compose

This repository provides a step-by-step guide to setting up a Nexus Repository Manager using Docker Compose.

## Prerequisites

Before proceeding, ensure you installed the docker and docker docker-compose

### 1. Clone the Repository

mkdir nexus-repository
cd nexus-repository

### 2. Create the `docker-compose.yml` File

Create a `docker-compose.yml` and use 

### 3. Start Nexus Repository

Run the following command to start Nexus Repository:

```sh
docker-compose up -d
```

This command will download the Nexus Repository image, create a container, and start it in detached mode.

### 4. Access Nexus Repository

Once the container is up and running, open your web browser and navigate to:

```
http://localhost:8081
```

## Usage

### Default Admin Credentials

- **Username:** `admin`
- **Password:** Retrieve from the container logs:

  docker-compose logs nexus | grep "admin password"

**Note:** Change the default password after the first login for security purposes.

## Persistent Data

The Nexus data is stored in a Docker volume named `nexus-data`, ensuring that your data persists across container restarts.

## Stopping the Service

To stop the Nexus Repository Manager, run:

```sh
docker-compose down
```


