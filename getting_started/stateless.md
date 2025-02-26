---
layout: default
title: BQAT Stateless
parent: Getting Started
nav_order: 3
---

# BQAT Stateless

<img alt="GitHub tag (latest by date)" src="https://img.shields.io/github/v/tag/biometix/bqat-stateless">

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

This project is run as a server which provides BQAT functionalities as RESTful API. To start, simply pull the Docker image and start it with the Docker compose file provided. Instead of storing the results in a database, this stateless server will not store any information locally and the output will be returned directly. 

### Download the Docker Compose file
{: .no_toc }

> [Download](https://raw.githubusercontent.com/Biometix/bqat-stateless/main/compose.yaml){: .btn }

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

>  The image is suitable for k8s deployment as well.

<a name="api">
## API

The documentation of the API endpoints lives in:

* `localhost:8848/docs`


## Further Details
{: .no_toc }
+ [Stateless API Playbook](https://biometix.github.io/playbook/stateless.html)
