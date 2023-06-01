# README (TO DO)
This repository contains the scripts (in jupyter notebooks) to generate the figure in the upcoming BGCFlow publication.

# USAGE
## 1. Clone this repository
```bash
git clone https://github.com/matinnuhamunada/saccharopolyspora_manuscript.git 
```

## 2. Set up BGCFlow
```bash
# create and activate new conda environment
conda create -n bgcflow pip -y
conda activate bgcflow

# install BGCFlow wrapper
pip install git+https://github.com/NBChub/bgcflow_wrapper.git

# clone BGCFlow to "bgcflow" folder
bgcflow clone bgcflow
```

## 2. Download the dataset
- TODO - make data accessible in zenodo

```bash
# move to bgcflow dir
cd bgcflow

# download and extract dataset
wget <zenodo link>
unzip saccharopolyspora_dataset.zip
```

## 3. Set configurations
```bash
# go back to the manuscript dir
cd ../saccharopolyspora_manuscript/

# edit the location of the bgcflow dir to the right directory
nano config.yaml
```

## 4. Run the notebooks
- There are two kind of notebooks, R (*.R.ipynb) and python (*.python.ipynb)
- Run the notebook using the corresponding conda environment: `python_notebook.yaml` or `r_notebook.yaml`
- Install the conda environment:
```bash
mamba env create -f python_notebook.yaml
mamba env create -f r_notebook.yaml
```
- Start jupyter session
```bash
# for python
conda activate python_notebook
jupyter lab
```
```bash
# for R
conda activate r_notebook
jupyter lab
```
- Run the notebooks in order