---
layout: default
title: Web GUI
parent: Cookbooks
nav_order: 4
---

<img alt="GitHub tag (latest by date)" src="https://img.shields.io/github/v/tag/biometix/bqat-gui">
<img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/biometix/bqat-gui">
<img alt="GitHub issues" src="https://img.shields.io/github/issues-raw/biometix/bqat-gui">
<img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/m/biometix/bqat-gui">
<img alt="GitHub" src="https://img.shields.io/github/license/biometix/bqat-gui">

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

---

## Setting Up

``` mermaid
---
config:
  theme: neutral
  layout: elk
---
graph TD
    download[Download the docker compose file] --> run(Spin up the container)
    run --> web{Visit localhost:9949}
    web --> raw[Raw data]
    web --> report[EDA report]
    web --> outlier[Outliers detected]

```

## Workflow

``` mermaid
---
config:
  theme: neutral
  layout: elk
---
graph LR
    input[Biometrics] --> upload(Upload data)
    subgraph bqat [BQAT Web GUI]
      upload --> process[Process biometric samples]
      process --> preview[Preview raw output]
    end
    preview --> raw(Download raw output as CSV)
    preview --> outlier(Identify potential outliers)
    preview --> report(Genrate EDA report from the data)

```

> BQAT-GUI could also distrubuted as a desktop application, reach out to us for further detail.

## User Interface

### Home

This is the landing page, with a brief introduction to the BQAT workflow.

![Screenshot](../assets/images/screenshot_web_intro.png)

### Data Input

Import/select input data and submit analysis task.

![Screenshot](../assets/images/screenshot_web_input_select.png)

1. Local files

   - The user could import dataset as zip file to the server.

   - Or may transfer the data to the data folder on the machine (if you run it on your local machine or have access to the machine).

2. Remote files

   - The user could also upload files from the browser directely (limited number possible), and the data won't be saved on the server once processed.

---

You may filter the input files by filename or type.

![Screenshot](../assets/images/screenshot_web_input_filter.png)

---

You may convert/rescale the input files if needed.

![Screenshot](../assets/images/screenshot_web_input_preprocessing.png)

---

Select dataset modality and processing engine(s).

![Screenshot](../assets/images/screenshot_web_input_engine.png)

### Task Management

Monitor status of ongoing task. You can stop/resume or cancel the task.

![Screenshot](../assets/images/screenshot_web_task.png)

---

Preview/download output data.

![Screenshot](../assets/images/screenshot_web_task_output.png)

---

Identify potential outliers using output data.

![Screenshot](../assets/images/screenshot_web_task_outlier.png)

---

Generate EDA report using output data.

![Screenshot](../assets/images/screenshot_web_task_report.png)

### Analysis Results

You may view/download the EDA report in this page. You can also share the report via the QR code.

![Screenshot](../assets/images/screenshot_web_results.png)

### Data Management

Instead of import/upload the dataset from input tab, you may upload the dataset via this tab beforehand (and delete if you like). 

![Screenshot](../assets/images/screenshot_web_files.png)

---

You can inspect the data as well (WSQ fingerprint files supported).

![Screenshot](../assets/images/screenshot_web_viewer.png)

---

## Output

### Raw Data

![Screenshot](../assets/images/screenshot_raw.png)

---

### EDA Report

![Screenshot](../assets/images/screenshot_report.png)

---

### Outlier Detection

![Screenshot](../assets/images/screenshot_outlier.png)


# BQAT-GUI lite

This version is a simple example web interface, which expose only the main biometic processing function.

> Note: Not suitable for large dataset processing due to browser limitation.

## Setting Up

``` mermaid
---
config:
  theme: neutral
  layout: elk
---
graph TD
    download[Download the docker compose file] --> run(Spin up the container)
    run --> web{Visit localhost:7860}
    web --> output[Output exported as CSV]

```

---

## Workflow

``` mermaid
---
config:
  theme: neutral
  layout: elk
---
graph LR
    input[Biometrics] --> submit(Submit task)
    subgraph BQAT Web GUI
    submit --> check[Check task status]
    check --> retrieve(Retrieve raw output when finished)
    end
    retrieve --> export(Download output as CSV)

```

## User Interface

![Screenshot](../assets/images/screenshot_web_lite.png)

---

## Output

The output can be downloaded as CSV.

![Screenshot](../assets/images/GUI-output.png)