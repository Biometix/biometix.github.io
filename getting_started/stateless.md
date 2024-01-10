---
layout: default
title: BQAT Stateless
parent: Getting Started
nav_order: 3
---

# BQAT Stateless

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

This project is run as a server which provides BQAT functionalities as RESTful API. You can simply pull the Docker image and start it with the Docker Compose file provided. In stead of store the results in database, this stateless server will not store any information locally, the output will be returned directly.

### Get the Docker Compose file

> [Download](https://raw.githubusercontent.com/Biometix/bqat-stateless/main/compose.yaml){: .btn }

### Pull the Docker Image from Registry

``` sh
# Pull the image
docker pull ghcr.io/biometix/bqat-stateless:latest
```

<!-- ### _Or_ Build the Image Locally

``` sh
# Clone the repo
git clone https://github.com/Biometix/bqat-stateless.git

# Build the image
docker compose build
``` -->

<a name="usage">
## Usage

+ Download the docker [compose file](https://raw.githubusercontent.com/Biometix/bqat-stateless/main/compose.yaml) into your working directory.
+ Start the BQAT Stateless API service:

``` sh
# Start container stack
docker compose up -d

# Stop the service
docker compose down
```
<a name="api">
## API

The documentation of the API endpoints lives in:

* `localhost:8848/docs`


## Detailed Info
+ [Stateless API Solution](https://biometix.github.io/solutions/stateless.html)
