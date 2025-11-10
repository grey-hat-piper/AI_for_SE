# AI for Software Engineering

This repository contains an assignment exploring the intersection of Artificial Intelligence and Software Engineering. The project combines theoretical analysis, ethical considerations, and practical implementation of AI techniques in software development contexts.

## Project Overview

The assignment covers three main areas:

1. **Theoretical Analysis** - Examination of AI-driven code generation tools, machine learning approaches for bug detection, and bias mitigation in user experience personalization
2. **Ethical Reflection** - Analysis of biases in AI models, particularly in medical imaging for breast cancer classification, and strategies for mitigation using fairness tools
3. **Practical Implementation** - A breast cancer tumor classification model using CNN feature extraction and Random Forest classification

## Contents

### Files
- `theory.md` - Theoretical analysis covering AI in software engineering topics
- `ethical_reflection.md` - Ethical considerations and bias mitigation strategies
- `breast_cancer_tumor_predict/breast_cancer.ipynb` - Jupyter notebook implementing the breast cancer classification model
- `breast_cancer_tumor_predict/training_set/` - Dataset containing benign and malignant tumor images

### Key Topics Covered

#### Theoretical Analysis (`theory.md`)
- AI-driven code generation tools (e.g., GitHub Copilot) and their limitations
- Supervised vs unsupervised learning for automated bug detection
- Bias mitigation in AI for user experience personalization
- AIOps in DevOps for automating deployment pipelines

#### Ethical Reflection (`ethical_reflection.md`)
- Potential biases in medical imaging datasets
- Sampling bias and representation issues
- Using IBM AI Fairness 360 toolkit for bias detection and mitigation
- Ensuring fairness in healthcare AI applications

#### Practical Implementation (`breast_cancer.ipynb`)
- CNN-based feature extraction from medical images
- Random Forest classification for tumor type prediction
- Model evaluation using accuracy, F1-score, and classification reports
- Data preprocessing and augmentation techniques

## Installation and Setup

### Prerequisites
- Python 3.7+
- TensorFlow 2.x
- scikit-learn
- OpenCV
- NumPy
- Jupyter Notebook

### Installation
```bash
# Clone the repository
git clone https://github.com/grey-hat-piper/AI_for_SE.git
cd AI_for_SE

# Install required packages
pip install tensorflow scikit-learn opencv-python numpy jupyter
```

## Usage

### Running the Breast Cancer Classification Model
1. Navigate to the project directory
2. Open the Jupyter notebook:
   ```bash
   jupyter notebook breast_cancer_tumor_predict/breast_cancer.ipynb
   ```
3. Run all cells to train and evaluate the model

The model will:
- Load and preprocess breast cancer tumor images
- Extract features using a CNN architecture
- Train a Random Forest classifier
- Evaluate performance on a validation set

## Model Architecture

The breast cancer classification system uses a two-stage approach:

1. **Feature Extraction**: A Convolutional Neural Network (CNN) with multiple convolutional and pooling layers extracts relevant features from input images
2. **Classification**: A Random Forest classifier uses the extracted features to predict whether tumors are benign or malignant

### CNN Feature Extractor
- Input: 224x224 RGB images
- Layers: Conv2D → MaxPooling → Conv2D → MaxPooling → Conv2D → MaxPooling → Conv2D → MaxPooling → Flatten → Dense → Dropout
- Output: 512-dimensional feature vectors

### Random Forest Classifier
- 100 decision trees
- Trained on extracted CNN features
- Binary classification (benign vs malignant)

## Evaluation Metrics

The model is evaluated using:
- **Accuracy**: Overall correct predictions
- **F1-Score**: Harmonic mean of precision and recall
- **Classification Report**: Detailed metrics per class

## Ethical Considerations

This project addresses important ethical issues in AI:
- **Bias Detection**: Identifying potential biases in medical datasets
- **Fairness Tools**: Using IBM AI Fairness 360 for bias mitigation
- **Healthcare Equity**: Ensuring AI models don't perpetuate healthcare disparities

## Contributing

This is an academic assignment repository. For questions or discussions about the content, please refer to the theoretical analysis and ethical reflection documents.

## License

This project is for educational purposes as part of an AI for Software Engineering course.
