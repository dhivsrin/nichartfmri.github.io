---
layout: home
title: "NiChart fMRI Imaging & Harmonization"
author_profile: false
---

<div style="text-align: center;">
     <img src="/nichartfmri.github.io/assets/images/logos/nichartfmri_logo.png" width="70%" height="auto" />
</div>

<div style="text-align:center;">
  <div style="display:flex; justify-content:center;">
    <b>
      NiChart-fMRI: Compilation of large scale resting state functional MRI data and Harmonization
    </b>
  </div>

  <p>
    This project involves the compilation of resting state functional MRI data from multiple large-scale studies focused on aging across the adult lifespan. All raw and processed functional data and associated metadata are curated to conform to the <a href="https://bids.neuroimaging.io">Brain Imaging Data Structure (BIDS)</a> standard to ensure consistency and reproducibility across datasets. Data pre-processing follows a standardized pipeline using tools such as <a href="https://fmriprep.org">fMRIPrep</a> and <a href="https://xcp-d.readthedocs.io/en/latest/index.html">XCP-D</a>.
  </p>

  <div style="display:flex; justify-content:center;">
    <b>Derived Measures</b>
  </div>
  <p>
    The output measures from XCP-D include cleaned BOLD timeseries, nuisance confounds, image quality metrics, and derived functional connectivity matrices, ALFF, and ReHo using commonly-used parcellations including Glasser, Gordon, Schaefer, and Tian atlases.
  </p>

  <div style="display:flex; justify-content:center;">
    <b>Personalized Functional Networks</b>
  </div>
  <p>
    The denoised 4D BOLD timeseries were subsequently used as input to <a href="https://github.com/MLDataAnalytics/pNet">pNet</a>, a framework for computing sparse, non-negative, personalized functional networks. This approach enables the extraction of personalized large-scale networks that represent subject-specific functional topography while maintaining correspondence across individuals. Using pNet, we identified <b>17 individualized functional networks</b> for each participant. These personalized maps were then used to compute <b>subject-specific functional connectivity matrices</b>.
  </p>

  <div style="display:flex; justify-content:center;">
    <b>Quality Control and Harmonization</b>
  </div>
  <p>
    Quality control measures included frame-wise displacement and nodal coverage. fMRI runs with a mean FD ≤ 0.2 mm and fewer than 10 nodes with missing coverage (NA) were retained for downstream analysis.
  </p>
</div>

