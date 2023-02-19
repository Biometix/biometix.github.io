---
layout: default
title: Limitations
parent: Solutions
nav_order: 4
---

## Limitations

Please note that only the following file extensions (file types) are supported:

* `.jpeg`
* `.jpg`
* `.bmp`
* `.png`
* `.jp2`
* `.wsq` (fingerprint only)

> Note: For fingerprint samples, by default, all input types will be converted to `.png`.

> Note: For iris samples, if the resolution of the input is higher than 640 by 480, it will be resized.

## Known Issues

## BQAT CLI

For large dataset on Linux, in the runtime, when the memory is exhausted, the kernel will try to reclaim some memory, which could freeze the system if critical system process was killed. This may not affect the final output because the docker runtime are still alive. This will not happen on MacOS or windows. Try to limit the memory or cpu available to Docker runtime or increase physical memory. Modify `--cpus` or `--memory` flags in `run.sh` or in the vanilla docker command.

## Apple Silicon Compatibility

At the moment, the Apple silicon platform is not fully compatible with BQAT. For this reason, users with Apple chips (M1, M2, M2 Pro, etc...) will not be able to perform biometric sample analysis with BQAT.
