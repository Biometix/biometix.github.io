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
