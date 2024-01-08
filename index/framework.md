---
layout: default
title: Framework
nav_order: 5
permalink: /framework/
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

{: .highlight }
> Todo: explanation

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

{: .highlight }
> Todo: explanation

***

``` mermaid
---
title: BQAT Stateless
---
graph LR
    upload(HTTP) --> api{Endpoints}
    api{Endpoints} --> output(JSON Response)
```

{: .highlight }
> Todo: explanation

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

{: .highlight }
> Todo: explanation
