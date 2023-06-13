# AIML Eurosat Coding Challnge

This Jupyter notebook is part of the [Eurosat Land Cover Classification](https://github.com/phelber/EuroSAT) Coding Challenge. The notebook is written in Python and uses libraries such as PyTorch, torchvision, numpy, matplotlib, seaborn, PIL, and rasterio.

Disclaimer: The code is far from good and lacks of cleanup.


## Overview

The notebook is divided into several sections:

1. **Importing Libraries**: Standard Python libraries and PyTorch deep learning library are imported. Libraries for data visualization such as matplotlib, seaborn, and PIL are also imported.

2. **Loading Data**: The data is loaded from a specified drive path or downloaded from a source URL. The data is then unzipped and moved to a specified directory.

3. **Setup**: Random seeds are set for reproducibility. Dictionaries are created to map class names to their respective numerical labels and vice versa.

4. **Dataloader**: Custom dataloader is defined to load and preprocess the data from the given directories.

5. **Transformations**: Standard preprocessing steps are applied to the data to increase the performance of the model and reduce overfitting.

6. **Defining the Model**: A model architecture based on the ResNet34 network is created. The model is then slightly modified to better suit the task at hand.

## Usage

To use this notebook, you need to have Python installed along with the libraries mentioned above. You can run the notebook cell by cell to understand how each part of the code works. Make sure to update the paths to the data files as per your local setup.
Or use [Google Colab](https://colab.research.google.com/) and skip [Installation](#run-it-local) (recommended)

### Run it local

```bash
#Create a new venv (here with conda)
conda create -n eurosat

#activate your new environment
conda activate eurosat

#install the required libraries
pip install -r requirements.txt

#start the notebook
jupyter euro_sat_classification.ipynb
```

## Data

The data used in this notebook is from the [Eurosat dataset](https://github.com/phelber/EuroSAT). It is a dataset of satellite images labeled with different classes such as 'AnnualCrop', 'Forest', 'HerbaceousVegetation', 'Highway', 'Industrial', 'Pasture', 'PermanentCrop', 'Residential', 'River', and 'SeaLake'. The data is loaded from a specified drive path or downloaded from a source URL.

## Model

The model used in this notebook is based on the ResNet34 architecture. The model is slightly modified to suit the task at hand. The final fully connected layer is adapted to predict which of the 10 classes the input image belongs to. The first convolutional layer is modified to accept 11 input channels instead of the original 3.

## Note

This notebook is a part of a coding challenge and is meant for educational purposes. It is always recommended to understand the code and the problem statement before using the notebook for your purposes.

## License

This project is licensed under the terms of the MIT License. This means that you are free to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the software, provided that you include the following copyright notice and permission notice in all copies or substantial portions of the software.

