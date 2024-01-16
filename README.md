# federated_learning_with_ZEPHYR

## Overview
This notebook demonstrates the implementation of federated learning for heart rate prediction using TensorFlow Federated (TFF). Federated learning is a machine learning approach where the model is trained across multiple decentralized devices or servers, ensuring privacy and security of sensitive data.

## Dataset
The dataset used in this notebook should be placed in the "dataset" folder within the same directory as this notebook. The dataset should follow the structure of individual participant folders (e.g., P01, P02) containing ZEPHYR subfolders with Summary.csv files. Each Summary.csv file should represent a participant's heart rate data.

Note: Please obtain the dataset and place it in the "dataset" folder before running the notebook.
You can download the dataset from this link: https://zenodo.org/records/6420886/files/dataset.zip?download=1
You can view the dataset structure from this page: https://zenodo.org/records/6420886

## Requirements
Ensure you have the required Python libraries installed by running the following command:

```bash
pip install -r requirements.txt
```
## Notebook Structure
1. Data Preparation:
The notebook starts by collecting paths to Summary.csv files within the "dataset" folder, excluding any unwanted files.
The dataset is preprocessed using a StandardScaler, and the processed data is stored in a federated format.

2. Federated Learning Model:
A simple feedforward neural network model is defined using TensorFlow and converted into a TFF model.
The federated averaging algorithm is used for training, and the model is trained on the collected federated datasets.

3. Model Saving:
The trained model weights and the StandardScaler object are saved using joblib for future use.

4. Model Evaluation:
The saved model and scaler are loaded.
A new test dataset is preprocessed and converted into a federated format.
The federated evaluation is performed on the test dataset.

## Usage
1. Dataset Preparation:
Place your heart rate dataset in the "dataset" folder.

2. Install Requirements:
Run the command pip install -r requirements.txt to install the necessary libraries.

3. Run the Notebook:
Execute the notebook cells to perform federated learning on the heart rate dataset.

4. Evaluate the Model:
After training, the model is evaluated on a test dataset.

5. Further Customization:
Adjust hyperparameters, model architecture, or dataset processing based on your specific requirements.

## Author
Stefano Carobene