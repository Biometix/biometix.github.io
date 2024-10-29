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
  theme: mc
  look: handDrawn
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
  theme: mc
  look: handDrawn
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
  theme: mc
  look: handDrawn
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
  theme: mc
  look: handDrawn
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
  theme: mc
  look: handDrawn
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

+ x86 platform
+ Linux, Windows, macOS

> Since data processing is compute-intensive, you may want to allocate more cpu/memory with the host machine for better performance and stability.

### Runtime

BQAT deliverables are packaged as Docker containers, you will need Docker engine to host the container.

### Performance Benchmark

| Mode | Throughput (per second) \| (per hour) |
| --- | --- |
| Face (BQAT) | 52 \| 187,200 |
| Face (OFIQ) | 1.1 \| 3,960 |
| Face (BIQT) | 4.7 \| 16,920 |
| Fingerprint (NFIQ2) | 6.8 \| 24,480 |
| Iris (BIQT) | 17.8 \| 64,080 |

> Test platform: 6 cores / 12 threads CPU, 16GB of RAM.

> Baseline testing done on BQAT-CLI, BQAT-API/BQAT-GUI should return similar numbers, while performance of BQAT-Stateless will be determined by upstream load balancer/scheduler.

### System Scaling

BQAT-CLI, BQAT-API (which is the backend of BQAT-GUI) runs in single node configuration, only vertical scaling is supported. If you want to scale the system horizontally, you can turn to [BQAT-Stateless](https://biometix.github.io/playbook/stateless.html#scalability).

In terms of cluster deployment for BQAT-Stateless:

| Nodes | Throughput (per second) \| (per hour) |
| --- | --- |
| 1 | 14.1 \| 50,760 |
| 2 | 26.3 \| 94,680 |
| 3 | 53.8 \| 193,680 |

> Test done in iris mode.
