This folder contains the random forests used for frost classification.
The notebook contains code for a few different models, including the baseline random forest,
the random forest + spatial function with a default lambda value (0.5),
and tuned random forest + spatial functions.

The code notebook also contains a function that can be used to evaluate the cost or value of a given model.
This function can be tuned to change how the cost or value of a given model is computed based on user goals.

NOTE: This file requires a CSV of data in a valid format to be passed. Valid format is a CSV file that contains
city names, latitude and longitudes, neighbor numbers, and features/response for the given problem. Please see
the files in the data folder for an example, or run the Data_Extraction code notebook before running the code here.