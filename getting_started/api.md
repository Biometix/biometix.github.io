---
layout: default
title: BQAT API
parent: Getting Started
nav_order: 2
---

## Installation

This project run as a server which provides BQAT functionalities as RESTful API.

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

# Start container stack locally
docker compose up -d

# Stop the services (ctrl + C)
docker compose down
```

## Usage
The documentation of the endpoints lives in:
* `localhost:8848/docs`

In dev mode, there is an management frontend for the database:
* `localhost:8081/`
