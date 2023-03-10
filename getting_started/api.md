---
layout: default
title: BQAT API
parent: Getting Started
nav_order: 2
---

# BQAT API

## Setup

This project is run as a server which provides BQAT functionalities as RESTful API. You can simply pull the Docker image and start it with the Docker Compose file provided.

### Get the Compose file

[Download](https://raw.githubusercontent.com/Biometix/bqat-api/main/docker-compose.yml){: .btn }

### Pull the Docker Image from Registry

``` sh
# Pull the image
docker pull ghcr.io/biometix/bqat-api:latest
```

### _Or_ Build the Image Locally

``` sh
# Clone the repo
git clone https://github.com/Biometix/bqat-api.git

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

## API

The documentation of the API endpoints lives in:

* `localhost:8848/docs`
