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

---
## Workflow

{: .highlight }
> Todo: text explanation and diagrams

## Endpoints
{: .no_toc }

> Note: Refer to `localhost:8848/docs` for full list of endpoints.

<!-- ## Workflow

1. Create a scan task with your input dataset (__POST /scan/__), the dataset could come from local `data/` folder or upload via the HTTP request.
2. Note the task id (`tid`) from the response, and check the status of this task (__GET /task/{task id}/__).
3. Retrieve the results using dataset id (`collection` id from response above) from the server (__GET /scan/{dataset id}/profiles__). -->

## Integration

There are full suit of endpoint to support the workflow, you can call them from upstream process as needed.

For instance, you may use the task management endpoints to control the task queue in the back but you don't have to use them.

The codebase in this repo did not include proper configuration for production environment, you may want to set up your proxy server, domain, web server workers, etc.

---
> {: .new-title }
>
> ### POST /scan/
> Create scan task from images under local `data/` folder.

---
> {: .new-title }
>
> ### POST /scan/uploaded
> Create scan task from images uploaded via the endpoint.

---

> {: .new-title }
>
> ### GET /scan/{dataset_id}/profiles
> Retrieve all scan results (image profiles) of this dataset.

---

> {: .new-title }
>
> ### GET /scan/{dataset_id}/outliers
> Retrieve outliers of this dataset.

---

> {: .new-title }
>
> ### GET /scan/{dataset_id}/report
> Get assesment report of this dataset.

---

## Output

{: .highlight }
> Todo: report explanation and screenshots