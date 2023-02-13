---
layout: default
title: BQAT API
parent: Getting Started
nav_order: 2
---

# Setup

This project run as a server which provides BQAT functionalities as RESTful API. You can simply pull the Docker image and start it with the Docker Compose file provided.

> Docker Compose File: [Download](https://github.com/Biometix/bqat-api/blob/main/docker-compose.yml){: .btn }

## Pull the Docker Image from Registry

``` sh
# Pull the image
docker pull ghcr.io/biometix/bqat-api:latest
```

## Or Build the Image Locally

``` sh
# Clone the repo
git clone https://github.com/Biometix/bqat-api.git

# Build the image
docker compose build
```

# Usage
You may setup reverse proxy as needed.

``` sh
# Start container stack locally
docker compose up -d

# Stop the services (ctrl + C)
docker compose down
```

# API

The documentation of the API endpoints lives in:
* `localhost:8848/docs`
