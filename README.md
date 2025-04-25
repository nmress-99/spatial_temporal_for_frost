# spatial_temporal_for_frost
Repository for spatial and temporal machine learning models used for frost classification.

## USAGE NOTE
The code within this repository follows a logical flow in order to construct machine learning models.
BEFORE ANY MODELS ARE BUILT, RUN THE CODE IN THE DATA_EXTRACTION FOLDER.

The data leveraged by these models is obtained from the NASA DAV API. The data extraction API calling is separate from
the model building/evaluation code notebooks. With this said, ensure that you save the data to a CSV in a folder that can
be found from the rest of the code notebooks for this project.
