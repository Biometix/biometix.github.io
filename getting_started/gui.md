---
layout: default
title: BQAT GUI
parent: Getting Started
nav_order: 4
---

# BQAT GUI

## Setup

This project is run as a docker stack which provides a simple web GUI for BQAT-API access. You can simply start it with the Docker Compose file provided.

### Get the Compose file

[Download](https://raw.githubusercontent.com/Biometix/bqat-gui/main/compose.yaml){: .btn }

## Usage

Under the directory where you put the compose file:

``` sh
# Start container stack
docker compose up -d

# Stop the services (ctrl + C)
docker compose down
```

## Web GUI

Find the page at:

* `localhost:7860`
