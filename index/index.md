---
layout: default
title: Home
nav_order: 1
permalink: /
---

# __Biometric Quality Assessment Tool (BQAT)__

## Overview

BQAT is a biometric quality assessment tool for generating and analysing given biometric samples’ quality to international standards as well as to customized metrics. The BQAT tool functions by taking an input directory of biometric data and will produce both the raw quality information as well as an analysis report.

The quality of biometric samples is a key aspect of the performance and usefulness of a biometric systems. Whilst there are a variety of tools per modality, this project is aimed to provide an open source framework to support all common modalities and allow for expansion as new methods are developed.

## Modality

+ __Fingerprint__

    The analysis of fingerprint engine based on NIST/NFIQ2 quality features. The quality score links image quality of optical and ink 500 PPI fingerprints to operational recognition performance.

+ __Face__

    The face image assessment provides metrics includes head pose, smile detection, inter-eye-distance, closed eyes, etc.

+ __Iris__

    The face image assessment provides various quality attributes, features, and ISO metrics.

+ __Speech__

    The speech assessment provides various quality metrics, including naturalness, coloration, noisiness, etc.

### Examples of biometric data quality variation

#### _Fingerprint_

![finger_example](../assets/images/finger_example.png)

#### _Iris_

![iris_example](../assets/images/iris_example.png)

#### _Face_

![face_example](../assets/images/face_example.png)

### Key features of the project

+ A variety of different methods of access including via CLI, GUI and as a server
+ Simple installation via docker
+ Outlier identification
+ Built by an experienced (>15 years) biometric consulting team
+ An active open source community

### Supporting libraries include

+ [NFIQ2](https://github.com/usnistgov/NFIQ2)
+ [BIQT](https://github.com/mitre/biqt)
+ [MediaPipe](https://github.com/google/mediapipe)
+ [NISQA](https://github.com/gabrielmittag/NISQA)

## Variation of the Tool

BQAT is available in multiple form factors:

+ __[CLI](https://github.com/Biometix/bqat-cli)__

    <img alt="GitHub tag (latest by date)" src="https://img.shields.io/github/v/tag/biometix/bqat-cli">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/biometix/bqat-cli">
    <img alt="GitHub issues" src="https://img.shields.io/github/issues-raw/biometix/bqat-cli">
    <img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/m/biometix/bqat-cli">
    <img alt="GitHub" src="https://img.shields.io/github/license/biometix/bqat-cli">
    [![Build Status](https://github.com/Biometix/bqat-cli/actions/workflows/build.yml/badge.svg)](https://github.com/Biometix/bqat-cli/actions/workflows/build.yml)
    [![Test Status](https://github.com/Biometix/bqat-cli/actions/workflows/test.yml/badge.svg)](https://github.com/Biometix/bqat-cli/actions/workflows/test.yml)
    [![Release Status](https://github.com/Biometix/bqat-cli/actions/workflows/release.yml/badge.svg)](https://github.com/Biometix/bqat-cli/actions/workflows/release.yml)
    [![Tests Status](https://github.com/Biometix/bqat-cli/blob/main/reports/junit/tests-badge.svg)](https://htmlpreview.github.io/?https://github.com/Biometix/bqat-cli/blob/main/reports/junit/report.html)
    [![Coverage Status](https://github.com/Biometix/bqat-cli/blob/main/reports/coverage/coverage-badge.svg)](https://htmlpreview.github.io/?https://github.com/Biometix/bqat-cli/blob/main/reports/coverage/index.html)

    BQAT that runs in a terminal. A CLI tool with Docker container backend.

+ __[API](https://github.com/Biometix/bqat-api)__

    <img alt="GitHub tag (latest by date)" src="https://img.shields.io/github/v/tag/biometix/bqat-api">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/biometix/bqat-api">
    <img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/biometix/bqat-api/github-actions.yml">
    <img alt="GitHub issues" src="https://img.shields.io/github/issues-raw/biometix/bqat-api">
    <img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/m/biometix/bqat-api">
    <img alt="GitHub" src="https://img.shields.io/github/license/biometix/bqat-api">

    BQAT functionalities provided via RESTful API. A server with BQAT core algorithm.

+ __[Stateless](https://github.com/Biometix/bqat-stateless)__

    <img alt="GitHub tag (latest by date)" src="https://img.shields.io/github/v/tag/biometix/bqat-stateless">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/biometix/bqat-stateless">
    <img alt="GitHub issues" src="https://img.shields.io/github/issues-raw/biometix/bqat-stateless">
    <img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/m/biometix/bqat-stateless">
    <img alt="GitHub" src="https://img.shields.io/github/license/biometix/bqat-stateless">
    [![Build Status](https://github.com/Biometix/bqat-stateless/actions/workflows/build.yml/badge.svg)](https://github.com/Biometix/bqat-stateless/actions/workflows/build.yml)
    [![Test Status](https://github.com/Biometix/bqat-stateless/actions/workflows/test.yml/badge.svg)](https://github.com/Biometix/bqat-stateless/actions/workflows/test.yml)
    [![Release Status](https://github.com/Biometix/bqat-stateless/actions/workflows/release.yml/badge.svg)](https://github.com/Biometix/bqat-stateless/actions/workflows/release.yml)
    [![Tests Status](https://github.com/Biometix/bqat-stateless/blob/main/reports/junit/tests-badge.svg)](https://htmlpreview.github.io/?https://github.com/Biometix/bqat-stateless/blob/main/reports/junit/report.html)
    [![Coverage Status](https://github.com/Biometix/bqat-stateless/blob/main/reports/coverage/coverage-badge.svg)](https://htmlpreview.github.io/?https://github.com/Biometix/bqat-stateless/blob/main/reports/coverage/index.html)

    Stateless version of BQAT API. No data was store on the server.

+ __GUI__

    BQAT as desktop application. _Coming soon._

{: .highlight }
Please contact us at info@biometix.com if you'd like more information.
