---
layout: default
title: Stateless API
parent: Playbooks
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
## Setting Up

``` mermaid

graph TD
  download[Download the docker compose file] --> run(Spin up the container)
  run --> doc{localhost:8848/docs}

```

---

## Workflow

``` mermaid

graph LR
  A[Frontend] --> B([Biometrics])
  B --> C{BQAT Stateless API}
  C --> |Outputs| A

```

---

## Endpoints

---

### POST /file

Upload a biometric file for quality assessment:

- **file**: biometric file
- **modality**: specify modality of the biometric

---

### POST /base64

Upload a biometric file (base64) for quality assessment:

- **modality**: specify modality of the biometric.
- **type**: biometric file type (png, jpg, wav, jp2, etc.).
- **data**: biometric file encoded as base64 string.
- **id**: biometric file identifier.
- **timestamp**: ISO 8601 date and time format.

---

> Note: Refer to `localhost:8848/docs` for full list of endpoints.

<!-- 

## Response

![Screenshot](../assets/images/statelessapi.png) -->

## Response

JSON:

``` JSON
{
  "file": "12347.jpg",
  "image_height": 244,
  "image_width": 212,
  "confidence": 0.866117537021637,
  "bbox_left": 49,
  "bbox_upper": 74,
  "bbox_right": 183,
  "bbox_lower": 208,
  "smile": false,
  "eye_closed_left": false,
  "eye_closed_right": false,
  "ipd": 48,
  "pupil_right_x": 43,
  "pupil_right_y": 45,
  "pupil_left_x": 91,
  "pupil_left_y": 47,
  "yaw_pose": "Right",
  "yaw_degree": -24.930552093832574,
  "pitch_pose": "Down",
  "pitch_degree": -32.260817406476285,
  "roll_pose": "Level",
  "roll_degree": -0.4556886155332786,
  "glasses": true
}
```

## Scalability

Due to BQAT's compute-intensive nature, the server’s throughput is primarily limited by the CPU of the host machine, including factors such as the number of cores and single-thread performance.​
    
Scaling options:​

+ Vertical: deploy to a machine with larger CPU.​

+ Horizontal: deploy to a cluster of machines (e.g. Kubernetes, Docker Swarm, etc.)

### Example (Docker Swarm):

> This is for local small scale deployment, use Kubernetes for large scale production environment.

> This example is tested on Linux nodes only, further configuration might be needed for Windows and macOS.

#### Prepare worker nodes

+ Make sure you have all your worker machines/VMs installed with [Docker Engine](https://docs.docker.com/engine/);

+ Take note of their IP addresses.

#### Set up cluster

Select one machine as the manager, then open the terminal on this manager computer:

``` sh
docker swarm init --advertise-addr <MANAGER-IP>
```

Use the command printed from previous step to add worker nodes (looks like this). Run this command on all the worker nodes:

``` sh
docker swarm join --token kz5s954yi3oex3nedyz0fb0xx1 192.168.101.101:8008
```

After all your worker nodes joined, check if your cluster was set up properly:

``` sh
docker node ls
```

#### Deploy to cluster

Deploy BQAT-Stateless to the cluster:

``` sh
docker stack deploy --compose-file compose.yaml bqat-stateless
```

Check service status

``` sh
docker stack services bqat-stateless
```

Scale up the service using the worker nodes (4 replicas in this example):

``` sh
docker service scale bqat-stateless_server=4
```

> Congratulations! The cluster has been set up! 🎉 You can now make requests to the endpoints as you typically would! The loads will be distributed across the worker nodes.

> Note: bring up more replicas than number of the physical machines might not further increase the throughput.

#### Clean up

Bring down the service:

``` sh
docker stack rm bqat-stateless
```

Disconnect worker node (on the worker machine):

``` sh
docker swarm leave
```

Remove the node from the cluster (on manager machine):

``` sh
docker node rm <NODE-ID>
```

> Please refers to Docker [official documentation](https://docs.docker.com/engine/swarm/) for further details.