---
layout: default
title: Stateless API
parent: Solutions
nav_order: 3
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
## Workflow

``` mermaid

---
title: BQAT Stateless API
---

graph TD
    download([Download the docker image]) --> data(Creat data/path to your data/ folder)
    data(Creat data/path to your data/ folder) --> run((Run the docker))
    run((Run the docker)) --> endpoints{Call the endpoints}
    endpoints{Call the endpoints} --> output[[Get your output]]
    output[[Get your output]] --> json[Raw JSON Data]


```

## Endpoints
{: .no_toc }

> Note: Refer to `localhost:8848/docs` for full list of endpoints.

---

> {: .new-title }
>
> ### POST /file
> Upload a biometric file for quality assessment:
>
> - **file**: biometric file
> - **modality**: specify modality of the biometric

---

> {: .new-title }
>
> ### POST /base64
> Upload a biometric file (base64) for quality assessment:
>
> - **modality**: specify modality of the biometric.
> - **type**: biometric file type (png, jpg, wav, jp2, etc.).
> - **data**: biometric file encoded as base64 string.
> - **id**: biometric file identifier.
> - **timestamp**: ISO 8601 date and time format.

---


## Output

<!-- TODO: report screenshots-->