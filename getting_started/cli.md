---
layout: default
title: BQAT CLI
parent: Getting Started
nav_order: 1
---

# BQAT CLI

## Setup

This tool is designed to be run as Docker container. You can simply pull the Docker image and start it with the script provided.

### Get the Script

Script (run.sh):

[Download](https://github.com/Biometix/bqat-cli/blob/main/run.sh){: .btn }

### Pull the Docker Image from Registry

``` sh
# Pull the image
docker pull ghcr.io/biometix/bqat-cli:latest
```

### _Or_ Build the Image Locally

``` sh
# Clone the repo
git clone https://github.com/Biometix/bqat-cli.git

# Build the image
docker build -t ghcr.io/biometix/bqat-cli:latest .
```

## Usage

Create a folder named `data` under your working directory and put your input images in this folder.

> Note: The tool is designed to be executed with a `/data` folder in your working directory. The `/data` folder (where all the images are stored) will be mounted on the container. Read and write permission is required for this folder.

Then just run the script provided (You might need to give it execution permission).

> Note: You may need to modify the path format of mounted volumns in the `run.sh` for specific shell.

### Example

``` sh
# Process samples in /input under /data with iris mode
./run.sh --input data/input/ --mode iris

# Process all samples in /data with face mode
./run.sh --input data --mode face
```

## Output

The default output location is: `data/output/`.
