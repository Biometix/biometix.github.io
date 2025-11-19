---
layout: default
title: BQAT GUI
parent: Getting Started
nav_order: 4
---

# BQAT GUI

[![GitHub Tag](https://img.shields.io/github/v/tag/biometix/bqat-gui)](https://github.com/Biometix/bqat-gui/releases)

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

+ Download the docker [compose file](https://raw.githubusercontent.com/Biometix/bqat-gui/main/compose.yaml) to your working directory.
+ Start the BQAT Web GUI service:


### Start BQAT GUI services
{: .no_toc }
``` sh
docker compose --profile default up -d
```

### Stop the services
{: .no_toc }
``` sh
docker compose --profile default down
```

Find the BQAT GUI at:

* `localhost:9949`

> You may configure url, port, proxy and other settings in the compose file.

## Further Details
{: .no_toc }
+ [Web GUI Cookbook](https://biometix.github.io/cookbook/gui.html)
