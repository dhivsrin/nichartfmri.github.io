---
layout: home
title: "NiChart fMRI Imaging & Harmonization"
author_profile: false
---

<div style="text-align: center;">
     <img src="/assets/images/logos/nichartfmri_logo.png" width="70%" height="auto" />
</div>

<br/>
<hr>
<br/>
<!-- comment carousel part as we don't have banner images yet
<div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
     <ol class="carousel-indicators">
          <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
          <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
          <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
     </ol>
     <div class="carousel-inner">
          <div class="carousel-item active">
               <img class="d-block w-100" src="/assets/images/banners/rbc_corticalthickness_v2.png" alt="First slide">
               <!-- No text on carousel for now
               <div class="carousel-caption d-none d-md-block">
               <h5>{{ page.title }}</h5>
               </div>
               -->
          </div>
          <!--The arrows seem to fail
          <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="sr-only">Previous</span>
          </a>
          <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="sr-only">Next</span>
          </a>
          -->
     </div>
</div>
-->

<br/>
<hr>
<br/>

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

