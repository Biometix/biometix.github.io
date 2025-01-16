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

<a name="v1.5.1"></a>

### v1.5.1 (2024-11-18)

#### 🚀 Features

- Add metrics for image colour temperature (pro)

#### 🛠 Fixes

- Refactor speech engine to optimize container size
- Better handling for failed face mesh detection


<a name="v1.5.0"></a>

### v1.5.0 (2024-11-07)

#### 🛠 Fixes

- Fix pupil location bug

#### 🚀 Features

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

#### 🛠 Fixes

- Fix OFIQ face engine folder mode output vaule type issue
- Switch to system temporary directory for OFIQ folder mode


<a name="v1.4.4"></a>

### v1.4.4 (2024-09-26)

#### 🛠 Fixes

- Fix error log issue
- Switch to system temporary directory for fingerprint conversion


<a name="v1.4.3"></a>

### v1.4.3 (2024-08-14)

#### 🛠 Fixes

- Rebuild OFIQ engine to support single file processing

<a name="v1.4.2"></a>

### v1.4.2 (2024-05-01)

#### 🛠 Fixes

- Fix reporting filepath label issue

<a name="v1.4.1"></a>

### v1.4.1 (2024-04-22)

#### 🛠 Fixes

- Fix speech modality logging issue

<a name="v1.4.0"></a>

### v1.4.0 (2024-04-10)

