# Food Image Classification

## Project Overview
- Built a deep learning image classifier to recognise three food categories: Bread, Soup and Vegetable-Fruit
- Implemented a full workflow including image loading, resizing, normalisation and one-hot label encoding for multi-class classification
- Trained and iterated on multiple Convolutional Neural Network (CNN) architectures, improving generalisation through dropout regularisation and architectural tuning to reduce overfitting 

## Code and Resources
Python Version: 3.10

Packages: pandas, numpy, matplotlib, seaborn, opencv-python, scikit-learn, tensorflow

Python Requirements: pip install -r requirements.txt

## Dataset
Source: MIT Professional Education

Type: Image dataset stored as .img files

The dataset consists of food images organised into three distinct categories:
- Bread
- Soup
- Vegetable-Fruit

Images are stored in separate directories per category. Each file is loaded programmatically for preprocessing and model training.

## Data Preprocessing
The image dataset was split into separate directories for training and testing, with a 25% test size. Afterwards the dataset was perpared into a consistent numerical format suitable for CNN training. The following preprocessing steps were applied to both directories:
- Loaded .img files from class-based directory folders and assigned labels accordingly
- Resized all images to 150 x 150 pixels to ensure consistent inout dimensions
- Converted images into NumPy arrays for efficient tensor processing
- Normalised pixel values from 0-255 to 0-1 to improve training stability
- Applied one-hot encoding to class labels for multi-class classification
- Shuffled the dataset to reduce ordering bias prior to model training

The dataset exhibits class imbalance, with Soup representing the largest proportion of images (45%). To get a better understanding of the distribution and characteristics of the data a small number of random data images were visualised.
  
## Model Building
Multiple CNNs were developed iteratively to improve performance.

- Baseline CNN (Model 1)
  - Implemented sequential convolution and max-pooling layers followed by fully connected dense layers
  - This served as the initial benchmark to assess baseline separability across the three food classes
- Tuned CNN (Model 2)
  - Increased convolutional filter capacity in earlier layers to enhance feature extraction
  - Dropout regularisation was introduced to reduce overfitting observed in the baseline model
- Regularised CNN (Model 3)
  - Further increased dropout regularisation to improve generalisation performance and stabilise validation loss
  - This model achieved the strongest balance between bias and variance

All models:
- Used ReLU activation for hidden layers
- Applied Softmax activation in the output layer for three-class classification
- Optimised using categorical cross-entropy loss
- Were trained and evaluated on the predefined training and test sets

## Model Performance
Models were evaluated using Accuracy, Precision, Recall and F1 Score metrics, with particular attention to per-class performace due to dataset imbalance. The models attained accuracies of:
- Model 1: 65.8%
- Model 2: 72.2%
- Model 3: 77.97%

Model 3 achieved the highest overall test accuracy and demonstrated improved generalisation compared to earlier iterations. The detailed classification performance:
- Class-level results:
  - Bread: Precision 0.68 | Recall 0.75 | F1 Score 0.71
  - Soup: Precision 0.81 | Recall 0.82 | F1-score 0.82
  - Vegetable-Fruit: Precision 0.93 | Recall 0.73 | F1-score 0.82
- Overall Accuracy: 78%
- Weighted F1 Score: 0.78 

Performance reflects strong classification capability for the majority class (Soup) and high precision for Vegetable-Fruit, with some recall limitations influenced by class imbalance.

## Project Evaluation
- 
