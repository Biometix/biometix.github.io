---
layout: default
title: Roadmap
parent: Solutions
nav_order: 5
---

## Roadmap

Our current development roadmap for future products part of the BQAT suite can be seen in the gantt chart below.

``` mermaid
gantt
    title BQAT Roadmap
    dateFormat  DD-MM
    axisFormat  %d-%m

    section BQAT-Stateless
    Initial Planning    : a1, 01-04, 3d
    Proof of Concept    : a2, after a1, 7d
    MVP                 : a3, after a2, 7d
    Quality Assurance   : a4, after a3, 7d
    Documentation       : after a3, 7d

    section BQAT GUI
    Initial Planning    : a1, 01-05, 3d
    Proof of Concept    : a2, after a1, 10d
    MVP                 : a3, after a2, 10d
    Quality Assurance   : a4, after a3, 10d
    Documentation       : after a3, 10d
```

Upcomming features:

+ Speech assessment module.
+ Pure Python entrypoint for BQAT CLI.
