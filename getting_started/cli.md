---
layout: default
title: BQAT CLI
parent: Getting Started
nav_order: 1
---

# BQAT CLI

[![GitHub Tag](https://img.shields.io/github/v/tag/biometix/bqat-cli)](https://github.com/Biometix/bqat-cli/releases)
[![PyPI - Version](https://img.shields.io/pypi/v/bqat)](https://pypi.python.org/pypi/bqat)
[![PyPI - Downloads](https://img.shields.io/pypi/dm/bqat)](https://pypi.python.org/pypi/bqat)

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
> 🚀 Introducing the new [BQAT-CLI](https://pypi.org/project/bqat/) entry point! Now it is a pure python interface to replace the legacy scripts.

{: .highlight }
> 🌟 BQAT-CLI has been upgraded and now supports ARM-based CPUs! Whether you're on an Apple M‑series or a Qualcomm Snapdragon X‑series processor, you can leverage its performance for biometric data analysis.


## Setup

Prerequisites:
- [Docker](https://www.docker.com/)
- Python (3.10+)
- AMD64 or ARM64 CPUs with minimum of 8 GB RAM

### Install BQAT CLI
{: .no_toc }

#### Python application

```sh
pip install bqat
```

[PyPI](https://pypi.org/project/bqat/){: .btn }


<a name="usage">
## Usage

To validate the installation, you could start a benchmark run.

```sh
bqat --benchmark
```

Example use cases for biometric quality assessment:

``` sh
# Process all face images in 'data/'
bqat --input data --mode face

# Process iris images in 'data/iris/'
bqat --input data/iris --mode iris

# Process all face images using OFIQ engine
bqat --input data --mode face --engine OFIQ

# Enable EDA report for the assessment
bqat --input data/fingerprint --mode fingerprint --report
```

Check current installed version:

```sh
bqat --verison
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

<a name="output">
## Output

When the task completed, it will produce the quality metrics in a CSV file, a EDA report if enabled.

## Further details about the command and advanced option flags
{: .no_toc }
+ [Command Line Interface Cookbook](https://biometix.github.io/cookbook/cli.html)
