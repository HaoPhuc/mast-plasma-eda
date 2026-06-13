PURPOSE: This project is an Exploratory Data Analysis (EDA) of experimental plasma data from the FAIR-MAST database — a publicly available dataset of 11,573 shots from the Mega Ampere Spherical Tokamak (UK).

GOAL: 
1. The main goal of this project is to understand and clean the data, then train a simple linear(or/and logistics) regression model.
2. The model is implemented from scratch using NumPy to demonstrate understanding of the underlying mathematics rather than relying on sklearn.

Packages:
Besides matplotlib and scipy, which I was introduced to at TU/e, I had to import some other new (to me) packages:
1. xarray: multi-dimensional labelled arrays for MAST time-series data
2. pyarrow: reading .parquet files (MAST shots metadata)
3. zarr: file format for MAST time-series storage
4. aiohttp: async HTTP, required by xarray to stream remote data
5. requests: HTTP library for basic web requests
6. seaborn: statistical plotting built on top of matplotlib


NOTE: This project is the first in a series — future extensions will apply more complex models as my ML knowledge develops.
