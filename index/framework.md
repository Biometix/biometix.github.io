---
layout: default
title: Framework
nav_order: 5
permalink: /framework/
---

# BQAT Framework

 BQAT (Biometric Quality Assessment Tool) framework consist of the [core](https://github.com/Biometix/bqat-core) algorthm component, a [command line user interface](https://github.com/Biometix/bqat-cli), [convenience web page for the API](https://github.com/Biometix/bqat-gui) and [web API](https://github.com/Biometix/bqat-api).

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


## BQAT Core

Core component of BQAT that implemented as a Python package which links vendor algorithms togather, including Face, Fingerprint, Iris modules.

It will process the input biometric samples using corresponding modality engine selected and spit out the quality assessment metrics as Python dict.

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

## Interfaces

The different interface wrappers take care of the image loadings and then send them to the core component for processing. When the task is done, load the raw outputs and save them in respective formats.

***

``` mermaid
---
title: BQAT CLI
---
graph LR
    input(Input Folder) --> cli{Command Line}
    cli{Command Line} --> report(Report)
    cli{Command Line} --> output(CSV)
    cli{Command Line} --> log(Log)
```

> BQAT CLI takes a folder in your file system as input and spit out the raw output in CSV along with a brief statistic report.

***

``` mermaid
---
title: BQAT API
---
graph LR
    file(File System) --> api{Endpoints}
    upload(HTTP) --> api{Endpoints}
    api{Endpoints} --> db[(Database)]
    db[(Database)] --> report(Report)
    db[(Database)] --> output(JSON)
    db[(Database)] --> log(Log)
```

> BQAT API adds task management and storage on top of basic BQAT functionalities. It handles inputs in bulk as separate tasks, and save the output into backend database which can be accessed via restful API. I was designed to work as a backend container.

***

``` mermaid
---
title: BQAT Stateless
---
graph LR
    upload(HTTP) --> api{Endpoints}
    api{Endpoints} --> output(JSON Response)
```

> BQAT Stateless is a simplify version of BQAT API. Getting rid of the task management and storage, it will return the raw output as standard JSON response. It handles biometric samples one by one, either in raw file or base64 string.

***

``` mermaid
---
title: BQAT GUI
---
graph LR
    upload(Upload) --> gui{Web}
    gui{Web GUI} --> api(BQAT-API)
    api(Backend) --> db[(Database)]
    db[(Database)] --> report(Quality Report)
    db[(Database)] --> output(Raw CSV)
    db[(Database)] --> outlier(Outlier Report)
```

> BQAT GUI is a simple frontend for BQAT API as a example project.
