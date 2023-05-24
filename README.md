# README (TO DO)
This repository contains the scripts (in jupyter notebooks) to generate the figure in the upcoming BGCFlow publication.

# USAGE
## 1. Clone this repository

## 2. Download the dataset
- TODO - make data accessible in zenodo

## 3. Set configurations

## 4. Run the notebooks
- There are two kind of notebooks, R (*.R.ipynb) and python (*.python.ipynb)
- Run the notebook using the corresponding conda environment: `python_notebook.yaml` or `r_notebook.yaml`
- Install the conda environment:
```bash
mamba env create -f python_notebook.yaml
mamba env create -f r_notebook.yaml
```
- Start jupyter session
```
# for python
conda activate python_notebook
jupyter lab

# for R
conda activate r_notebook
jupyter lab
```
- Run the notebooks in order