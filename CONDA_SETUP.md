# EDA with Gemini - Conda Environment Setup

**WARNING:** These setup instructions assume a certain familiarity with Python and virtual environments, If in doubt, please 
**ask for expert help** before potentially damaging your Python configuration ([don't let this be you](https://imgs.xkcd.com/comics/python_environment.png)). 


This repository contains a Jupyter notebook for Exploratory Data Analysis (EDA) using AI assistants. 

Follow the instructions below to set up the required conda environment (called eda_ia).

## Prerequisites

Make sure you have conda or miniconda installed on your system. If not, download it from:

- [Miniconda](https://docs.conda.io/en/latest/miniconda.html) (recommended)

- [Anaconda](https://www.anaconda.com/products/distribution)

## Environment Setup

### 1. Create the conda environment

Navigate to the project directory and run:

```bash
conda env create -f EDA_IA_conda_environment.yml
```

This will create a new conda environment called `eda_ia` with all the required packages.



### 2. Use the environment with VS Code

+ The following assumes that you have installed VS Code, that you can access GitHub Copilot with it (see the slides of the session for more setup info).  

+ Open VS Code and load the EDA_with_copilot.ipynb notebook.

+ In the top right corner you will see a *Select Kernel* button. Cilck on it and select your `eda_ia` environment. Now you can run the notebook cells. 


### 3. Using Jupyter Notebook (or Lab)

+ Open a Terminal (Anaconda terminal recommended in Windows)

+ Activate the environment executing

```bash
conda activate eda_ia
```

+ Launch Jupyter

```bash
jupyter notebook
```

it will open in your default browser and then open the `EDA_with_gemini_V1.ipynb` file in your browser.

### Deactivating the Environment

When you're done working close Jupyter in the browser and in the terminal type:

```bash
conda deactivate
```

## 4. Removing or exporting the environment

To completely remove the environment after this session:

```bash
conda env remove -n eda_ia
```

To export your current environment (if you make changes):

```bash
conda env export > environment.yml
```




