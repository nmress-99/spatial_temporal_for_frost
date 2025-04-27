# spatial_temporal_for_frost
Repository for spatial and temporal machine learning models used for frost classification.

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
