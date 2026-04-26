# Hopewell Earthworks LiDAR - CAE Anomaly Detection: Anomaly is All You Need
This repository is for applying ML techniques on LiDAR imaging of Ohio's Hopewell earthworks. This effort is being written in a Python 3.11.9 environment.

A bespoke Convolutional Autoencoder was trained on LiDAR DEM tiles of Ohio terrain. Then a test dataset of a balance of normal terrain tiles and tiles with Hopewell earthworks is evaluated to detect Hopewell earthworks as anomalies from the reconstruction error.  An ablation study with six variants of the model was conducted to evaluate model response to the data. Please refer to the paper for more information.

## Requirements
- Python 3.11 or equivalent
- Jupyter Notebook
- Install dependencies from requirements.txt: pip install -r requirements.txt
- All models were developed and run on a CPU. No GPU required.

## Data Source
Ohio Geographically Referenced Information Program
https://gis1.oit.ohio.gov/geodatadownload/

A list of tiles used in this study are in this repo under the tiles_and_weights folder. To acquire the data one needs to access the site and look for the tile IDs from the tile_and_weights folder. This direct link to the DEM files by county may be useful for gathering these: https://gis1.oit.ohio.gov/ZIPARCHIVES_III/ELEVATION/3DEP/DEM/

Weights for the baseline model and the baseline model+HPF are included in the tiles_and_weights folder. See the paper for more information. The Jupyter Notebooks contain sections that can be uncommented to load the weights. Make certain you assign the CAE architecture to "model" before loading weights.

## Geographic Focus
- Ohio 
- UNESCO World Heritage List sites for Hopewell Ceremonial Earthworks: https://whc.unesco.org/en/list/1689/maps/

## Notebooks
Each notebook can run independently.

- 01_cae_v1.ipynb — Baseline CAE model (no output activation)
- 01_cae_v2.ipynb — CAE with TanH output activation
- 01_cae_v3.ipynb — CAE with Sigmoid output activation
- 01_cae_hpf1.ipynb — Baseline CAE with high-pass filter
- 01_cae_hpf2.ipynb — TanH CAE with high-pass filter
- 01_cae_hpf3.ipynb — Sigmoid CAE with high-pass filter

## Notes:
Author is Dennis Guhl, Graduate Student for a MAsters in Data Science.

Though not mentioned explicitly in the paper, the approach taken for the paper is echoing a CRISP-DM approach in problem solution while ising an IEEE template.

This repo will be accessible by the public until Memorial Day 2026. IF you have any comments beyond the requirements for the class then email me at guhl.2@wright.edu.
