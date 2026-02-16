# LSST-Crowded-Fields
By Audrey Budlong

## LSST Crowded Fields Processing Pipeline – Development Notebooks

This repository contains a collection of Jupyter notebooks and supporting code used to explore, prototype, and validate components of a new crowded-fields processing pipeline for the Rubin Observatory Legacy Survey of Space and Time (LSST).

The notebooks document experiments, comparisons, and algorithm development focused on improving source detection, modeling, and photometry in highly crowded stellar fields, where standard pipelines face significant challenges due to blending and complex PSF structure.

This repository serves as a research and development workspace for testing ideas, validating methods, and guiding implementation of future pipeline components.

## Repository Structure

The repository is organized into four main directories, each corresponding to a major area of investigation:
- <code>1-dataSelection/</code>
- <code>2-crowdSource/</code>
- <code>3-modelImages/</code>
- <code>4-wingsCode</code>

### <code>1-dataSelection/</code>

This directory contains notebooks and utilities for selecting and preparing datasets used throughout the pipeline development process.

Topics include:
- Selection of crowded field regions from LSST simulations or processed data
- Querying and filtering exposures and visit images
- Preparing inputs for downstream modeling and photometric analysis
- Data quality inspection and validation

These notebooks define the datasets used for algorithm testing and benchmarking.

### <code>2-crowdSource/</code>

This directory contains notebooks analyzing outputs from crowdSource, a crowded-field photometry package.

Topics include:
- Running crowdSource on LSST-like data
- Evaluating source detection performance
- Comparing photometry and astrometry to reference catalogs
- Investigating blending behavior and residual structure
- Identifying strengths and limitations relative to LSST pipeline methods

These notebooks help establish baseline performance and guide improvements.

### <code>3-modelImages/</code>

This directory contains notebooks for building and inspecting model images from two different pipelines:

**LSST Pipeline Model Images**

These notebooks use outputs from the LSST Science Pipelines to reconstruct the model image that the pipeline fits to the data.

They allow you to:
- Rebuild the full model image from fitted sources
- Compare the model to the original image
- Examine residuals (data − model)
- See how flux is distributed between blended sources

This helps diagnose how the LSST pipeline handles crowded regions.

**crowdSource Model Images**

These notebooks use crowdSource outputs to construct its corresponding model image.

They allow you to:
- Recreate the crowdSource model image
- Inspect residuals
- Compare its behavior to the LSST model and original exposures

### <code>4-wingsCode/</code>

This directory contains notebooks and prototype implementations of new modeling approaches, including experimental "wings" modeling.

These methods focus on improving treatment of:
- Extended PSF wings
- Residual minimization

This directory represents active development of new techniques intended for integration into future pipeline components.

### Requirements

Typical requirements include:
- Python 3.10+
- Jupyter Notebook or JupyterLab
- LSST Science Pipelines
- NumPy
- Matplotlib
- Astropy

*Additional dependencies may be required depending on the notebook.*
