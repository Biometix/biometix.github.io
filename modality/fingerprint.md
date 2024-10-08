---
layout: default
title: Fingerprint
parent: Modalities
nav_order: 1

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

## Overview

The engine for the analysis of fingerprints is based on NIST/NFIQ2 quality features. The quality score links the image quality of optical and ink 500 PPI fingerprints to operational recognition performance. 

## Examples of Fingerprint quality variation

![finger_example](../assets/images/finger_example.png)

***

## Input

For fingerprints, the tool works with the image formats WSQ and PNG. For both of these formats, the image will be run directly through NFIQ2. Image formats other than WSQ and PNG are first converted into a compatible format before being run through NFIQ2. 

<!-- _Any biometric sample which was had preprocessing or conversion applied to it during the quality assessment process will be noted within the output log._ -->

NFIQ2 expects images to have a resolution of at least 500 PPI. The tool will force NFIQ2 to run on images of lower resolution, but the result may be inaccurate. 

***

## Output

BQAT will produce the quality scores generated by the engines as well as additional information in columns. It will be saved as CSV from CLI or JSON from API. 

***

__Fingerprint__:

| Column                              | Description |
| ----------------------------------- | ----------- |
| file                                | Filename of the sample, including the directory path |
| NFIQ2                               | NFIQ2 quality score |
| quantized                           | Input quantized or not |
| resampled                           | Input resampled or not |
| uniform_image                       | Standard deviation of gray levels in image indicates uniformity ([NFIQ2](https://pages.nist.gov/NFIQ2/docs/v2.1.0/namespace_n_f_i_q2_1_1_identifiers_1_1_actionable_quality_feedback.html)) |
| empty_image_or_contrast_too_low     | The image is blank or the contrast is too low ([NFIQ2](https://pages.nist.gov/NFIQ2/docs/v2.1.0/namespace_n_f_i_q2_1_1_identifiers_1_1_actionable_quality_feedback.html))
| fingerprint_image_with_minutiae     | Number of minutia in image ([NFIQ2](https://pages.nist.gov/NFIQ2/docs/v2.1.0/namespace_n_f_i_q2_1_1_identifiers_1_1_actionable_quality_feedback.html)) |
| sufficient_fingerprint_foreground   | Number of pixels in the computed foreground ([NFIQ2](https://pages.nist.gov/NFIQ2/docs/v2.1.0/namespace_n_f_i_q2_1_1_identifiers_1_1_actionable_quality_feedback.html)) |
| edge_std                            | Metric to identify malformed images |
| image_width                         | Width of the input in pixels |
| image_height                        | Height of the input in pixels |

> [NIST Interagency Report](https://nvlpubs.nist.gov/nistpubs/ir/2021/NIST.IR.8382.pdf)

