---
layout: page
title: Advanced Support
nav_order: 6
---

# Advanced Support

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

## Scaling
<a name="scaling">

To process large datasets, you can apply the following strategies:

+ You may deploy BQAT-Stateless as a [cluster](https://biometix.github.io/playbook/stateless.html#scalability) of containers across your array of servers.
+ You may split the dataset into smaller chunks and process them in parallel using BQAT-CLI or BQAT-API (only vertical scaling is supported by default).

Depend on your use case, you might need customised scaling solution in the cloud or on-premise. We will help to design and implement horizontal scaling for BQAT-CLI and BQAT-API (BQAT-GUI).

## Optimisation
<a name="optimisation">

By default, BQAT is not optimised to use all available CPU cores and memory due to robustness and stability concerns. We will need to look at the specifications of your machine to suggest the best configuration for you.

On the other hand, GPU acceleration is not enabled in BQAT. We will need to look at the specifications of your GPU and driver version to suggest the best configuration for you. This will speed up a series of machine learning components of the algorithm.

## Security
<a name="security">

We continuously monitor CVEs and available patches for dependencies. If you have specific security requirements, we're here to help you mitigate any risks in your production environment.

## Compliance
<a name="compliance">

Through the provision of quality metrics, BQAT can help to evaluate the quality of your data for international standard compliance. For instance, regarding face, [ISO 29794-5](https://www.iso.org/standard/81005.html) is the relevant international standard we are looking at. If you would like to add other quality metrics, we can help you to customise BQAT to meet your compliance requirements.

## Customisation
<a name="customisation">

BQAT offers customisation options such as:
+ Data IO customisation (e.g. base64 handling, output formating)
+ API endpoint customisation (adapt to upstream and downstream system)
+ EDA report customisation (advance visualisation)
+ Web access control for remote user
+ Backend data storage management
+ Metric score calibration and labeling customisation (adapt to different compliance standard)

{: .highlight }
> [Contact us](https://biometix.github.io/about/#about-us) for advanced support.