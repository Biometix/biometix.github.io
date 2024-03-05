---
layout: default
title: BQAT GUI
parent: Getting Started
nav_order: 4
---

# BQAT GUI

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

This project is run as a Docker stack which provides a simple web GUI for BQAT-API access. To begin, simply start it with the Docker compose file provided. 

### Download the Docker Compose file
{: .no_toc }

> [Download](https://raw.githubusercontent.com/Biometix/bqat-gui/main/compose.yaml){: .btn }

<a name="usage">
## Usage

+ Download the docker [compose file](https://raw.githubusercontent.com/Biometix/bqat-gui/main/compose.yaml) into your working directory.
+ Start the BQAT Web GUI service:


``` sh
# Start container stack
docker compose up -d

# Stop the services (ctrl + C)
docker compose down
```

<a name="output">
## Output

Find the page at:

* `localhost:7860`

## Further Details
{: .no_toc }
+ [Web GUI Playbook](https://biometix.github.io/playbook/gui.html)
