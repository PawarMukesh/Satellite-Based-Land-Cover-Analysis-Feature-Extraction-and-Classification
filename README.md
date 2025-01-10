# Satellite-Based Land Cover Analysis: Feature Extraction and Classification

Accurate land cover classification helps stakeholders understand land usage patterns, assess environmental changes, and make informed decisions in areas like agriculture, urban development, and disaster management.

## BUSINESS CASE
Accurate land cover classification helps stakeholders understand land usage patterns, assess environmental changes, and make informed decisions in areas like agriculture, urban development, and disaster management. This classification can support environmental monitoring, urban planning, and resource management.

## GOAL OF THE PROJECT
The project aims to extract the features from images and classify different types of land cover (e.g., urban, agriculture, forest, water) from satellite images.

### TASK: Multiclass Classification

## DATA SUMMARY:
* Dataset Name: EuroSAT Land Cover Classification Dataset
* Data Source: Zenodo EuroSAT Dataset
* Data Type: Satellite Imagery
* Data Format:
  1. RGB Images: .jpg (for 10 land cover classes)
  2. Multispectral Images: .tif (for the same 10 land cover classes)
  3. Number of Classes: 10
[AnnualCrop, Forest, HerbaceousVegetation, Highway, Industrial, Pasture, PermanentCrop, Residential, River SeaLake]
* Total Number of Samples: Approximately 27,000 images (3,000 images per class)

## STEPS & METHODOLOGY 

### 1. Prepare Training, Validation, and Testing Sets
* Divide the dataset into three subsets:
  1. Training Set: Used to train the model.
  2. Validation Set: Used to tune model hyperparameters and prevent overfitting.
  3. Testing Set: Used for final evaluation of model performance.
* Data Augmentation: Apply transformations such as rotation, flipping, scaling, and brightness adjustments to increase dataset diversity.

### 2. Get All Class Labels
Extract and list all unique class labels from the dataset to ensure the model correctly maps images to their respective classes.

### 3. Visualize the Training Images
![image](https://github.com/user-attachments/assets/95a0f11e-b6fe-4503-aa69-59ef57cef17d)
* Display images with their corresponding class labels for better understanding and validation of the dataset.

### 4. Create DCNN and Use VGG19 Model
* Deep Convolutional Neural Network (DCNN): Design a custom DCNN architecture.
* VGG19 Model: Integrate the pretrained VGG19 model for feature extraction or fine-tuning. Use it as the backbone for the classification task.

### 5. Model Compilation
* Compile the model with appropriate loss functions, optimizers, and evaluation metrics.
  1. Loss Function: categorical_crossentropy for multi-class classification.
  2. Optimizer: Adam or SGD.
  3. Metrics: accuracy.

### 6. Model Training
* Train the model using the training set and validate on the validation set.
* Monitor metrics such as loss and accuracy during training.
* Implement early stopping or learning rate schedulers to optimize training.

### 7. Model Evaluation
* Evaluate the trained model on the testing set.
* Calculate metrics such as:
  1. Accuracy: 88.5%
  2. Precision: 87.2%
  3. Recall: 86.8%
  4. F1-Score: 87.0%
* Plot confusion matrix for detailed analysis.
![image](https://github.com/user-attachments/assets/3c4eff11-0c34-41ad-bf07-28976376e711)


### 8. Model Saving
* Save the trained model for future use using formats like .h5 or TensorFlow's SavedModel format.
* Save training metadata, including class labels and preprocessing details.

### 9. Prediction on Test Data
* Use the saved model to make predictions on unseen test data.
* Visualize predictions alongside ground truth labels for validation.
![image](https://github.com/user-attachments/assets/0ce81445-4a9c-4504-9ec6-5b92e0039752)
![image](https://github.com/user-attachments/assets/4e254deb-9119-43e0-8c38-39e637f76738)




## Tools and Technologies
* Programming Language: Python
* Frameworks and Libraries:
  1. TensorFlow/Keras
  2. NumPy
  3. Pandas
  4. Matplotlib/Seaborn
  5. OpenCV
  6. scikit-learn

* Hardware Requirements: GPU-enabled machine for faster training.

## Project Workflow
* Data Preparation and Augmentation
* Model Design (DCNN + VGG19)
* Training and Validation
* Evaluation and Analysis
* Model Deployment



