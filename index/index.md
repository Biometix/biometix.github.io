---
layout: default
title: Introduction
nav_order: 1
permalink: /
---

_Latest News_

> [OFIQ](https://www.bsi.bund.de/SharedDocs/Downloads/EN/BSI/OFIQ/Overview_presentation_OFIQ.pdf?__blob=publicationFile&v=2) `v1.0.3` has been released and integrated in BQAT!

> Fingerprint processing engine upgraded to [NFIQ2](https://github.com/usnistgov/NFIQ2/releases/tag/v2.3.0) `v2.3.0`!

> 🚀 Introducing ARM-based CPU support for [BQAT-CLI](https://biometix.github.io/getting_started/cli.html)!

---

_Releases_

{: .highlight }
>  BQAT-CLI [v1.8.4](https://biometix.github.io/changelog/#bqat-cli) released! Join and share your ideas at [Discussions](https://github.com/Biometix/bqat-cli/discussions) 🎉

{: .highlight }
>  BQAT-API [v1.6.0](https://biometix.github.io/changelog/#bqat-api) released! Join and share your ideas at [Discussions](https://github.com/Biometix/bqat-api/discussions) 🎉

---

![logo_bqat](../assets/images/logo-bqat.png)

by [Biometix](https://www.biometix.com/)

<!-- # __Biometric Quality Assessment Tool (BQAT)__ -->

<!-- ``` mermaid
mindmap
  root((**BQAT**))
    BQAT-CLI
      EDA Report
      CSV
    BQAT-API
      Cloud
      Self-Hosted
    BQAT-GUI
      Web
      Lightweight
``` -->

---

## Overview

[BQAT](https://github.com/Biometix) (Biometric Quality Assessment Tool) is an open-source biometric quality assessment tool for generating and analyzing biometric samples’ quality against international standards as well as customized metrics. BQAT functions by taking an input directory of biometric data and producing raw quality information and an analysis report.

The quality of biometric samples is a key aspect of the performance and efficacy of a biometric system. Whilst there are a variety of tools suitable for each modality, this project is aimed to provide an open-source framework to support all common modalities and allow for expansion as new methods are developed. 

---

``` mermaid
---
config:
  theme: neutral
  layout: elk
---
    graph LR
        subgraph title [ ]
            core[BQAT-Core] --> face("`__Face__`")
            core --> finger("`__Fingerprint__`")
            core --> iris("`__Iris__`")
            core --> speech("`__Speech__`")
            finger --> nfiq([NFIQ2])
            iris --> biqt-iris([BIQT])
            face --> bqat([Biometix])
            face --> ofiq([OFIQ])
            face --> biqt-face([BIQT])
            speech --> nisqa([NISQA])
        end
            title --> cli(BQAT-CLI)
            title --> api(BQAT-API)
            title --> gui(BQAT-GUI)
            title --> stateless(BQAT-Stateless)
        click finger "https://biometix.github.io/modality/fingerprint.html" _blank
        click face "https://biometix.github.io/modality/face.html" _blank
        click iris "https://biometix.github.io/modality/iris.html" _blank
        click speech "https://biometix.github.io/modality/speech.html" _blank
        click cli "https://github.com/Biometix/bqat-cli" _blank
        click api "https://github.com/Biometix/bqat-api" _blank
        click gui "https://github.com/Biometix/bqat-gui" _blank
        click stateless "https://github.com/Biometix/bqat-stateless" _blank
        click nfiq "https://github.com/usnistgov/NFIQ2" _blank
        click biqt-face "https://github.com/mitre/biqt-face" _blank
        click biqt-iris "https://github.com/mitre/biqt-iris" _blank
        click bqat "https://github.com/Biometix" _blank
        click ofiq "https://www.bsi.bund.de/EN/Themen/Unternehmen-und-Organisationen/Informationen-und-Empfehlungen/Freie-Software/OFIQ/OFIQ_node.html" _blank
        click nisqa "https://github.com/gabrielmittag/NISQA" _blank
```

---

## Modalities

+ [__Fingerprint__](https://biometix.github.io/modality/fingerprint.html)

    The engine for the analysis of fingerprints is based on NIST/NFIQ2 quality features. The quality score links the image quality of optical and ink 500 PPI fingerprints to operational recognition performance. 

+ [__Face__](https://biometix.github.io/modality/face.html)

    The face image assessment module provides metrics including head pose, smile detection, inter-eye distance, closed eyes, etc. 

+ [__Iris__](https://biometix.github.io/modality/iris.html)

    The iris sample assessment module provides various quality attributes, features, and ISO metrics.

+ [__Speech__](https://biometix.github.io/modality/speech.html)

    The speech assessment module provides various quality metrics, including naturalness, colouration, noisiness, etc. 

### Key features of the project

+ Biometrics quality assessment platform for different modalities and processing engines
+ A variety of different methods of access, including via CLI, web page and/or web API 
+ Simple installation via Docker 
+ Quality report
+ Built by an experienced biometric consulting team
+ An active open-source community

### Supporting libraries

+ [NFIQ2](https://github.com/usnistgov/NFIQ2)
+ [OFIQ](https://www.bsi.bund.de/EN/Themen/Unternehmen-und-Organisationen/Informationen-und-Empfehlungen/Freie-Software/OFIQ/OFIQ_node.html)
+ [BIQT](https://github.com/mitre/biqt)
+ [MediaPipe](https://github.com/google/mediapipe)
+ [NISQA](https://github.com/gabrielmittag/NISQA)

## Variation of the Toolbox

BQAT is available in multiple form factors:

+ __[CLI](https://github.com/Biometix/bqat-cli)__

    <img alt="GitHub tag (latest by date)" src="https://img.shields.io/github/v/tag/biometix/bqat-cli">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/biometix/bqat-cli">
    <img alt="GitHub issues" src="https://img.shields.io/github/issues-raw/biometix/bqat-cli">
    <img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/m/biometix/bqat-cli">
    <img alt="GitHub" src="https://img.shields.io/github/license/biometix/bqat-cli">

    [![PyPI - Version](https://img.shields.io/pypi/v/bqat)](https://pypi.python.org/pypi/bqat)
    [![PyPI - Downloads](https://img.shields.io/pypi/dm/bqat)](https://pypi.python.org/pypi/bqat)
    [![PyPI - Format](https://img.shields.io/pypi/format/bqat)](https://pypi.python.org/pypi/bqat)
    [![PyPI - Python Version](https://img.shields.io/pypi/pyversions/bqat)](https://pypi.python.org/pypi/bqat)
    [![PyPI - License](https://img.shields.io/pypi/l/bqat)](https://pypi.python.org/pypi/bqat)

    BQAT in the terminal. A CLI tool for biometric quality assessment.

+ __[API](https://github.com/Biometix/bqat-api)__

    <img alt="GitHub tag (latest by date)" src="https://img.shields.io/github/v/tag/biometix/bqat-api">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/biometix/bqat-api">
    <img alt="GitHub issues" src="https://img.shields.io/github/issues-raw/biometix/bqat-api">
    <img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/m/biometix/bqat-api">
    <img alt="GitHub" src="https://img.shields.io/github/license/biometix/bqat-api">

    BQAT via RESTful API. A self-contained server solution.

+ __[Stateless](https://github.com/Biometix/bqat-stateless)__

    <img alt="GitHub tag (latest by date)" src="https://img.shields.io/github/v/tag/biometix/bqat-stateless">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/biometix/bqat-stateless">
    <img alt="GitHub issues" src="https://img.shields.io/github/issues-raw/biometix/bqat-stateless">
    <img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/m/biometix/bqat-stateless">
    <img alt="GitHub" src="https://img.shields.io/github/license/biometix/bqat-stateless">

    Stateless BQAT API. Single endpoint server, best for micro service deployment.

+ __[GUI](https://github.com/Biometix/bqat-gui)__

    <img alt="GitHub tag (latest by date)" src="https://img.shields.io/github/v/tag/biometix/bqat-gui">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/biometix/bqat-gui">
    <img alt="GitHub issues" src="https://img.shields.io/github/issues-raw/biometix/bqat-gui">
    <img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/m/biometix/bqat-gui">
    <img alt="GitHub" src="https://img.shields.io/github/license/biometix/bqat-gui">

    Refernece frontend for BQAT API. An easy to use user interface to the BQAT services.

## Roadmap

- [x] Face image analysis module
- [x] Fingerprint image analysis module
- [x] Iris image analysis module
- [x] Speech audio file analysis module
- [x] Result EDA reporting feature
- [x] Image formating feature as preprocess
- [x] Image resizing feature as preprocess
- [x] [OFIQ](https://www.bsi.bund.de/EN/Themen/Unternehmen-und-Organisationen/Informationen-und-Empfehlungen/Freie-Software/OFIQ/OFIQ_node.html) processing engine for face modality
- [x] ARM CPU support
- [ ] Ray cluster based distributed processing for CLI and API
- [ ] Duplicates removal feature for output
- [ ] Identity removal feature as preprocess
- [ ] Document image quality check for face modality
- [ ] Contact lens detection feature for face modality
- [ ] Face liveness detection feature for face modality
- [ ] NFIQ1 as alternative fingerprint processing engine
- [ ] Morphing detection
- [ ] Spoofing detection
- [ ] Iris PAD detection
- [ ] GPU acceleration

More to come! 🚀

---

{: .highlight }
> Please [contact us](https://biometix.github.io/about/#about-us) if you'd like more information.
