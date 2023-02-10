---
layout: default
title: BQAT CLI
parent: Getting Started
nav_order: 1
---

## Installation

This tool is designed to be run as container.

### Pull the Docker Image from Registry

``` sh
# Pull the image
docker pull ghcr.io/biometix/bqat-cli:latest
```

### Build the Image

You can also build the image locally.

``` sh
# Build the image
docker build -t ghcr.io/biometix/bqat-cli:latest .
```

## Usage

The tool is designed to be executed on a directory of /data. You will need to mount the primary working directory (where all the images are stored) into the container. The default directory in the container for mounting the work directory is `/app/data`, this can be done using the `-v` option in Docker.

The tool does require additional shared memory and this can be set by using the `--shm-size` option in Docker. Generally setting this to 8G works well.

### Commands

The `run.sh` is a convenience script for running BQAT.

Example:
``` sh
# Run samples in /input with fingerprint mode as default
./run.sh --input data/input/

# Run benchmarking task
./run.sh --input data/input/ --benchmarking

# Run samples in /input with iris mode
./run.sh --input data/input/ --mode iris

# Search the file with name pattern in the input folder
./run.sh --input data/input/ --mode iris --filename "*FINGER*"

# Search the file with specific format in the input folder
./run.sh --input data/input/ --mode iris --search "jp2 pgm bmp"

# Convert the files with specific formats before scanning
./run.sh --input data/input/ --mode fingerprint --convert "jp2 jpeg"

# Specify the file format to convert to
./run.sh --input data/input/ --mode fingerprint --target wsq

# Run samples in /input with face mode, extension function enabled, limit to 100k scan
./run.sh --input data/input/ --mode face --extension --limit 100000
```

Alternate interface:
``` sh
# Enter interactive CLI
./run.sh --interactive
```

### Optional Flags
You can append optional flags as follows:
* -M, --mode         (REQUIRED)  Specify assessment mode (Fingerprint, Face, IRIS).
* -I, --input        (REQUIRED)  Specify input directory
* -O, --output       (OPTIONAL)  Specify output csv file or directory
* -B, --benchmark    (OPTIONAL)  Run system benchmarking analysis
* -L, --limit        (OPTIONAL)  Set a limit for number of files to scan
* -F, --filename     (OPTIONAL)  Specify filename pattern for searching in the folder
* -S, --search       (OPTIONAL)  Specify file types to search within the input folder
* -C, --convert      (OPTIONAL)  Specify file types to convert before processing
* -T, --target       (OPTIONAL)  Specify target type to convert to
* -E, --extension    (OPTIONAL)  Enable customized extension function
* -A, --arm          (OPTIONAL)  Disable multithreading (For ARM64 platform)
* -X, --interactive  (OPTIONAL)  Enter terminal interactive ui
* --help             Show a help message

If the output or log options are not specified then the tool will use a default value.

> For powershell (windows) replace this line
``` sh
-v ${PWD}/data:/app/data
```

### Log:
The log file will show some information on the process, including errors, warnings, and the total execution time of the job.

## Install validation & Benchmarking

The tool has a benchmark module to profile the host machine. It will go through a dataset of 1000 files which consist of multiple formats and even corrupted files. The output also includes simple spec of the host machine.

```sh
# Use run.sh
./run.sh --benchmarking
```
