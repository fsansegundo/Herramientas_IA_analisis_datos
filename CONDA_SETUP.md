# EDA with Gemini - Conda Environment Setup

This repository contains a Jupyter notebook for Exploratory Data Analysis (EDA) using AI assistants. Follow the instructions below to set up the required conda environment.

## Prerequisites

Make sure you have conda or miniconda installed on your system. If not, download it from:
- [Miniconda](https://docs.conda.io/en/latest/miniconda.html) (recommended, lightweight)
- [Anaconda](https://www.anaconda.com/products/distribution) (full distribution)

## Environment Setup

### 1. Create the conda environment

Navigate to the project directory and run:

```bash
conda env create -f environment.yml
```

This will create a new conda environment called `eda_ia` with all the required packages.

### 2. Activate the environment

```bash
conda activate eda_ia
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

Then open the `EDA_with_gemini_V1.ipynb` file in your browser.

## Alternative Setup Methods

### Option 1: Create environment manually

If you prefer to create the environment step by step:

```bash
# Create a new environment with Python 3.9
conda create -n eda_ia python=3.9

# Activate the environment
conda activate eda_ia

# Install core packages
conda install -c conda-forge pandas numpy matplotlib seaborn statsmodels jupyter ipykernel notebook wget missingno

# Install PDF generation packages via pip
pip install markdown2 weasyprint cffi cairocffi pycparser
```

### Option 2: Using mamba (faster alternative)

If you have mamba installed (faster conda alternative):

```bash
mamba env create -f environment.yml
mamba activate eda_ia
```

## Package Dependencies

The environment includes the following key packages:

- **pandas**: Data manipulation and analysis
- **numpy**: Numerical computing
- **matplotlib**: Data visualization
- **seaborn**: Statistical data visualization
- **statsmodels**: Statistical modeling and time series analysis
- **missingno**: Missing data visualization
- **jupyter**: Jupyter notebook support
- **wget**: Data downloading utility
- **markdown2**: Markdown to HTML conversion
- **weasyprint**: HTML to PDF conversion

## Troubleshooting

### Issue: WeasyPrint installation problems

WeasyPrint requires additional system dependencies. If you encounter issues:

**On macOS:**
```bash
brew install cairo pango gdk-pixbuf libffi
```

**On Ubuntu/Debian:**
```bash
sudo apt-get install build-essential python3-dev python3-pip python3-setuptools python3-wheel python3-cffi libcairo2 libpango-1.0-0 libpangocairo-1.0-0 libgdk-pixbuf2.0-0 libffi-dev shared-mime-info
```

**On Windows:**
Use the conda-forge channel or consider using an alternative PDF generation library.

### Issue: Jupyter kernel not found

If the Jupyter kernel is not available:

```bash
conda activate eda_ia
python -m ipykernel install --user --name eda_ia --display-name "Python (EDA Gemini)"
```

## Deactivating the Environment

When you're done working:

```bash
conda deactivate
```

## Removing the Environment

To completely remove the environment:

```bash
conda env remove -n eda_ia
```

## Environment Export

To export your current environment (if you make changes):

```bash
conda env export > environment.yml
```

## Notes

- The notebook uses shell commands (`!wget`, `!mkdir`, `!unzip`) which work on Unix-like systems (macOS, Linux). On Windows, you might need to adapt these commands or use alternative methods.
- The environment is optimized for the specific packages used in the notebook. Additional packages can be installed as needed using `conda install` or `pip install` after activating the environment.
