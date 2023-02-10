---
layout: default
title: BQAT API
parent: Getting Started
nav_order: 2
---

## Setup

This project run as a server which provides BQAT functionalities as RESTful API. You can simply pull the Docker image and start it with the Docker Compose file provided.

> Download: [Docker Compose File](https://github.com/Biometix/bqat-api/blob/main/docker-compose.yml)

### Pull the Docker Image from Registry

``` sh
# Pull the image
docker pull ghcr.io/biometix/bqat-api:latest
```

### Build the Image

You can also build the image locally.

``` sh
# Build the image
docker compose build
```

## Usage

``` sh
# Start container stack locally
docker compose up -d

# Stop the services (ctrl + C)
docker compose down
```

The documentation of the API endpoints lives in:
* `localhost:8848/docs`
