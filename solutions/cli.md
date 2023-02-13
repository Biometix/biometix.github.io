---
layout: default
title: Commmand Line Tool
parent: Solutions
nav_order: 1
---

# Use Cases

``` sh
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

# Run samples in /input with face mode, limit to 100k scan
./run.sh --input data/input/ --mode face --limit 100000
```

## Option Flags
Short | Long            | Description
----- | --------------- | -----------
`-M`  | `--mode`        | (REQUIRED)  Specify analysis mode (Fingerprint, Face, IRIS)
`-I`  | `--input`       | (REQUIRED)  Specify input directory
`-O`  | `--output`      | (OPTIONAL)  Specify output csv file or directory
`-B`  | `--benchmark`   | (OPTIONAL)  Run system benchmarking analysis
`-L`  | `--limit`       | (OPTIONAL)  Set a limit for number of files to scan
`-F`  | `--filename`    | (OPTIONAL)  Specify filename pattern for searching in the folder
`-S`  | `--search`      | (OPTIONAL)  Specify file types to search within the input folder
`-C`  | `--convert`     | (OPTIONAL)  Specify file types to convert before processing
`-T`  | `--target`      | (OPTIONAL)  Specify target type to convert to
`-A`  | `--arm`         | (OPTIONAL)  Disable multithreading (For ARM64 platform)
`-X`  | `--interactive` | (OPTIONAL)  Enter terminal interactive UI

## Log
The log file will keep record of information on the analysis process, including errors, warnings, and other metadata of the job.

# Validation & Benchmarking

The tool has a benchmark module to profile the host machine. It will go through a dataset of 1000 files which consist of multiple formats and even corrupted files. The output also includes brief spec of the host machine. It can also be used to validate the setup.

``` sh
# Start benchmarking
./run.sh --benchmarking
```

# Alternative interface
``` sh
# Enter interactive CLI
./run.sh --interactive
```

> Note: For powershell (windows) replace volumn mounted in the script as: `-v ${PWD}/data:/app/data`
