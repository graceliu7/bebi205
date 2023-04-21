**READ ME**

All python notebooks are placed in the same parent directory as the unzipped keren/ folder. 

The read_files.ipynb notebook loads the first file in the directory, normalizes the data, segments the cells, and retrieves the labels. It then stores this information in cell_channels.npy and cell_labels.npy. These files are very large, so I didn't upload them, but they will be automatically created if the notebook is run

The model.ipynb notebook loads cell_channels.npy and cell_labels.npy. It implements a convolutional neural network and saves the trained model. It also creates a confusion matrix and saves the array as confusion_matrix.npy

The plots.ipynb notebook makes the marker expression and confusion matrix plots. It loads cell_channels.npy, cell_labels.npy, and confusion_matrix.npy and saves the plots marker_expression.png and confusion_matrix.png

The run_inference notebook implements segmentation for a random set of X and y, without labels. It also loads the trained CNN and makes predictions for the cell type of each instance, and returns this as a dictionary. 