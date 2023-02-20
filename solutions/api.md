---
layout: default
title: RESTful API
parent: Solutions
nav_order: 2
---

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

## Endpoints
{: .no_toc .text-delta }

---

### POST /scan/

Create scan task from images under local `data/` folder.

---

### POST /scan/uploaded

Create scan task from images uploaded via the endpoint.

---

### GET /scan/{dataset_id}/profiles

Retrieve all scan results (image profiles) of this dataset.

---

### GET /scan/{dataset_id}/outliers

Retrieve outliers of this dataset.

---

### GET /scan/{dataset_id}/report

Get assesment report of this dataset.

---

> Note: Refer to `localhost:8848/docs` for full list of endpoints.
