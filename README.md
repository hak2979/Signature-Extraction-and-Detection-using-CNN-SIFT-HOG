# Signature Extraction and Detection using CNN, SIFT, and HOG

## Overview
This project focuses on extracting and detecting handwritten signatures from unscanned and noisy images using image processing techniques. The processed images are then used to train different machine learning models—Convolutional Neural Networks (CNN), Histogram of Oriented Gradients (HOG), and Scale-Invariant Feature Transform (SIFT). The efficiency and accuracy of these models are compared to determine the most effective approach for signature detection.

## Methodology
### 1. Image Processing
The first step is to preprocess the images to remove noise and extract signature data. This involves:
- **Scanning the Image:** Using OpenCV, the images are thresholded with enhanced brightness and contrast to improve clarity.
- **Noise Removal and Binary Image Creation:** Morphological operations and adaptive thresholding are applied to remove noise and create a binary image.
- **Detecting Horizontal and Vertical Contours:** Small contours are discarded as noise, and the remaining contours are used to locate the cell containing the signature.
- **Extracting Signature Data:** The extracted columns are organized into folders where the first column (text) becomes the folder name, and the subsequent columns contain signature image data.

### 2. Model Development
Three different models were implemented for signature detection:
- **CNN (Convolutional Neural Network)**
- **HOG (Histogram of Oriented Gradients)**
- **SIFT (Scale-Invariant Feature Transform)**

### 3. Model Training and Testing
After image processing, the dataset was split, and each model was trained and tested on the processed images.

## Results
The models were evaluated based on their accuracy:
- **CNN Accuracy:** 65.0%
- **HOG Accuracy:** 30.0%
- **SIFT Accuracy:** 5.0%

### Conclusion
For the same model complexity and hyperparameters, CNN and HOG performed significantly better than SIFT. Among them, CNN slightly outperformed HOG in most cases, making it the preferred model for signature detection.

## Installation & Usage
### Prerequisites
Ensure you have the following dependencies installed:
```bash
pip install opencv-python numpy tensorflow keras scikit-image
```

### Execution Steps
1. **Run Image Processing:**
   Open and run `Image_Processing.ipynb`
2. **Split Dataset:**
   Open and run `DataSet_Split.ipynb`
3. **Train Model:**
   Open and run `Train_proc.ipynb`
