---
layout: default
title: CHANGELOG
nav_order: 7
permalink: /changelog/
---

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

## BQAT-Core

### 1.1.0

+ Introduce speech assessment feature (alpha).

### 1.2.2

+ Refactor and bug fix for speech mode.

### 1.3.0

+ Update iris module with new metrics.

+ Modify certain iris assessment thresholds to handle wider target samples.

+ Update resize logic for iris samples.

+ Update face quality scoring with ISO/IEC 29794-1 standard scale (1-100).

+ Add glasses detection for face modality.

### 1.3.1

+ Update readme.

### 1.3.2

+ Update for refactoring image building configuration.

### 1.3.3

+ Lower input resize upper limit to improve iris engine robustness.

### 1.3.4

+ Fix fingerprint file format conversion issue.

### 1.3.5

+ Fix fingerprint modality metrics naming issue.

### 1.3.6

+ Update iris engine resizing range to improve iris engine robustness.

### 1.4.0

+ Introduce OFIQ engine for face modality (alpha).

### 1.4.1

+ Fix speech modality logging issue.

### 1.4.2

+ Fix reporting filepath label issue.


---


## BQAT-API

### 1.1.0

+ Introduce speech assessment feature.

### 1.2.0

+ Rebuild container with updated iris engine.

+ Fix Python dependency issues.

+ Fix endpoint path issues.

### 1.3.0

+ Refactor build configuration.

+ Resolve test script issue.


---


## BQAT-CLI

<a name="v1.6.1"></a>
 
### v1.6.1 (2024-05-01)

#### 🛠 Fixes

- Fix conversion type issue.
- Fix resizing width issue.
- Fix BMP format issue.
- Fix reporting column label issue.


<a name="v1.6.0"></a>
 
### v1.6.0 (2024-04-24)

#### 🚀 Features

- Support Engine Flag for Benchmarking [#29](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/29)

- Introduce preprocessing mode (image conversion, resizing) [#30](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/30)

- Update convenience script with dynamic shared memory allocation feature.

#### 🛠 Fixes

- Fix iris benchmarking sample file conflict issue. [#28](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/28)

- Fix speech modality logging issue.


#### ⚙️ Miscellaneous Tasks

- Improve logging readability.

<a name="v1.5.1"></a>
 
### v1.5.1 (2024-04-11)

#### 🚀 Features

- Add update command in the run script to pull latest container.

- Add report flag to let the user disable reporting feature. [#15](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/15)

#### 🛠 Fixes
- Fix broken benchmarking module.

#### ⚙️ Miscellaneous Tasks

- Revert opencv in nfiq2

<a name="v1.5.0"></a>
 
### v1.5.0 (2024-04-09)

#### 🚀 Features

- Support OFIQ engine for face modality (alpha). [#25](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/25)

- Add optional flag for alternate face modality engine.

<a name="v1.4.1"></a>
 
### v1.4.1 (2024-03-13)

#### 🚀 Features

- Add reporting mode

#### ⚙️ Miscellaneous Tasks

- Update readme

- Build configuration refactor.


<a name="v1.3.0"></a>
 
### v1.3.0 (2023-07-28)

#### ⚙️ Miscellaneous Tasks

- Rebuild with bqat-core v1.3.1.
- Update image dependencies


<a name="v1.2.4"></a>
 
### v1.2.4 (2023-06-09)

#### 🛠 Fixes

- Fix speech mode recursive glob issue.


<a name="v1.2.3"></a>
 
### v1.2.3 (2023-05-23)

#### 🚀 Features

- Update quality report module. [#12](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/12)


<a name="v1.2.2"></a>
 
### v1.2.2 (2023-04-13)

#### 🛠 Fixes

- Bug Fixes

#### ⚙️ Miscellaneous Tasks

- Update Dockerfile


<a name="v1.2.1"></a>
 
### v1.2.1 (2023-04-12)

#### 🚀 Features

- Introduce speech assessment feature. [#9](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/9)


- Add test cases [#11](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/11)


- Generate test reports [#5](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/5)


<a name="v1.1.2"></a>
 
### v1.1.2 (2023-02-24)

#### 🚀 Features

- Add filter flag [#2](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/2)

#### 🛠 Fixes

- Fix OOM issue
- Resolve "Output issue with small dataset" [#6](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/6)
- Resolve "One incomplete input no output" [#7](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/7)

#### 🚧 Refactor

- Redo csv output function

#### ⚙️ Miscellaneous Tasks

- Initial commit

- Update readm

- Add basic test cases

- Update gitlab-ci.yml

- Update scripts

- Update submodules

---

## BQAT-Stateless

<a name="v0.4.1"></a>

### v0.4.1 (2023-12-15)

#### 🛠 Fixes

- Resolve temp file conflict issue.

#### ⚙️ Miscellaneous Tasks

- Update compose file.
- Refactor build configuration [#5](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-stateless/-/issues/5)


<a name="v0.4.0"></a>

### v0.4.0 (2023-07-28)

#### ⚙️ Miscellaneous Tasks

- Rebuilt with latest BQAT-core.

<a name="v0.3.3"></a>

### v0.3.3 (2023-07-28)

#### 🚀 Features

- Update iris module

#### 🛠 Fixes

- Iris quality score
- Fix base64 padding

#### ⚙️ Miscellaneous Tasks

- Update test cases for new metrics

<a name="v0.3.2"></a>

### v0.3.2 (2023-04-26)

#### 🚀 Features

- Add testing samples [#3](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-stateless/-/issues/3)

- Update coverage report


<a name="v0.3.1"></a>

### v0.3.1 (2023-04-25)

#### 🚀 Features

- Support base64url format

#### ⚙️ Miscellaneous Tasks

- Update metadata


<a name="v0.3.0"></a>

### v0.3.0 (2023-04-24)

#### 🚀 Features

- Update endpoints to support base64 format [#2](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-stateless/-/issues/2)


<a name="v0.2.0"></a>

### v0.2.0 (2023-04-24)

#### 🚀 Features

- Introduce speech assessment feature. [#1](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-stateless/-/issues/1)


<a name="v0.1.0"></a>

### v0.1.0 (2023-03-22)

#### ⚙️ Miscellaneous Tasks

- Initial commit

- Add LICENSE

- Update .gitlab-ci.yml file

---

## BQAT-GUI

### 0.1.2 alpha

+ Introduce Web GUI.

### 0.1.3 alpha

+ Fix temporary export file issue.

### 0.1.6 alpha

+ Cleanup CSV output.

+ Update compose configuration.

### 0.1.8 alpha

+ Remove user data after output retrieval.

### 0.1.9 alpha

+ Update "Clear" button to clear the page as well as user data.
