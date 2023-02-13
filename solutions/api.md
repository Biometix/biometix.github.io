---
layout: default
title: RESTful API
parent: Solutions
nav_order: 2
---

# Endpoints
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## POST /scan/

__Description__

Add new scan tasks

__Parameters__

+ face
+ iris
+ fingerprint

__Body__

```json
{
  "options": {
    "engine": "default"
  },
  "input": [
    "data/20301003_1.jpg",
    "data/20315024_1.jpg",
    "data/17349955_1.jpg"
  ]
}
```

```json
{
  "input": "data/",
  "collection": "2e7f31ef-cba8-4365-856e-38b0621a6041"
}
```

---

## POST /scan/uploaded

__Description__

Add new scan tasks from uploaded file

__Parameters__

+ face
+ iris
+ fingerprint

---

## GET /scan/logs

__Description__

Retrieved all scan logs 

---

## GET /scan/{dataset_id}/profiles

__Description__

Retrieved all results in this task 

__Parameters__

+ UUID of the dataset

---

> Note: Refer to `/docs` for full list of endpoints