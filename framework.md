---
layout: default
title: Framework Concept
nav_order: 4
---

# BQAT Framework

 BQAT (Biometric Quality Assessment Tool) consist of a [core](https://github.com/Biometix/bqat-core) algorthm component and a wapper user interface which can be a [command line UI](https://github.com/Biometix/bqat-cli), [graphic UI](https://github.com/Biometix/bqat-gui) or [web API](https://github.com/Biometix/bqat-api).

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

It will process the input image according to the mode selected and spit out the assessment metrics as Python dict.

``` mermaid
---
title: BQAT Core
---
graph LR
    input(Biometric samples) --> core{Core}
    core{Core Interface} --> face(Face)
    core{Core} --> finger(Fingerprint)
    core{Core} --> iris(Iris)
```

## BQAT Interfaces

The interface wrappers take care of the image loadings and then send them to the core component for processing. When the task is done, load the raw outputs and save them in respective formats.

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

***

``` mermaid
---
title: BQAT GUI
---
graph LR
    file(File System) --> gui{GUI}
    upload(Upload) --> gui{GUI}
    gui{GUI} --> db[(Database)]
    db[(Database)] --> report(Report)
    db[(Database)] --> output(JSON)
    db[(Database)] --> log(Log)
```


