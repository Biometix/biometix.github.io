---
layout: default
title: Limitations
parent: Playbook
nav_order: 5
---

### Apple Silicon Compatibility

Some dependencies of BQAT might not fully compatibale with Macintosh machine with Apple chips (M1, M2, M2 Pro, etc.) yet. But it might work in certain cases, you could have a try.

### Memory

For large dataset on Linux, in the runtime, when the memory is exhausted, the kernel will try to reclaim some memory, which could freeze the system if critical system process was killed. This may not affect the final output because the docker runtime are still alive. This will not happen on MacOS or windows. Try to limit the memory or cpu available to Docker runtime or increase physical memory. Modify `--cpus` or `--memory` flags in `run.sh` or in the vanilla docker command.

### Iris Sample Resizing

The size/resolution of the iris image will be resized if it is higher than 640 by 480.

### Throughput

> Ubuntu 23.10, AMD Ryzen™ 5 5600G with Radeon™ Graphics × 12, 16.0 GiB

+ Face: 45 it/s
+ Iris: 20 it/s
+ Fingerprint: 10 it/s

The performance can be affected by other peocesses in the system.
