# ML Image Detection Project

## Developers

-   Kiarash Grayeli
-   Parham Baradaran Noveiry
-   Paria Salsablily


## Overview

This project focuses on **machine learning-based image detection**, specifically face detection, feature extraction, and shape prediction. The goal is to process and analyze images to extract detailed descriptors of human faces for applications like recognition, verification, or analysis.

## Key Features

1. **Face Detection**:
   - Utilizes a Deep Neural Network (DNN) model to detect faces in images.

2. **Shape Prediction**:
   - Employs a face landmark model to predict key points on detected faces, such as eyes, nose, and mouth.

3. **Feature Extraction**:
   - Leverages a ResNet-based model to extract detailed face descriptors, capturing the unique shape and features of each individual.

## Data Management

- **Database**:
  - Processed and trained images are stored in a pickle model file for efficient access and usage during detection and analysis.

## Training

### Train-Test Split:
- **Training Rate**: 80%
- **Test Rate**: 20%

### Models Used:
1. **Logistic Regression**
2. **Support Vector Classifier (SVC)**
3. **Random Forest Classifier**
4. **Voting Classifier** (ensemble of the above models)

### Voting Classifier:
- The Voting Classifier combines the predictions of the individual models using specific weightage:
  - **Logistic Regression**: Weight = 2
  - **SVC**: Weight = 3
  - **Random Forest**: Weight = 1
- This method enhances the overall accuracy by estimating the importance of each model in the ensemble.

### Install Requiments
```bash
pip install -r requirements.txt
```
### Start Project
```bash
python manage.py runserver
```
## Usage
By running the Django project and uploading your image, this application identifies the similarity between you and a celebrity with a probability percentage.

## Note
Due to the large size of the celebrity dataset, only a sample of it has been trained. Naturally, increasing the dataset will improve the model's accuracy.