#### 🚀 Features
- Introduce OFIQ engine for face modality (alpha) [#15](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-core/-/issues/15)

#### 🛠 Fixes

- Iris resize and convert issue

<a name="v1.3.6"></a>

### v1.3.6 (2024-04-04)

#### 🛠 Fixes

- Update iris engine resizing range to improve iris engine robustness

<a name="v1.3.5"></a>

### v1.3.5 (2024-03-13)

#### 🛠 Fixes

- Fix fingerprint modality metrics naming issue [#20](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-core/-/issues/20)

<a name="v1.3.4"></a>

### v1.3.4 (2024-03-13)

#### 🛠 Fixes

- Fix fingerprint file format conversion issue [#19](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-core/-/issues/19)

<a name="v1.3.3"></a>

### v1.3.3 (2024-02-26)

#### 🛠 Fixes

- Lower resolution to improve engine robustness [#17](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-core/-/issues/17)

#### ⚙️ Miscellaneous Tasks

- Add alternate conda env file for speech

<a name="v1.3.2"></a>

### v1.3.2 (2023-12-14)

#### ⚙️ Miscellaneous Tasks

- Update for refactoring image building configuration

<a name="v1.3.1"></a>

### v1.3.1 (2023-07-28)

#### ⚙️ Miscellaneous Tasks

- Cleanup cli log

<a name="v1.3.0"></a>

### v1.3.0 (2023-07-28)

#### 🚀 Features

- Update iris module with new metrics
- Modify certain iris assessment thresholds to handle wider target samples
- Update face quality scoring with ISO/IEC 29794-1 standard scale (1-100) [#11](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-core/-/issues/11)
- Add glasses detection for face modality

#### 🛠 Fixes

- Fix iris score issue with low sclera related values [#10](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-core/-/issues/10)

<a name="v1.2.2"></a>

### v1.2.2 (2023-06-09)

#### 🛠 Fixes

- Speech mode recursive glob

<a name="v1.2.1"></a>

### v1.2.1 (2023-05-17)

####  🚀 Features

- Handle negtive corrdinates [#6](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-core/-/issues/6)

<a name="v1.2.0"></a>

### v1.2.0 (2023-04-18)

#### ⚙️ Miscellaneous Tasks

- Update Dockerfile and test cases for speech module

<a name="v1.1.0"></a>

### v1.1.0 (2023-04-11)

#### 🚀 Features

- Add fingerprint module
- Add iris module
- Add test module
- Disable df and bk
- Add speech model [#3](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-core/-/issues/3)

#### 🛠 Fixes

 - Bug fixes

#### 📚 Documentation

- Update readme

#### ⚙️ Miscellaneous Tasks

- Initial commit

- Update gitignore

- Update lock file

---


## BQAT-API

<a name="v1.4.0"></a>

### v1.4.0 (2024-09-09)

#### 🚀 Features

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

#### ⚙️ Miscellaneous Tasks

- Migrate to Pydantic V2

<a name="v1.3.0"></a>

### v1.3.0 (2023-12-15)

#### 🛠 Fixes
- Resolve test script issue

#### ⚙️ Miscellaneous Tasks
- Rework docker image [#9](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-api/-/issues/9)

- Rework dockerfile [#9](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-api/-/issues/9)

<a name="v1.2.0"></a>

### v1.2.0 (2023-07-28)

#### 🚀 Features

- Update iris engine

#### 🛠 Fixes

- Fix Python dependency issues
- Fix endpoint path issues

<a name="v1.1.0"></a>

### v1.1.0 (2023-06-14)
#### 🚀 Features

- implement speech module [#1](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-api/-/issues/1)


<a name="v1.0.0"></a>

### v1.0.0 (2023-02-17)

#### 🚧 Refactor

- Update report title

#### ⚙️ Miscellaneous Tasks

- Update cicd config


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

<a name="v0.3.11"></a>
### v0.3.11 (2024-12-05)

#### 🛠 Fixes

- 🐛 Auth trategy issues

- Minor refactor


<a name="v0.3.10"></a>
### v0.3.10 (2024-12-02)

#### 🛠 Fixes

- 🐛 Operational UI issues


<a name="v0.3.9"></a>
### v0.3.9 (2024-11-27)

#### 🛠 Fixes

- UI layout issues


<a name="v0.3.8"></a>
### v0.3.8 (2024-11-21)

#### 🚀 Features

- 💡 Support runtime environment variables


<a name="v0.3.7"></a>
### v0.3.7 (2024-10-29)

#### 🚀 Features

- 💡 Introduce file management tab (beta)

- 💡 Introduce landing page (beta)

- 🙌 Add fail safe logic that work with backend health check feature

#### 🛠 Fixes

- Improve outlier detection UX


<a name="v0.3.6"></a>
### v0.3.6 (2024-10-03)

#### 🚀 Features

- 🙌 Render audio player in preview

#### 🛠 Fixes

- Improve UX


<a name="v0.3.1"></a>
### v0.3.1 (2024-09-19)

#### 🛠 Fixes

- Task log loading issue

- Collapse input folder view

- Minor UX fixes


<a name="v0.3.0"></a>
### v0.3.0 (2024-09-09)

#### 🚧 Refactor

- Refactor project structure


<a name="v0.2.5"></a>
### v0.2.5 (2024-05-31)

#### 🚀 Features

- 💡 Add desktop version for BQAT

- 🙌 Implement preprocess layout

#### 🛠 Fixes

- 🔧 Outlier reloading issue

- Check report function not stop

#### 🚧 Refactor

- Initialise reports lifecycle

#### 📚 Documentation

- Modify binary image install&desktop development

#### 🎨 Styling

- Update the workflow text & icons on home page

#### ⚙️ Miscellaneous Tasks

- Update text&button


<a name="v0.2.4"></a>
### v0.2.4 (2024-05-29)

#### 🚀 Features

- Configurate detector column options

- 🙌 Make outlier request with configurations

- Set match file by name&type

#### ⚙️ Miscellaneous Tasks

- Format code


<a name="v0.2.3"></a>
### v0.2.3 (2024-05-28)

#### 🚀 Features

- 🙌 Implement outlier detector section

#### 🚧 Refactor

- Refactor the structure of loading reports

#### 📚 Documentation

- 💡 Add comments for all methods


<a name="v0.2.2"></a>
### v0.2.2 (2024-05-22)

#### 🚀 Features

- 🙌  Implement scan local path

#### 🚧 Refactor

- Refactor the uploader section


<a name="v0.2.1"></a>
### v0.2.1 (2024-05-09)

#### 🛠 Fixes

- 🔧 Internal connnect & image ratio issue

- 🔧 Internal connnect & image ratio issue

- 🔧 Issue of image ratio when preview


<a name="v0.2.0"></a>
### v0.2.0 (2024-04-23)

#### 🚀 Features

- Make the home icons controllable.

- Finish scan input page

- Develop the basic framework of  BQAT new UI

- Connect new UI with backend  server

- Finish develop all basic features with backends

#### 🎨 Styling

- 💡 Add some icons for items

#### ⚙️ Miscellaneous Tasks

- Delete useless files

- Remove useless files

<a name="v0.1.9"></a>

### v0.1.9 (2023-08-14)

#### 🚀 Features


- Update “Clear” button to clear the page as well as user data [#7](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-gui/-/issues/7)


<a name="v0.1.8"></a>

### v0.1.8 (2023-08-14)

#### 🛠 Fixes

- Resolve: Remove the samples and and associated documents after retrival [#6](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-gui/-/issues/6)



<a name="v0.1.6"></a>

### v0.1.6 (2023-07-28)

#### ⚙️ Miscellaneous Tasks

- Cleanup CSV output
- Update compose configuration

<a name="v0.1.5"></a>

### v0.1.5 (2023-07-13)

#### 🛠 Fixes

- Hotfix


<a name="v0.1.4"></a>

### v0.1.4 (2023-07-13)

#### 🛠 Fixes

- hotfix-temp-folder


<a name="v0.1.3"></a>

### v0.1.3 (2023-07-11)

#### 🛠 Fixes


- Fix temporary export file issue [#2](https://gitlab.com/biometix/products/biometric-quality-assessment-tool/bqat-gui/-/issues/2)




<a name="v0.1.2"></a>

### v0.1.2 (2023-06-07)

#### 🚀 Features

- Introduce Web GUI


#### ⚙️ Miscellaneous Tasks


- Initial commit


- Update pyproject.toml


- Refactor layout and update README


- Add docker deployment option


<!-- generated by Biometix -->
---

