---
layout: default
title: CHANGELOG
nav_order: 7
permalink: /changelog/
---

# CHANGELOG

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

## BQAT-Core

<a name="v1.6.4"></a>

### v1.6.4 (2025-10-29) 🆕

#### 📎 Miscellaneous
{: .no_toc }

- Add dependency artifact for aarch64 build


<a name="v1.6.3"></a>

### v1.6.3 (2025-09-16)

#### 🚀 Features
{: .no_toc }

- Add image file metadata

#### 🛠️️️ Fixes
{: .no_toc }

- Refactor boolean value to numerical value
- Refactor submodule import path logic
- Fix face engine config issue
- Fix NFIQ2 error message issue


<a name="v1.6.2"></a>

### v1.6.2 (2025-06-11)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Refactor submodule logic of processing engines


<a name="v1.6.1"></a>

### v1.6.1 (2025-04-09)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Fix overwritten issue for duplicated attributes in fusion mode
- Fix overwritten issue for duplicated names in output specs 

#### 📎 Miscellaneous
{: .no_toc }

- Refactor some error log handling logic


<a name="v1.6.0"></a>

### v1.6.0 (2025-02-07)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Add head location estimation


<a name="v1.5.3"></a>

### v1.5.3 (2025-02-03)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Improve smile estimation performance
- Improve eyeglasses detection performance


<a name="v1.5.2"></a>

### v1.5.2 (2024-12-05)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Add support for CPU allocation control
- Add metrics for colour temperature (pro)


<a name="v1.5.1"></a>

### v1.5.1 (2024-11-18)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Add metrics for image colour temperature (pro)

#### 🛠️️️ Fixes
{: .no_toc }

- Refactor speech engine to optimize container size
- Better handling for failed face mesh detection


<a name="v1.5.0"></a>

### v1.5.0 (2024-11-07)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Fix pupil location bug

#### 🚀 Features
{: .no_toc }

- Add metrics for face location offset
- Add metrics for face area ratio
- Add image metadata, includes brightness, dynamic range, contrast and sharpness
- Add fusion engine mode for face modality
- Disable warning log in prod mode
- Add metrics for eye gazing direction (pro)
- Add eye colour detection (pro)
- Add metrics for image background (pro)
- Add metrics for hair coverage (pro)
- Add metrics for headgear detection (pro)


<a name="v1.4.5"></a>

### v1.4.5 (2024-10-09)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Fix OFIQ face engine folder mode output vaule type issue
- Switch to system temporary directory for OFIQ folder mode


<a name="v1.4.4"></a>

### v1.4.4 (2024-09-26)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Fix error log issue
- Switch to system temporary directory for fingerprint conversion


<a name="v1.4.3"></a>

### v1.4.3 (2024-08-14)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Rebuild OFIQ engine to support single file processing

<a name="v1.4.2"></a>

### v1.4.2 (2024-05-01)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Fix reporting filepath label issue

<a name="v1.4.1"></a>

### v1.4.1 (2024-04-22)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Fix speech modality logging issue

<a name="v1.4.0"></a>

### v1.4.0 (2024-04-10)
{: .no_toc }

