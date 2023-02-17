---
layout: default
title: Home
nav_order: 1
---

# Biometric Quality Assessment Tool (BQAT)

## Overview

BQAT is a biometric quality assessment tool for generating and analysing given biometric samples’ quality to international standards as well as to customized metrics. The BQAT tool functions by taking an input directory of biometric data and will produce both the raw quality information as well as an analysis report.

+ __Fingerprint__

    The analysis of fingerprint engine based on NIST/NFIQ2 quality features. The quality score links image quality of optical and ink 500 PPI fingerprints to operational recognition performance.

+ __Face__

    The face image assessment provides metrics includes head pose, smile detection, inter-eye-distance, closed eyes, etc.

+ __Iris__

    The face image assessment provides various quality attributes, features, and ISO metrics.

## Importance

The quality of biometric samples is a key aspect of the performance and usefulness of a biometric systems. Whilst there are a variety of tools per modality, this project is aimed to provide an open source framework to support all common modalities and allow for expansion as new methods are developed. 

### Key features of the project:

- a variety of different methods of access including via CLI, GUI and as a server
- simple installation via docker
- outlier identification
- built by an experienced (>15 years) biometric consulting team
- an active open source community

### Supporting libraries include:

- [NFIQ2](https://github.com/usnistgov/NFIQ2),
- [BIQT](https://github.com/mitre/biqt), 
- [MediaPipe](https://github.com/google/mediapipe)

### Examples of biometric data quality variation:

Fingerprint
![finger_example](assets/images/finger_example.png)

Face
![face_example](assets/images/face_example.png)

Iris
![iris_example](assets/images/iris_example.png)

## Versions

BQAT is available in multiple form factors:

+ __[CLI](https://github.com/Biometix/bqat-cli)__

    BQAT that runs in a terminal. A CLI tool with Docker container backend.

+ __[API](https://github.com/Biometix/bqat-api)__

    BQAT functionalities provided via RESTful API. A server with BQAT core algorithm.

+ __GUI__

    BQAT as desktop application. _Coming soon._

> Please contact us at info@biometix.com if you'd like more information.