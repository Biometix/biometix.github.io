---
layout: default
title: BQAT API
parent: Getting Started
nav_order: 2
---
# BQAT API

---
<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

---


<a name="setup">
## Setup

This project is run as a server which provides BQAT functionalities as RESTful API. You can simply pull the Docker image and start it with the Docker Compose file provided.

### Get the Docker Compose file

> [Download](https://raw.githubusercontent.com/Biometix/bqat-api/main/compose.yaml){: .btn }

### Pull the Docker Image from Registry

``` sh
# Pull the image
docker pull ghcr.io/biometix/bqat-api:latest
```

<a name="usage">
## Usage

+ Download the docker [compose file](https://raw.githubusercontent.com/Biometix/bqat-api/main/compose.yaml) into your working directory.
+ Create a `data/` folder within your working directory and put your input images in this folder.
+ Start the BQAT API service:

``` sh
# Start container stack
docker compose up -d

# Stop the service
docker compose down
```

> Note: The server is designed to be executed with a `/data` folder in your working directory. The `/data` folder (where all the images are stored) will be mounted to the container. Read and write permission is required for this folder. You should be fine as long as you created the folder before spinning up the server. Otherwise you need to change the ownership of the folder.

<a name="api">
## API

The documentation of the API endpoints lives in:

* `localhost:8848/docs`

> [MORE](https://biometix.github.io/solutions/api.html) about endpoints.

## Detailed Info
+ [API Solution](https://biometix.github.io/solutions/api.html)
