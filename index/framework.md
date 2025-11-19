---
layout: default
title: Framework
nav_order: 5
permalink: /framework/
---

# Framework

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

## Project Diagram

 The BQAT (Biometric Quality Assessment Tool) framework consists of the [core](https://github.com/Biometix/bqat-core) algorithm component, a [command line interface](https://github.com/Biometix/bqat-cli), a [web API server](https://github.com/Biometix/bqat-api), and a [web application for the API](https://github.com/Biometix/bqat-gui).

``` mermaid
---
title: Biometric Quality Assessment Tool
config:
  theme: neutral
  layout: elk
---
graph TD
    subgraph BQAT
        core((BQAT Core)) --> cli(BQAT CLI)
        core((BQAT Core)) --> api(BQAT API)
        core((BQAT Core)) --> gui(BQAT GUI)
    end
```


### BQAT Core

The core component of BQAT is implemented as a Python package, which links vendor algorithms together, including face, fingerprint, iris and voice modules. 

It will analyse the input biometric samples using the corresponding processing engine and produce the quality metrics. 

``` mermaid
---
title: BQAT Core
config:
  theme: neutral
  layout: elk
---
graph LR
    input(Biometric samples) --> core{Core}
    core{Core} --> face(Face)
    core{Core} --> finger(Fingerprint)
    core{Core} --> iris(Iris)
    core{Core} --> speech(Speech)
```

### Interfaces

The BQAT core exposed via different interfaces (CLI, API, and GUI), which handle data loading, data management and task queueing.

***

``` mermaid
---
title: BQAT CLI
config:
  theme: neutral
  layout: elk
---
graph LR
    input(Input Folder) --> cli{Command Line}
    cli{Command Line} --> report(EDA Report)
    cli{Command Line} --> output(CSV)
    cli{Command Line} --> log(Log)
```

+ The BQAT CLI provides terminal commands to interact with BQAT core.

+ It takes a folder in your file system as input and produces the raw metrics in CSV along with a EDA report.

+ It is distributed as Docker container.

***

``` mermaid
---
title: BQAT API
config:
  theme: neutral
  layout: elk
---
graph LR
    file(File System) --> api{Endpoints}
    upload(HTTP) --> api{Endpoints}
    api{Endpoints} --> db[(Database)]
    db[(Database)] --> report(EDA Report)
    db[(Database)] --> output(JSON)
    db[(Database)] --> log(Log)
```

+ The BQAT API adds task management and storage on top of BQAT core functionalities.

+ It handles inputs individual scanning tasks, and saves the output into a document database which can be accessed via RESTful API.

+ It is designed to be a web server that requires a frontend to interact with.

+ Vertical scaling only.

+ It is distributed as Docker container.

***

``` mermaid
---
title: BQAT Stateless
config:
  theme: neutral
  layout: elk
---
graph LR
    upload(HTTP) --> api{Endpoints}
    api{Endpoints} --> output(JSON Response)
```

+ BQAT Stateless is a stateless version of BQAT API. Without the task management and database, it will return the raw output as standard JSON responses.

+ It handles biometric samples asynchronously, either in raw file or base64 string.

+ It is designed to be a web server that requires a frontend to interact with, as well as a middleware to manage load balancing.

+ Vertical and horizontal scaling possible.

+ Serverless/FaaS deployment possible.

+ It is distributed as Docker container.

***

``` mermaid
---
title: BQAT GUI
config:
  theme: neutral
  layout: elk
---
graph LR
    upload(Upload) --> gui{Web}
    gui{Web GUI} --> api(BQAT-API)
    api(Backend) --> db[(Database)]
    db[(Database)] --> report(EDA Report)
    db[(Database)] --> output(Raw CSV)
    db[(Database)] --> outlier(Outliers Detected)
```

+ BQAT GUI is a web application for BQAT API.

+ Can be deployed as web site or desktop application.

+ Vertical scaling only.

+ It is distributed as Docker container.


## Solution Architecture

``` mermaid
---
title: BQAT Core
config:
  theme: neutral
  layout: elk
---
flowchart TD
 subgraph s1["Python Package"]
    n0["Python Interface"]
    n0 --> n1["Face Engines"]
    n1 --> a1["Biometix"]
    n1 --> a2["OFIQ"]
    n1 --> a3["BIQT"]
    n0 --> n2["Iris Engine"]
    n2 --> a4["BIQT"]
    n0 --> n3["Fingerprint Engine"]
    n3 --> a5["NFIQ2"]
    n0 --> n4["Voice Engine"]
    n4 --> a6["NISQA"]
  end
```

---
``` mermaid
---
title: BQAT CLI
config:
  theme: neutral
  layout: elk
---
flowchart TD
  subgraph s1["Docker Container"]
    n0["Python Commands"] --> n1["Ray Parallel Processing Framework"]
    n1 --> n2["BQAT-Core"]
  end
  s1 --> n3["Shell Commands"]
```

---

``` mermaid
---
title: BQAT API
config:
  theme: neutral
  layout: elk
---
flowchart TD
  subgraph s1["FastAPI Web Server"]
    n0["Web API Endpoints"] --> n1["Ray Parallel Processing Framework"]
    n1 --> n2["BQAT-Core"]
  end
  s1 --> n3["Database (MongoDB)"]
  s1 --> n4["Task Queue (Redis)"]

```

---
``` mermaid
---
title: BQAT GUI
config:
  theme: neutral
  layout: elk
---
flowchart LR
  subgraph s1["Docker Compose Stack"]
    n1["Vue.js Web Application"] --> n2["BQAT-API"]
  end
```

---

``` mermaid
---
title: BQAT Stateless
config:
  theme: neutral
  layout: elk
---
flowchart TD
  subgraph s1["FastAPI Web Server"]
    n0["Web API Endpoints"] --> n1["BQAT-Core"]
    n1["BQAT-Core"]
  end

```

## System Requirements

### Operating System

+ x86, ARM platform
+ Linux, Windows, macOS

> Since data processing is compute-intensive, you may want to allocate more cpu/memory with the host machine for better performance and stability.

### Runtime

BQAT deliverables are packaged as Docker containers, you will need Docker engine to host the container.

### Performance Benchmark

Test Platform 1: 6/12 cores, amd64, Ubtuntu 25.10, 16 GB of RAM.

| Mode | Throughput (per second) \| (per hour) |
| --- | --- |
| Face (BQAT) | 9.86 \| 35,496 |
| Face (OFIQ) | 1.02 \| 3,672 |
| Face (BIQT) | 3.75 \| 13,500 |
| Fingerprint (NFIQ2) | 7.16 \| 25,776 |
| Iris (BIQT) | 18.63 \| 67,068 |
| Speech (NISQA) | 0.77 \| 2,772 |

Test Platform 2: 14 cores, arm64, macOS 15.6.1, 32 GB of RAM.

| Mode | Throughput (per second) \| (per hour) |
| --- | --- |
| Face (BQAT) | 53.94 \| 194,184 |
| Face (OFIQ) | 2.08 \| 7,488 |
| Face (BIQT) | 8.54 \| 30,744 |
| Fingerprint (NFIQ2) | 14.54 \| 52,344 |
| Iris (BIQT) | 40.14 \| 144,504 |
| Speech (NISQA) | 1.50 \| 5,400 |


> Baseline testing conducted on BQAT-CLI, and BQAT-API/BQAT-GUI should return similar numbers, but performance of BQAT-Stateless will be determined by upstream load balancer/scheduler.

> As new quality metrics added to the engine, the benchmark number above might not reflect the current status of the project.

### System Scaling

BQAT-CLI, BQAT-API (which is the backend of BQAT-GUI) runs in single node configuration, only vertical scaling is supported. If you want to scale the system horizontally, you can turn to [BQAT-Stateless](https://biometix.github.io/cookbook/stateless.html#scalability).

In terms of cluster deployment for BQAT-Stateless:

| Nodes | Throughput (per second) \| (per hour) |
| --- | --- |
| 1 | 14.1 \| 50,760 |
| 2 | 26.3 \| 94,680 |
| 3 | 53.8 \| 193,680 |

> Test done in iris mode.
