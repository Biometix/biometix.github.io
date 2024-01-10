---
layout: default
title: BQAT GUI
parent: Getting Started
nav_order: 4
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

# BQAT GUI

<a name="setup">
## Setup

This project is run as a docker stack which provides a simple web GUI for BQAT-API access. You can simply start it with the Docker Compose file provided.

### Get the Docker Compose file

> [Download](https://raw.githubusercontent.com/Biometix/bqat-gui/main/compose.yaml){: .btn }

## Usage

+ Download the docker [compose file](https://raw.githubusercontent.com/Biometix/bqat-gui/main/compose.yaml) into your working directory.
+ Start the BQAT Web GUI service:


``` sh
# Start container stack
docker compose up -d

# Stop the services (ctrl + C)
docker compose down
```

## Web GUI

Find the page at:

* `localhost:7860`

## Detailed Info
+ [GUI Solution](https://biometix.github.io/solutions/gui.html)