#### 🚀 Features
{: .no_toc }
- Introduce OFIQ engine for face modality (alpha) [#15](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-core/-/issues/15)

#### 🛠️️️ Fixes
{: .no_toc }

- Iris resize and convert issue

<a name="v1.3.6"></a>

### v1.3.6 (2024-04-04)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Update iris engine resizing range to improve iris engine robustness

<a name="v1.3.5"></a>

### v1.3.5 (2024-03-13)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Fix fingerprint modality metrics naming issue [#20](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-core/-/issues/20)

<a name="v1.3.4"></a>

### v1.3.4 (2024-03-13)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Fix fingerprint file format conversion issue [#19](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-core/-/issues/19)

<a name="v1.3.3"></a>

### v1.3.3 (2024-02-26)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Lower resolution to improve engine robustness [#17](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-core/-/issues/17)

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Add alternate conda env file for speech

<a name="v1.3.2"></a>

### v1.3.2 (2023-12-14)
{: .no_toc }

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Update for refactoring image building configuration

<a name="v1.3.1"></a>

### v1.3.1 (2023-07-28)
{: .no_toc }

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Cleanup cli log

<a name="v1.3.0"></a>

### v1.3.0 (2023-07-28)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Update iris module with new metrics
- Modify certain iris assessment thresholds to handle wider target samples
- Update face quality scoring with ISO/IEC 29794-1 standard scale (1-100) [#11](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-core/-/issues/11)
- Add glasses detection for face modality

#### 🛠️️️ Fixes
{: .no_toc }

- Fix iris score issue with low sclera related values [#10](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-core/-/issues/10)

<a name="v1.2.2"></a>

### v1.2.2 (2023-06-09)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Speech mode recursive glob

<a name="v1.2.1"></a>

### v1.2.1 (2023-05-17)
{: .no_toc }

####  🚀 Features
{: .no_toc }

- Handle negtive corrdinates [#6](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-core/-/issues/6)

<a name="v1.2.0"></a>

### v1.2.0 (2023-04-18)
{: .no_toc }

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Update Dockerfile and test cases for speech module

<a name="v1.1.0"></a>

### v1.1.0 (2023-04-11)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Add fingerprint module
- Add iris module
- Add test module
- Disable df and bk
- Add speech model [#3](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-core/-/issues/3)

#### 🛠️️️ Fixes
{: .no_toc }

 - Bug fixes

#### 📚 Documentation
{: .no_toc }

- Update readme

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Initial commit

- Update gitignore

- Update lock file

---


## BQAT-API

<a name="v1.6.0"></a>

### v1.6.0 (2025-10-07) 🆕

#### 🚀 Features
{: .no_toc }

- OFIQ upgrade to [v1.0.3](https://github.com/BSI-OFIQ/OFIQ-Project/releases/tag/v1.0.3)
- NFIQ2 upgrade to [v2.3.0](https://github.com/usnistgov/NFIQ2/releases/tag/v2.3.0)


<a name="v1.5.2"></a>

### v1.5.2 (2025-04-29)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Support selected input rerun [#32](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-api/-/issues/32)


<a name="v1.5.1"></a>

### v1.5.1 (2025-04-10)

#### 🚀 Features

- Support input file filter for fusion mode [#22](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-api/-/issues/22)


<a name="v1.5.0"></a>

### v1.5.0 (2025-04-07)

#### 🚀 Features

- Support various benchmarking functionalities [#20](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-api/-/issues/20)

- Support file management feature [#14](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-api/-/issues/14)

- Support file deduplication [#14](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-api/-/issues/14)

- Support dataset modality estimation [#14](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-api/-/issues/14)


#### 📎 Miscellaneous

- Refactor speech mode [#21](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-api/-/issues/21)


<a name="v1.4.4"></a>

### v1.4.4 (2025-02-07)

#### 🛠️️️ Fixes
{: .no_toc }

- Fix beanie pydantic conflict model schema issue


<a name="v1.4.3"></a>

### v1.4.3 (2024-12-05)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Improve host resources allocation config


<a name="v1.4.0"></a>

### v1.4.0 (2024-09-09)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Support OFIQ engine

- Add engine selection flag

- Add preprocessing flag

- Support image resizing

- Support image conversion

- Add reporting flag

- Add outlier detection flag

- Support BQAT-GUI integration

- Refactor task control endpoints

- Add simple input data preview page

- Support JP2, WSQ image preview

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Migrate to Pydantic V2

<a name="v1.3.0"></a>

### v1.3.0 (2023-12-15)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }
- Resolve test script issue

#### 📎 Miscellaneous Tasks
{: .no_toc }
- Rework docker image [#9](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-api/-/issues/9)

- Rework dockerfile [#9](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-api/-/issues/9)

<a name="v1.2.0"></a>

### v1.2.0 (2023-07-28)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Update iris engine

#### 🛠️️️ Fixes
{: .no_toc }

- Fix Python dependency issues
- Fix endpoint path issues

<a name="v1.1.0"></a>

### v1.1.0 (2023-06-14)
{: .no_toc }
#### 🚀 Features
{: .no_toc }

- implement speech module [#1](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-api/-/issues/1)


<a name="v1.0.0"></a>

### v1.0.0 (2023-02-17)
{: .no_toc }

#### 🚧 Refactor
{: .no_toc }

- Update report title

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Update cicd config


---


## BQAT-CLI

<a name="v1.8.4"></a>

# v1.8.4 (2025-11-12) 🆕

#### 🚀 Features
{: .no_toc }

- Improve input/output path handling.
- Add flag to CLI for shared memory config.

#### 🔧 Fixes
{: .no_toc }

- Resolve CSV heading empty line issue.
- Resolve Windows data table path issue.

<a name="v1.8.3"></a>

### v1.8.3 (2025-11-10)
{: .no_toc }

#### 🔧 Fixes
{: .no_toc }

- Resolve wsq dependency issue on arm64 platform.
- Rework file path for fingerprint mode.

<a name="v1.8.2"></a>

### v1.8.2 (2025-11-05)
{: .no_toc }

#### ⚙️ Miscellaneous
{: .no_toc }

- Refactor Dockerfile

<a name="v1.8.1"></a>

### v1.8.1 (2025-10-30)
{: .no_toc }

#### 🔧 Fixes
{: .no_toc }

- Fix OFIQ recursive input dir issue.
- Resolve job type flag conflict.

#### 🚀 Features
{: .no_toc }

- AArch64 Support [#48](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/48)
- Add version check up at runtime.

<a name="v1.7.1"></a>

### v1.7.1 (2025-10-09)
{: .no_toc }

#### 🛠️ Fixes
{: .no_toc }

- Fix engine flag bug.

#### 🚀 Features
{: .no_toc }

- New entry point [#45](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/45)

<a name="v1.7.0"></a>

### v1.7.0 (2025-09-15)
{: .no_toc }

#### 🛠️Fixes
{: .no_toc }

- Upgrade Dockerfile to remove conda env.
- Rework OFIQ engine processing logic.

#### 🚀 Features
{: .no_toc }

- Add fusion engine benchmarking support.
- Upgrade NFIQ2 to v2.3.0
- New installation method [#36](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/36)
- Upgrade OFIQ to v1.0.3 [#42](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/42)


<a name="v1.6.1"></a>
 
### v1.6.1 (2024-05-01)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Fix conversion type issue.
- Fix resizing width issue.
- Fix BMP format issue.
- Fix reporting column label issue.


<a name="v1.6.0"></a>
 
### v1.6.0 (2024-04-24)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Support Engine Flag for Benchmarking [#29](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/29)

- Introduce preprocessing mode (image conversion, resizing) [#30](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/30)

- Update convenience script with dynamic shared memory allocation feature.

#### 🛠️️️ Fixes
{: .no_toc }

- Fix iris benchmarking sample file conflict issue. [#28](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/28)

- Fix speech modality logging issue.


#### 📎 Miscellaneous Tasks
{: .no_toc }

- Improve logging readability.

<a name="v1.5.1"></a>
 
### v1.5.1 (2024-04-11)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Add update command in the run script to pull latest container.

- Add report flag to let the user disable reporting feature. [#15](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/15)

#### 🛠️️️ Fixes
{: .no_toc }
- Fix broken benchmarking module.

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Revert opencv in nfiq2

<a name="v1.5.0"></a>
 
### v1.5.0 (2024-04-09)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Support OFIQ engine for face modality (alpha). [#25](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/25)

- Add optional flag for alternate face modality engine.

<a name="v1.4.1"></a>
 
### v1.4.1 (2024-03-13)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Add reporting mode

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Update readme

- Build configuration refactor.


<a name="v1.3.0"></a>
 
### v1.3.0 (2023-07-28)
{: .no_toc }

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Rebuild with bqat-core v1.3.1.
- Update image dependencies


<a name="v1.2.4"></a>
 
### v1.2.4 (2023-06-09)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Fix speech mode recursive glob issue.


<a name="v1.2.3"></a>
 
### v1.2.3 (2023-05-23)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Update quality report module. [#12](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/12)


<a name="v1.2.2"></a>
 
### v1.2.2 (2023-04-13)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Bug Fixes

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Update Dockerfile


<a name="v1.2.1"></a>
 
### v1.2.1 (2023-04-12)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Introduce speech assessment feature. [#9](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/9)


- Add test cases [#11](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/11)


- Generate test reports [#5](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/5)


<a name="v1.1.2"></a>
 
### v1.1.2 (2023-02-24)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Add filter flag [#2](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/2)

#### 🛠️️️ Fixes
{: .no_toc }

- Fix OOM issue
- Resolve "Output issue with small dataset" [#6](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/6)
- Resolve "One incomplete input no output" [#7](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat/-/issues/7)

#### 🚧 Refactor
{: .no_toc }

- Redo csv output function

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Initial commit

- Update readm

- Add basic test cases

- Update gitlab-ci.yml

- Update scripts

- Update submodules

---

## BQAT-Stateless

<a name="v0.5.1"></a>

### v0.5.1 (2025-02-26)

#### 🚀 Features
{: .no_toc }

- Expose configuration for server worker number as env variable.

<a name="v0.5.0"></a>

### v0.5.0 (2025-02-11)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Update core to 1.6.0
- Add engine selection support [#9](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-stateless/-/issues/9)

<a name="v0.4.1"></a>

### v0.4.1 (2023-12-15)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Resolve temp file conflict issue.

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Update compose file.
- Refactor build configuration [#5](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-stateless/-/issues/5)


<a name="v0.4.0"></a>

### v0.4.0 (2023-07-28)
{: .no_toc }

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Rebuilt with latest BQAT-core.

<a name="v0.3.3"></a>

### v0.3.3 (2023-07-28)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Update iris module

#### 🛠️️️ Fixes
{: .no_toc }

- Iris quality score
- Fix base64 padding

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Update test cases for new metrics

<a name="v0.3.2"></a>

### v0.3.2 (2023-04-26)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Add testing samples [#3](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-stateless/-/issues/3)

- Update coverage report


<a name="v0.3.1"></a>

### v0.3.1 (2023-04-25)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Support base64url format

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Update metadata


<a name="v0.3.0"></a>

### v0.3.0 (2023-04-24)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Update endpoints to support base64 format [#2](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-stateless/-/issues/2)


<a name="v0.2.0"></a>

### v0.2.0 (2023-04-24)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Introduce speech assessment feature. [#1](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-stateless/-/issues/1)


<a name="v0.1.0"></a>

### v0.1.0 (2023-03-22)
{: .no_toc }

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Initial commit

- Add LICENSE

- Update .gitlab-ci.yml file

---

## BQAT-GUI

<a name="v0.3.13"></a>

### v0.3.13 (2025-02-11)

#### 🛠️️️ Fixes
{: .no_toc }

- Outlier table bug resolved


<a name="v0.3.12"></a>
### v0.3.12 (2025-02-04)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- 💡 Fetch quality metric description from API

- 💡 Better preview table for outliers

#### 🛠️️️ Fixes
{: .no_toc }

- Put default config file in the container


<a name="v0.3.11"></a>
### v0.3.11 (2024-12-05)
{: .no_toc }

#### 🛠️️️️️ Fixes
{: .no_toc }

- 🐛 Auth trategy issues

- Minor refactor


<a name="v0.3.10"></a>
### v0.3.10 (2024-12-02)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- 🐛 Operational UI issues


<a name="v0.3.9"></a>
### v0.3.9 (2024-11-27)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- UI layout issues


<a name="v0.3.8"></a>
### v0.3.8 (2024-11-21)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- 💡 Support runtime environment variables


<a name="v0.3.7"></a>
### v0.3.7 (2024-10-29)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- 💡 Introduce file management tab (beta)

- 💡 Introduce landing page (beta)

- 🙌 Add fail-safe logic that work with backend health check feature

#### 🛠️️️ Fixes
{: .no_toc }

- Improve outlier detection UX


<a name="v0.3.6"></a>
### v0.3.6 (2024-10-03)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- 🙌 Render audio player in preview

#### 🛠️️️ Fixes
{: .no_toc }

- Improve UX


<a name="v0.3.1"></a>
### v0.3.1 (2024-09-19)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Task log loading issue

- Collapse input folder view

- Minor UX fixes


<a name="v0.3.0"></a>
### v0.3.0 (2024-09-09)
{: .no_toc }

#### 🚧 Refactor
{: .no_toc }

- Refactor project structure


<a name="v0.2.5"></a>
### v0.2.5 (2024-05-31)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- 💡 Add desktop version for BQAT

- 🙌 Implement preprocess layout

#### 🛠️️️ Fixes
{: .no_toc }

- 🔧 Outlier reloading issue

- Check report function not stop

#### 🚧 Refactor
{: .no_toc }

- Initialise reports lifecycle

#### 📚 Documentation
{: .no_toc }

- Modify binary image install&desktop development

#### 🎨 Styling
{: .no_toc }

- Update the workflow text & icons on home page

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Update text&button


<a name="v0.2.4"></a>
### v0.2.4 (2024-05-29)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Configurate detector column options

- 🙌 Make outlier request with configurations

- Set match file by name&type

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Format code


<a name="v0.2.3"></a>
### v0.2.3 (2024-05-28)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- 🙌 Implement outlier detector section

#### 🚧 Refactor
{: .no_toc }

- Refactor the structure of loading reports

#### 📚 Documentation
{: .no_toc }

- 💡 Add comments for all methods


<a name="v0.2.2"></a>
### v0.2.2 (2024-05-22)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- 🙌  Implement scan local path

#### 🚧 Refactor
{: .no_toc }

- Refactor the uploader section


<a name="v0.2.1"></a>
### v0.2.1 (2024-05-09)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- 🔧 Internal connnect & image ratio issue

- 🔧 Internal connnect & image ratio issue

- 🔧 Issue of image ratio when preview


<a name="v0.2.0"></a>
### v0.2.0 (2024-04-23)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Make the home icons controllable.

- Finish scan input page

- Develop the basic framework of  BQAT new UI

- Connect new UI with backend  server

- Finish develop all basic features with backends

#### 🎨 Styling
{: .no_toc }

- 💡 Add some icons for items

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Delete useless files

- Remove useless files

<a name="v0.1.9"></a>

### v0.1.9 (2023-08-14)
{: .no_toc }

#### 🚀 Features
{: .no_toc }


- Update “Clear” button to clear the page as well as user data [#7](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-gui/-/issues/7)


<a name="v0.1.8"></a>

### v0.1.8 (2023-08-14)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Resolve: Remove the samples and and associated documents after retrival [#6](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-gui/-/issues/6)



<a name="v0.1.6"></a>

### v0.1.6 (2023-07-28)
{: .no_toc }

#### 📎 Miscellaneous Tasks
{: .no_toc }

- Cleanup CSV output
- Update compose configuration

<a name="v0.1.5"></a>

### v0.1.5 (2023-07-13)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- Hotfix


<a name="v0.1.4"></a>

### v0.1.4 (2023-07-13)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }

- hotfix-temp-folder


<a name="v0.1.3"></a>

### v0.1.3 (2023-07-11)
{: .no_toc }

#### 🛠️️️ Fixes
{: .no_toc }


- Fix temporary export file issue [#2](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-gui/-/issues/2)




<a name="v0.1.2"></a>

### v0.1.2 (2023-06-07)
{: .no_toc }

#### 🚀 Features
{: .no_toc }

- Introduce Web GUI


#### 📎 Miscellaneous Tasks
{: .no_toc }


- Initial commit


- Update pyproject.toml


- Refactor layout and update README


- Add docker deployment option


<!-- generated by Biometix -->
