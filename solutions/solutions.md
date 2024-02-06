---
layout: default
title: Solutions
has_children: true
nav_order: 4
has_toc: false
---

The BQAT biometric analysis suite offers comprehensive tools for assessing the quality and performance of biometric data across multiple modalities, including fingerprints, facial recognition, iris recognition, and speech analysis. Developed by a team with over 15 years of experience in biometric consulting, our tools are designed for flexibility, ease of use, and integration into existing projects.

## Web GUI
The BQAT Web-based Graphical User Interface (GUI) provides an intuitive platform for users to easily upload and analyze biometric samples. It offers a user-friendly way to interact with analysis modules, providing immediate visual feedback and results.

### Features:
Real-time quality assessments
Comprehensive metrics for each biometric modality
Outlier identification with visual cues

## Command Line Tool
For users preferring a scriptable interface, our Command Line Interface (CLI) tool offers full access to all functionalities. It is ideal for integrating biometric analysis into automated workflows or for users who prefer terminal-based operations.

### Features:
Full access to fingerprint, face, iris, and speech analysis modules
Batch processing capabilities
Simple integration into existing scripts or workflows

## Integrated into Existing Projects
Our solutions can be seamlessly integrated into existing projects through our RESTful API, offering a stateless interface for easy incorporation into web services, applications, and other systems.

#### RESTful API Features:

Easy integration with existing systems
Stateless operations ensuring scalability and performance
Support for all analysis modules via HTTP requests

#### Stateless API:
Designed for high-volume, scalable applications
Ensures consistent performance without server-side session management

## Requirements

Please note that only the following file extensions (file types) are supported:

* `.jpeg`
* `.jpg`
* `.bmp`
* `.png`
* `.jp2`
* `.wsq` (fingerprint only)

> Note: For fingerprint samples, by default, all input types will be converted to `.png`.

> Note: For iris samples, if the resolution of the input is higher than 640 by 480, it will be resized.