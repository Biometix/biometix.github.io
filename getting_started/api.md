---
layout: default
title: BQAT API
parent: Getting Started
nav_order: 2
---

# BQAT API

[![GitHub Tag](https://img.shields.io/github/v/tag/biometix/bqat-api)](https://github.com/Biometix/bqat-api/releases)

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

This project is run as a server which provides BQAT functionalities as RESTful API. To begin, simply pull the Docker image and start it with the Docker compose file provided. 

### Download the Docker Compose file
{: .no_toc }

> [Download](https://raw.githubusercontent.com/Biometix/bqat-api/main/compose.yaml){: .btn }


<a name="usage">
## Usage

+ Download the docker [compose file](https://raw.githubusercontent.com/Biometix/bqat-api/main/compose.yaml) into your working directory.
+ Create a `data` folder within your working directory and put your input images in this folder.
+ Start the BQAT API service:

``` sh
# Start container stack
docker compose up -d

# Stop the service
docker compose down
```

> Note: The tool is designed to be executed with a `/data` folder in your working directory. The `/data` folder (where all the images are stored) will be mounted to the container. “Read and write” permission is required for this folder. It should work as long as the folder was created before spinning up the server. Otherwise, the ownership of the folder will need to be changed. 

<a name="api">
## API

The documentation of the API endpoints lives in:

* `localhost:8848/docs`

## Further Details
{: .no_toc }
+ [API Cookbook](https://biometix.github.io/cookbook/api.html)
