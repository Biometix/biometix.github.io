---
layout: default
title: Commmand Line Tool
parent: Solutions
nav_order: 1
---

## Use Cases

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

# Run with the output filtered by specified query
./run.sh --input data/input/ --mode finger --attributes NFIQ2 --query "NFIQ2>20"

# Filter existing output CSV file with specified query
./run.sh --mode filter --output data/output.csv --query "NFIQ2>20"

# Filter existing output CSV file with query on specified attributes (columns)
./run.sh --mode filter --output data/output.csv --attributes NFIQ2 --query "NFIQ2>20"
```

## Option Flags

Short | Long            | Description
----- | --------------- | -----------
`-M`  | `--mode`        | (REQUIRED)  Specify analysis mode (fingerprint, face, iris, filter)
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
`-D`  | `--attributes`  | (OPTIONAL)  Specify attributes (columns) to investigate
`-Q`  | `--query`       | (OPTIONAL)  Queries to apply on the attributes
`-R`  | `--sort`  | (OPTIONAL)  Specify attributes (columns) to sort by
`-W`  | `--cwd`  | (OPTIONAL)  Specify current working directory for url in the report

## Log

The log file will keep record of information on the analysis process, including errors, warnings, and other metadata of the job.

## Benchmarking

The tool has a benchmark module to profile the host machine. It will go through a dataset of 1000 samples which consist of multiple formats and even corrupted files. The output also includes brief spec of the host machine. It can also be used to validate the setup.

``` sh
# Start benchmarking
./run.sh --mode face --benchmarking
```

## Alternative interface

``` sh
# Enter interactive CLI
./run.sh --interactive
```

## Build the image locally

``` sh
# Clone the repo
git clone https://github.com/Biometix/bqat-api.git

# Build the image
docker compose build
```

> Note: For powershell (windows) replace volumn mounted in the script as: `-v ${PWD}/data:/app/data`
