---
layout: default
title: Cookbooks
has_children: true
nav_order: 4
has_toc: false
---

The BQAT suite offers tools for assessing the quality of biometric data. It supports biometric modalities including fingerprints, face, iris, and voice. Developed by our experienced team, our tools are designed for flexibility, ease of use, and integration into existing projects.

## CLI Tool

For users preferring a scriptable interface, our Command Line Interface (CLI) tool offers easy to use entry point. It is ideal for integrating biometric analysis into automated workflows or for users who prefer terminal-based operations. 

### Highlights

* Full access to fingerprint, face, iris, and speech analysis modules
* Multi-core processing enabled
* Simple integration into existing scripts or workflows

## Web APIs

Our solutions can be integrated into existing projects using our RESTful API project. We also offer a stateless API for running the solution as a web service as part of your service mesh.

### RESTful API

A ready to run docker compose project that includes database, task queueing, file mangement, etc.

#### Highlights

* Easy integration with existing frontend application
* Self‑contained backend with task management
* Provide a series of supporting services

### Stateless API

Single docker container best for deploy as micro service.

#### Highlights

* Simple endpoint for single file processing
* Ready for scalable applications
* Provide provide base64 interface

## Web GUI

The web GUI provided is a reference frontend implementation for BQAT-API

### Highlights

* Ready to deploy
* Can be hosted on offline environment as well as cloud
