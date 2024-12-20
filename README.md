# cryoET kaggle contest

<a target="_blank" href="https://cookiecutter-data-science.drivendata.org/">
    <img src="https://img.shields.io/badge/CCDS-Project%20template-328F97?logo=cookiecutter" />
</a>


> Use Google if needed

> Learn about Git commands: push, pull, add, commit, etc.


## Setup

1. Install `git`, `conda` and setup your `ssh` credentials in GitHub.
2. Clone this repo, and `cd` into it (use terminal)
```bash
git clone git@github.com:nveshaan/cryoET-kaggle-contest.git
cd cryoET-kaggle-contest
```
3. Create a new Conda environment
```bash
conda create --prefix ./env python=3.10
conda activate ./env
```
4. Install the packages
```bash
pip3 install torch torchvision torchaudio

conda install jupyter pandas numpy matplotlib scikit-learn tqdm

pip install napari monai zarr "numpy<2" cryoet-data-portal==4.0.0 s3fs trimesh ome-zarr scikit-image trimesh pyside2

pip install --no-deps copick>=0.6.0
pip install --no-deps git+https://github.com/copick/copick-utils.git
pip install --no-deps h5py
pip install --no-deps morphospaces
pip install --no-deps git+https://github.com/copick/copick-torch.git

pip install copick
pip install napari
pip install monai

conda install -c conda-forge pyqt
conda install -c conda-forge pyside2

# incase it doesn't work, run the below command too
pip install pyqt5-tools
```
> **WARNING!** There could be some errors in the installation steps. Please run the `test.ipynb` to check if everything is installed. If not, follow the suggestions shown in the error log. Use Google/StackOverFlow to address the issues.

> Often, the output specifies what packages are missing, just simply run the following in your terminal.
```bash
conda install -c conda-forge `missing-package-name`
```
5. If everything is installed correctly, you should be able to visualize the layers in `test.ipynb`. Run in the `env` we just created, not in `base`.
6. Note that it is a sample only, you need to download the dataset separately from Kaggle. Contact me if you need help.

## Project Organization

```
├── LICENSE            <- Open-source license if one is chosen
├── Makefile           <- Makefile with convenience commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
│
├── docs               <- A default mkdocs project; see www.mkdocs.org for details
│
├── models             <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`.
│
├── pyproject.toml     <- Project configuration file with package metadata for 
│                         cryoet_kaggle_contest and configuration for tools like black
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
├── setup.cfg          <- Configuration file for flake8
│
└── cryoet_kaggle_contest   <- Source code for use in this project.
    │
    ├── __init__.py             <- Makes cryoet_kaggle_contest a Python module
    │
    ├── config.py               <- Store useful variables and configuration
    │
    ├── dataset.py              <- Scripts to download or generate data
    │
    ├── features.py             <- Code to create features for modeling
    │
    ├── modeling                
    │   ├── __init__.py 
    │   ├── predict.py          <- Code to run model inference with trained models          
    │   └── train.py            <- Code to train models
    │
    └── plots.py                <- Code to create visualizations
```

--------

