---
layout: default
title: BQAT CLI
parent: Getting Started
nav_order: 1
---

# BQAT CLI

---
<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

---

<a name="setup">
## Setup

This tool is designed to be run as Docker container via command line interface (terminal). For ease of use, convenience script is provided to help you.

### Get the script

> [Bash](https://raw.githubusercontent.com/Biometix/bqat-cli/main/run.sh){: .btn }

> [Powershell](https://raw.githubusercontent.com/Biometix/bqat-cli/main/run.ps1){: .btn }

<a name="usage">
## Usage

+ Download the script above into your working directory.
+ Create a folder named `data` under your working directory and put your input files in this folder.

After you finish the aforementioned steps, you should have a folder like this:

![Screenshot](../assets/images/working-directory.png)

+ Open your CLI and navigate to this directory.
+ Enter the command below to run BQAT.

For Bash (Linux, macOS, Windows):

``` sh
# Grant execution permission to the script (only for Linux shell script)
sudo chmod +x *.sh

# For example:
# Process all face images in data/ folder
./run.sh --input data/ --mode face

# Process iris images in data/iris/ folder
./run.sh --input data/iris/ --mode iris
```

> Note: You may need to modify the path format of mounted volumns in the `run.sh` for specific shell (e.g. under Windows. Or you can use the powershell script as follows).

For PowerShell (Winodws, Linux):

``` sh
# Process all face images in data/ folder
.\run.ps1 --input data/ --mode face

# Process iris images in data/iris/ folder
.\run.ps1 --input data/iris/ --mode iris
```

<a name="output">
## Output

The outputs will be saved at: `data/output/`.

## Further details about the command and other option flags
+ [Command Line Interface Playbook](https://biometix.github.io/playbook/cli.html)

> Note: The tool is designed to be executed with a `/data` folder in your working directory. The `/data` folder (where all the images are stored) will be mounted to the container. Read and write permission is required for this folder. You should be fine as long as you created the folder before spinning up the server. Otherwise you need to change the ownership of the folder.