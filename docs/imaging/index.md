---
title: Functional Imaging
excerpt: QC
layout: single
permalink: /imaging/
---

This project involves the compilation of resting state functional MRI data from multiple large-scale studies focused on aging across adult lifespan. All raw and processed functional data and associated metadata are curated to conform to the [Brain Imaging Data Structure (BIDS)](https://bids.neuroimaging.io) standard to ensure consistency and reproducibility across datasets. 

Data pre-processing follows a standardized pipeline using tools such as [fMRIPrep](https://fmriprep.org), [XCP-D](https://xcp-d.readthedocs.io/en/latest/index.html). 

---
## Derived Measures

The output measures from XCP-D included cleaned BOLD timeseries, nuisance confounds, image quality metrics, derived functional connectivity matrices, ALFF and ReHo using commonly-used parcellations Glasser, Gordon, Schaefer and Tian atlases.

# ![](/assets/images/preprocessing_flow.png)
---
## Personalized Functional Networks

The denoised 4D BOLD timeseries were subsequently used as input to [pNet](https://github.com/MLDataAnalytics/pNet), a framework for computing sparse,non-negative, personalized functional networks. This approach enables the extraction of personalized large-scale networks that represents subject-specific functional topography while mainitaining correspondence across individuals.

Using pNet, we identified **17 individualized functional networks** for each participant. These personalized maps were then used to compute **subject-specific functional connectivity matrices**.

![](/assets/images/pfn.jpg)
*Figure 2: Example pNet-derived group networks.*

---
## Quality control and Harmonization

Quality control measures included frame-wise displacement and nodal coverage. fMRI runs with a mean FD less than or equal to 0.2 mm and fewer than 10 nodes with missing coverage(NA) were retained for downstream analysis.

![](/assets/images/fmri_qc.png)