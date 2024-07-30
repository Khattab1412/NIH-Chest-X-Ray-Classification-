# NIH-Chest-X-Ray-Classification-
Classification and Localization of Thoracic Diseases

# Dataset
The ChestX-ray14 dataset consists of 112,120 frontal chest X-ray images from 30,805 unique patients, annotated with 14 disease labels. To ensure rigorous evaluation, we divided the dataset into training (70%), validation (10%), and test (20%) sets based on patient IDs, preventing any overlap between these subsets.

# Usage
1. Clone Repository: Clone this repository using Git.
2. Download Data: Download the ChestX-ray14 dataset from Kaggle:
 https://www.kaggle.com/datasets/nih-chest-xrays/data
3. Verify Paths: Ensure all file paths in the code point to the downloaded data directory.
4. Specify GPUs (Optional): If using multiple GPUs for training, specify the desired GPU IDs in the code.
# Data Preparation:
  - Split the dataset into training (70%), validation (10%), and testing (20%) subsets, ensuring no overlap between them.
  - Standardize the data using the mean and standard deviation of ImageNet.
# Model Development:
  - Create a DenseNet121 model pre-trained with Keras.
  - Employ the Adam optimizer with an initial learning rate of 1e-3, decaying by a factor of 10 every 2 epochs.
  - Save the model with the lowest validation loss during training.
# Evaluation:
  - Evaluate the performance of the saved model on the test dataset.
# Comparsion
- Wang et al.: 0.7381
-  Yao et al.: 0.8027
-  CheXNet: 0.8414
-  Ours: 0.8454 and
-  Our Micro-Average ROC AUC Score: 0.8878


| Pathology          | [Wang et al.](https://arxiv.org/abs/1705.02315) | [Yao et al.](https://arxiv.org/abs/1710.10501) | [CheXNet](https://arxiv.org/abs/1711.05225) | Ours                     |
|--------------------|-------------|------------|---------|--------------------------|
| Atelectasis        | 0.716       | 0.772      | 0.8094  | 0.8237                   |
| Cardiomegaly       | 0.807       | 0.904      | 0.9248  | 0.9135                   |
| Effusion           | 0.784       | 0.859      | 0.8638  | 0.8888                   |
| Infiltration       | 0.609       | 0.695      | 0.7345  | 0.7169                   |
| Mass               | 0.706       | 0.792      | 0.8676  | 0.8608                   |
| Nodule             | 0.671       | 0.717      | 0.7802  | 0.7757                   |
| Pneumonia          | 0.633       | 0.713      | 0.7680  | 0.7705                   |
| Pneumothorax       | 0.806       | 0.841      | 0.8887  | 0.8963                   |
| Consolidation      | 0.708       | 0.788      | 0.7901  | 0.8130                   |
| Edema              | 0.835       | 0.882      | 0.8878  | 0.8932                   |
| Emphysema          | 0.815       | 0.829      | 0.9371  | 0.9242                   |
| Fibrosis           | 0.769       | 0.767      | 0.8047  | 0.8182                   |
| Pleural Thickening | 0.708       | 0.765      | 0.8062  | 0.7974                   |
| Hernia             | 0.767       | 0.914      | 0.9164  | 0.9436                   |


