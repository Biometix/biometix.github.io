---
layout: default
title: BQAT CLI
parent: Getting Started
nav_order: 1
---

# BQAT CLI

## Setup

This tool is designed to be run as Docker container. You can simply pull the Docker image and start it with the script provided.

### Get run script

> [Bash](https://raw.githubusercontent.com/Biometix/bqat-cli/main/run.sh){: .btn }

> [Powershell](https://raw.githubusercontent.com/Biometix/bqat-cli/main/run.ps1){: .btn }

## Usage

Create a folder named `data` under your working directory and put your input images in this folder.

> Note: The tool is designed to be executed with a `/data` folder in your working directory. The `/data` folder (where all the images are stored) will be mounted to the container. Read and write permission is required for this folder. You should be fine as long as you created the folder before spinning up the server. Otherwise you need to change the ownership of the folder.

Put the run script above under the working directory, then just run the script provided (You might need to give it execution permission).

### Quick start!

For bash (Linux, macOS, Windows):

``` sh
# Process samples in /input under /data with iris mode
./run.sh --input data/input/ --mode iris
```

``` sh
# Process all samples in /data with face mode
./run.sh --input data --mode face
```

> Note: You may need to modify the path format of mounted volumns in the `run.sh` for specific shell (e.g. Windows, or you can use the powershell script).

For powershell (Winodws, Linux):

``` sh
# Process samples in /input under /data with iris mode
.\run.ps1 --input data/input/ --mode iris
```

``` sh
# Process all samples in /data with face mode
.\run.ps1 --input data --mode face
```

> [More](https://biometix.github.io/solutions/cli.html) about optional flags.

## Output

The default output location is: `data/output/`.
