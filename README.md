# Deep neural network for classification and QSAR

This is a cascaded DNN model in which a classifier classifies unknown chemical library into actives and inactive compounds and in the next step regressor predict the pIC50 values of these classified active compounds. Pubchem fingerprints are used to generate classifier while extended fingerprints are used to generate regressor.

## training_data

This folder contains the files `pubchem.xlsx` and `exdfp_renin.csv`. The header file includes the input data for classifier and the other file includes the input data for regressor. This data is used to train and test the models.

The code for classifier is provided in the `classifier.ipynb` file.

The code for regressor is provided in the `regressor.ipynb` file.

## library_to_screen

This folder contains the files `pubchem_maybridge.csv` and `exdfp_maybridge.csv`.

- `pubchem_maybridge.csv` is used as an input (unknown dataset) to classifier. It will give an output file of classified hits named as `output_hits.csv`. This `output_hits.csv` file is an input for regressor.

- `exdfp_maybridge.csv` is used as an input (unknown dataset) to regressor. It will give an output of list of compounds with their respective pIC50 values.
