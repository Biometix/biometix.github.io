---
layout: default
title: BQAT CLI
parent: Getting Started
nav_order: 1
---

# BQAT CLI

<img alt="GitHub tag (latest by date)" src="https://img.shields.io/github/v/tag/biometix/bqat-cli">

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

{: .highlight }
> 🚀 Introducing the new BQAT entry point! It is a python based CLI interface to replace the legacy scripts.


## Setup

Prerequisites:
- [Docker](https://www.docker.com/)
- Python

> You may use the legacy shell script which does not require Python.

### Download BQAT CLI
{: .no_toc }

#### Python wheel

[Download](https://github.com/Biometix/bqat-cli/releases/download/v1.7.1-beta/bqat-1.7.1-py3-none-any.whl){: .btn }

```sh
pip install bqat-*-py3-none-any.whl
```

#### Install from source

```sh
pip install git+https://github.com/Biometix/bqat-cli.git#subdirectory=cli
```

#### Pre-built executable

[Download](https://github.com/Biometix/bqat-cli/releases/download/v1.7.1-beta/bqat){: .btn }

``` sh
# Grant execution permission to the EXE
sudo chmod +x bqat
```

<a name="usage">
## Usage

+ Check if the installation is successful.

  ```sh
  bqat --verison
  ```

+ (Optional) Run a benchmark test against your system.

  ```sh
  bqat -B
  ```

+ Create a folder named `data` under your working directory and put your input files in this folder.

  ```sh
  mkdir data
  ```
  
+ Enter the command below to run BQAT.

Examples:

``` sh
# Process all face images in 'data/' folder
bqat --input data/ --mode face

# Process iris images in 'data/iris/' folder
bqat --input data/iris/ --mode iris
```

> Note: If there is any space along the filepath, wrap it with double quotes and escape the space.<br> Please refer to the example below: 
e.g. input folder is `data/iris folder/`
```sh
bqat --input "data/iris\ folder/" --mode iris
```


Get BQAT-CLI Update if available:

``` sh
bqat --update
```

<a name="uninstall">
## Uninstall

```sh
bqat --uninstall
```


---

<a name="legacy">
## Legacy CLI

## Setup

This tool is designed to be run as a Docker container via command line interface (terminal). For ease of use, a convenience script is provided. 

### Download the script
{: .no_toc }

#### Linux
{: .no_toc }

[Bash](https://raw.githubusercontent.com/Biometix/bqat-cli/main/run.sh){: .btn }

#### Windows
{: .no_toc }

[Powershell](https://raw.githubusercontent.com/Biometix/bqat-cli/main/run.ps1){: .btn }

## Usage
{: .no_toc }

+ Download the script above into your working directory.
+ Create a folder named `data` under your working directory and put your input files in this folder.

After the aforementioned steps, you should have a folder like this:

![Screenshot](../assets/images/working-directory.png)

``` sh
# Grant execution permission to the script (for Linux shell script)
sudo chmod +x run.sh
```

+ Open your CLI and navigate to this directory.
+ Enter the command below to run BQAT.

For Bash (Linux, macOS):

``` sh
# Process all face images in 'data/' folder
./run.sh --input data/ --mode face

# Process iris images in 'data/iris/' folder
./run.sh --input data/iris/ --mode iris
```

> Note: If there is any space along the filepath, wrap it with double quotes and escape the space.<br> Please refer to the example below: 
e.g. input folder is `data/iris folder/`
```sh
./run.sh --input "data/iris\ folder/" --mode iris
```

> Note: The path format of the mounted volumes in the run.sh may need modification for the specific shell (e.g. under Windows. Or you can use the powershell script as follows). 

For PowerShell (Windows):

``` ps
# Process all face images in 'data/' folder
.\run.ps1 --input data/ --mode face

# Process iris images in 'data/iris/' folder
.\run.ps1 --input data/iris/ --mode iris
```

Get BQAT-CLI Update if available:

``` sh
# Linux
./run.sh --update
```

``` ps
# Windows
.\run.ps1 --update
```

## Output
{: .no_toc }

The outputs will be saved at: `data/output/`.

## Further details about the command and other option flags
{: .no_toc }
+ [Command Line Interface Playbook](https://biometix.github.io/playbook/cli.html)

> Note: The tool is designed to be executed with a `/data` folder in your working directory. The `/data` folder (where all the images are stored) will be mounted to the container. "Read and write” permission is required for this folder. It should work as long as the folder was created before spinning up the server. Otherwise, the ownership of the folder will need to be changed. 