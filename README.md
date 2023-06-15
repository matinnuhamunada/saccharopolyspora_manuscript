# README
This repository contains the scripts (in jupyter notebooks) to generate the figure in the manuscript **"[BGCFlow: Systematic pangenome workflow for the analysis of biosynthetic gene clusters across large genomic datasets](https://doi.org/10.1101/2023.06.14.545018)"**.

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
- Donwload the dataset containing the BGCFlow runs from [Zenodo](https://doi.org/10.5281/zenodo.8018055)

```bash
# move to bgcflow dir
cd bgcflow

# download and extract dataset
wget https://zenodo.org/record/8018055/files/saccharopolyspora_dataset.zip
unzip saccharopolyspora_dataset.zip
```

## 3. Set configurations
```bash
# go back to the manuscript dir
cd ../saccharopolyspora_manuscript/

# edit the location of the bgcflow dir to the right directory
nano config.yaml
```

## 4. Setting up Conda Environments
Install these conda environments:
```bash
mamba env create -f python_notebook.yaml
mamba env create -f r_notebook.yaml
mamba env create -f <bgcflow_dir>/workflow/envs/cblaster.yaml
```

## 5. Run the notebooks
- There are two kind of notebooks, R (*.R.ipynb) and python (*.python.ipynb)
- Run the notebook using the corresponding conda environment: `python_notebook` or `r_notebook`
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

# Citation
> Matin Nuhamunada, Omkar S. Mohite, Patrick V. Phaneuf, Bernhard O. Palsson, and Tilmann Weber. (2023). BGCFlow: Systematic pangenome workflow for the analysis of biosynthetic gene clusters across large genomic datasets. bioRxiv 2023.06.14.545018; doi: [https://doi.org/10.1101/2023.06.14.545018](https://doi.org/10.1101/2023.06.14.545018)

> Nuhamunada, Matin, & Mohite, Omkar Satyavan. (2023). BGCFlow Analysis of Saccharopolyspora Genomes (0.1.0) [Data set]. Zenodo. [https://doi.org/10.5281/zenodo.8018055](https://doi.org/10.5281/zenodo.8018055
)
