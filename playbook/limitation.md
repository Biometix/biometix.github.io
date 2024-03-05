---
layout: default
title: Limitations
parent: Playbook
nav_order: 5
---

### Apple Silicon Compatibility

Some dependencies of BQAT might not be fully compatible with Macintosh machines with Apple chips (M1, M2, M2 Pro, etc.) yet. It might work in certain cases, so it merits trying.  

### Memory

For a large dataset on Linux, in the runtime, when the memory is exhausted, the kernel will try to reclaim some memory; this could freeze the system if the critical system process was killed. This may not affect the final output because the Docker runtime are still alive. This will not happen on MacOS or Windows. Try to limit the memory or CPU available to Docker runtime or increase physical memory. Modify `--cpus` or `--memory` flags in `run.sh` or in the vanilla Docker command.

### Iris Sample Resizing

The size/resolution of the iris image will be resized if it is higher than 640 by 480. 

### Throughput

> Ubuntu 23.10, AMD Ryzen™ 5 5600G with Radeon™ Graphics × 12, 16.0 GiB

+ Face: 45 it/s
+ Iris: 20 it/s
+ Fingerprint: 10 it/s

The performance can be affected by other processes in the system.
