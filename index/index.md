---
layout: default
title: Introduction
nav_order: 1
permalink: /
---

# __Biometric Quality Assessment Tool (BQAT)__

## Overview

BQAT is a biometric quality assessment tool for generating and analysing biometric samples’ quality against international standards as well as customised metrics. BQAT functions by taking an input directory of biometric data and producing both the raw quality information as well as an analysis report. 

The quality of biometric samples is a key aspect of the performance and efficacy of a biometric system. Whilst there are a variety of tools suitable for each modality, this project is aimed to provide an open-source framework to support all common modalities and allow for expansion as new methods are developed. 

## Modality

+ [__Fingerprint__](https://biometix.github.io/modality/fingerprint.html)

    The engine for the analysis of fingerprints is based on NIST/NFIQ2 quality features. The quality score links the image quality of optical and ink 500 PPI fingerprints to operational recognition performance. 

+ [__Face__](https://biometix.github.io/modality/face.html)

    The face image assessment module provides metrics including head pose, smile detection, inter-eye distance, closed eyes, etc. 

+ [__Iris__](https://biometix.github.io/modality/iris.html)

    The iris sample assessment module provides various quality attributes, features, and ISO metrics.

+ [__Speech__](https://biometix.github.io/modality/speech.html)

    The speech assessment module provides various quality metrics, including naturalness, colouration, noisiness, etc. 

<!-- ### Examples of biometric data quality variation

#### _Fingerprint_

![finger_example](../assets/images/finger_example.png)

#### _Iris_

![iris_example](../assets/images/iris_example.png)

#### _Face_

![face_example](../assets/images/face_example.png) -->

### Key features of the project

+ A variety of different methods of access, including via CLI, web page and/or web API 
+ Simple installation via Docker 
+ Quality report
+ Built by an experienced biometric consulting team
+ An active open-source community

### Supporting libraries include

+ [NFIQ2](https://github.com/usnistgov/NFIQ2)
+ [BIQT](https://github.com/mitre/biqt)
+ [MediaPipe](https://github.com/google/mediapipe)
+ [NISQA](https://github.com/gabrielmittag/NISQA)

## Variation of the Toolbox

BQAT is available in multiple form factors:

+ __[CLI](https://github.com/Biometix/bqat-cli)__

    <img alt="GitHub tag (latest by date)" src="https://img.shields.io/github/v/tag/biometix/bqat-cli">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/biometix/bqat-cli">
    <img alt="GitHub issues" src="https://img.shields.io/github/issues-raw/biometix/bqat-cli">
    <img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/m/biometix/bqat-cli">
    <img alt="GitHub" src="https://img.shields.io/github/license/biometix/bqat-cli">

    BQAT in the terminal. A CLI tool for biometrics.

+ __[API](https://github.com/Biometix/bqat-api)__

    <img alt="GitHub tag (latest by date)" src="https://img.shields.io/github/v/tag/biometix/bqat-api">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/biometix/bqat-api">
    <img alt="GitHub issues" src="https://img.shields.io/github/issues-raw/biometix/bqat-api">
    <img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/m/biometix/bqat-api">
    <img alt="GitHub" src="https://img.shields.io/github/license/biometix/bqat-api">

    BQAT via RESTful API. A self-contained server solution.

+ __[Stateless](https://github.com/Biometix/bqat-stateless)__

    <img alt="GitHub tag (latest by date)" src="https://img.shields.io/github/v/tag/biometix/bqat-stateless">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/biometix/bqat-stateless">
    <img alt="GitHub issues" src="https://img.shields.io/github/issues-raw/biometix/bqat-stateless">
    <img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/m/biometix/bqat-stateless">
    <img alt="GitHub" src="https://img.shields.io/github/license/biometix/bqat-stateless">

    Stateless version of BQAT API. No data will be stored on the server, similar to a serverless function.

+ __[GUI](https://github.com/Biometix/bqat-gui)__

    <img alt="GitHub tag (latest by date)" src="https://img.shields.io/github/v/tag/biometix/bqat-gui">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/biometix/bqat-gui">
    <img alt="GitHub issues" src="https://img.shields.io/github/issues-raw/biometix/bqat-gui">
    <img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/m/biometix/bqat-gui">
    <img alt="GitHub" src="https://img.shields.io/github/license/biometix/bqat-gui">

    Simple Web GUI for BQAT API. An easy to use user interface to the services.

---

{: .highlight }
> Please contact us at info@biometix.com if you'd like more information.

