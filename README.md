# Hopewell Earthworks LiDAR - CAE Anomaly Detection
This repository is for applying ML techniques on LiDAR imaging of Ohio's Hopewell earthworks. This effort is being written in a Python 3.11.9 environment.

A Convolutional Autoencoder is trained on LiDAR DEM tiles of Ohio terrain. Then a test dataset of a balance of normal terrain tiles and tiles with Hopewell earthworks is evaluated to detect Hopewell earthworks as anomalies from the reconstruction error. 

## Requirements
- Python 3.11 or equivalent
- Jupyter Notebook
- Install dependencies from requirements.txt: pip install -r requirements.txt
- All models were developed and run on a CPU. No GPU required.

## Data Source
Ohio Geographically Referenced Information Program
https://gis1.oit.ohio.gov/geodatadownload/
A list of tiles used in this study are in this repo under the tiles_and_weights folder

## Geographic Focus
- Ohio 
- UNESCO World Heritage List sites for Hopewell Ceremonial Earthworks: https://whc.unesco.org/en/list/1689/maps/

## Notebooks

Each notebook runs independently.

- 01_cae_v1.ipynb — Baseline CAE model (no output activation)
- 01_cae_v2.ipynb — CAE with TanH output activation
- 01_cae_v3.ipynb — CAE with Sigmoid output activation
- 01_cae_hpf1.ipynb — Baseline CAE with high-pass filter
- 01_cae_hpf2.ipynb — TanH CAE with high-pass filter
- 01_cae_hpf3.ipynb — Sigmoid CAE with high-pass filter

