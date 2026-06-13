PURPOSE: This project is an Exploratory Data Analysis (EDA) of experimental plasma data from the FAIR-MAST database — a publicly available dataset of 11,573 shots from the Mega Ampere Spherical Tokamak (UK).

GOAL:
1. Understand and clean the data, then train a simple linear regression model to predict total ohmic heating energy from plasma parameters.
2. The model is implemented from scratch using NumPy to demonstrate understanding of the underlying mathematics rather than relying on sklearn.

NOTE: This project is the first in a series — future extensions will apply more complex models as my ML knowledge develops.

---

PACKAGES:
Besides numpy, matplotlib, scipy and pandas, which I was introduced to at TU/e, I had to import some new packages:
1. xarray — multi-dimensional labelled arrays for MAST time-series data
2. pyarrow — reading .parquet files (MAST shots metadata)
3. zarr — file format for MAST time-series storage
4. aiohttp — async HTTP, required by xarray to stream remote data
5. requests — HTTP library for basic web requests
6. seaborn — statistical plotting built on top of matplotlib

---

COLUMN SELECTION:
Out of 189 available columns, 15 were selected based on:
- Documentation from the FAIR-MAST CPF tutorial (mastapp.site/cpf_data.html)
- Physical relevance to plasma confinement and energy
- Column naming conventions

Full column documentation is not yet available for all 189 parameters 
as FAIR-MAST is a recently released database. A detailed breakdown of 
selected columns is provided in the notebook.
