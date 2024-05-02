---
layout: default
title: Limitations
parent: Playbooks
nav_order: 5
---

### Apple Silicon Compatibility

Some dependencies of BQAT might not be fully compatible with Macintosh machines with Apple chips (M1, M2, M2 Pro, etc.) yet. It might work in certain cases, so it merits trying.  

### Memory leakage

When processing a large dataset on Linux, when the memory is exhausted, the kernel will try to reclaim some memory; this could freeze the system if the critical system process was killed. This may not affect the final output because the Docker runtime are still alive. This won't happen on macOS or Windows. You could try to limit the memory or CPU available to Docker runtime or increase physical memory. Modify `--cpus` or `--memory` flags in `run.sh` or in the vanilla Docker command.

### Iris Sample Resizing

The size/resolution of the iris image will be rescaled for processing if out of range. When resized, the quality score might deviate from original input. For certain edge cases, the processing engine may fail to generate output. [BIQT-Iris](https://github.com/mitre/biqt-iris)

### Throughput

> Ubuntu 23.10, AMD Ryzen™ 5 5600G with Radeon™ Graphics × 12, 16.0 GiB

+ Face: 45 it/s
+ Iris: 20 it/s
+ Fingerprint: 10 it/s

### NISQA (Speech)

This implementation is in alpha stage, progress bar is not functioning properly.

### OFIQ (Face)

This implementation is in alpha stage, progress bar is not functioning properly.
