# Utilizing Robust Geospatial-Temporal Machine Learning Models for Frost Classification
This repository contains machine learning models to classify frost of target locations given NASA DAV
satellite data. In this repository, we provide the code necessary to extract data from the NASA DAV API,
construct various models using the extracted data, and compare different model approaches using a customizable
cost-value matrix. Our approach in classifying forst utilizes the spatial and temporal aspects of meteorological
data to provide a more robust, generalizable, and risk-averse solution in classifying frost.

## USAGE NOTE
The code within this repository follows a logical flow in order to construct machine learning models.
BEFORE ANY MODELS ARE BUILT, RUN THE CODE IN THE DATA_EXTRACTION FOLDER.

We have also put some data files that we used for the model in the Data_Files folder. However, this folder
does not contain the combined_data.csv required for model code usage. The combined_data.csv file exceeds the
maximum size for GitHub file uploads. As such, the user is responsible for concatenating the CSV files for model
building and code usage. Alternatively, the data extraction folder contains a file that combines and exports the data.

The data leveraged by these models is obtained from the NASA DAV API. The data extraction API calling is separate from
the model building/evaluation code notebooks. With this said, ensure that you save the data to a CSV in a folder that can
be found from the rest of the code notebooks for this project.

## DATA FILES / EXTRACTION

As stated above, all data extraction should be done before running model construction code. Please run the code file in the 
Data_Extraction folder first. Additionally, some sample/non-combined files have been provided in the Data_Files folder. These can
be used for model construction, however they must be combined into a single CSV before running model code. A combined file was not
able to be uploaded due to the limited file size allowed for uploading to a GitHub Repository.

## MODELS

This repository contains multiple folders for the different models we constructed to classify frost. Folders are named based
on the model built from the code inside the folders. The repository has code folders for the following models:

Random Forests:
- Baseline RF model
- Spatial RF model (with tuning)

LSTM:
- LSTM model for temporal component of dataset

CNN + LSTM:
- CNN + LSTM multi-model approach for spatial and temporal considerations of dataset

## MISCELLANEOUS

There is one additional folder provided in this GitHub Repository, with the name PCA_Tile_Visualization. Initially, we had planned
to utilize PCA for dimension reduction of our feature space into three-dimensional vectors per instance for use in a traditional CNN. 
However, this idea was ultimately scrapped in favor of a 1-Dimensional CNN. Despite scrapping the idea, the PCA_Tile_Visualization folder
was left in the code repository since it contains some helpful visuals to provide some clarity as to how the data structures store data.
We utlized the PCA code to scale features into RGB vectors, and plotting tile information as a PNG of pixels using the scaled RGB vectors.
This provides a more clear illustration for the data structure used in the data files.
