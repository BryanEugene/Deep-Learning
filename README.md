---

# Deep Learning Project: Human Activity Recognition & Pneumonia Detection

## 📋 Table of Contents
1. [Introduction](#introduction)
2. [Datasets](#datasets)
3. [Feature Selection](#feature-selection)
4. [Model Architecture](#model-architecture)
5. [Training and Evaluation](#training-and-evaluation)
6. [Results](#results)
7. [Usage](#usage)
8. [Installation](#installation)
9. [Contributing](#contributing)
10. [License](#license)

---

## 📖 Introduction
This project focuses on two distinct tasks using deep learning techniques:
1. **Human Activity Recognition using Accelerometer Data**
2. **Pneumonia Detection using Chest X-ray Images**

The goal is to build and evaluate neural network models to achieve high accuracy for both classification problems.

## 📊 Datasets
- **Human Activity Recognition**: The dataset consists of accelerometer readings to classify human activities such as walking, sitting, and running. [Download the dataset here](https://drive.google.com/file/d/1ciwzKIPl1n7otcWQTYVX-j1k3TYmVeGL/view?usp=sharing).
- **Pneumonia Detection**: The dataset includes grayscale chest X-ray images categorized as either 'Normal' or 'Pneumonia'. [Download the dataset here](https://drive.google.com/file/d/1ciwzKIPl1n7otcWQTYVX-j1k3TYmVeGL/view?usp=sharing).

> 📥 **Note**: Please download the datasets from the provided links and place them in the respective directories.

## 🛠 Feature Selection
### Human Activity Recognition
- **Feature Extraction**: Selected 15 relevant features from accelerometer data (e.g., mean, standard deviation).
- **Feature Normalization**: All features were normalized to ensure balanced input to the model.
- **Feature Selection Method**: Utilized `SelectKBest` for selecting the most impactful features.

### Pneumonia Detection
- Used raw pixel data from grayscale chest X-ray images resized to 64x64 pixels for input.

## 🧠 Model Architecture
### Human Activity Recognition Model
- **Input**: Accelerometer data after feature selection.
- **Architecture**: 
  - 4 hidden layers starting with 512 neurons and reducing by half in each subsequent layer.
  - Output layer uses Softmax activation for multi-class classification.
- **Training**: 
  - Trained for 50 epochs using Adam optimizer.
  - Monitored accuracy and loss for both training and validation sets.

### Pneumonia Detection Model (CNN)
- **Input**: Grayscale images of size 64x64.
- **Architecture**:
  - 2 Convolutional Layers with Average Pooling.
  - Flattening followed by 3 Dense Layers (120, 84, 10 neurons).
  - Output layer with Sigmoid activation for binary classification.
- **Training**:
  - Trained for 50 epochs using Adam optimizer.

## 📈 Training and Evaluation
- **Data Splitting**:
  - Train: 80%
  - Validation: 10%
  - Test: 10%
- **Metrics**: Accuracy, Precision, Recall, F1-score.
- **Tools**: Used `scikit-learn` for evaluation metrics and `matplotlib` for visualizations.

### Human Activity Recognition
- **Training Accuracy**: 90.30%
- **Validation Accuracy**: 90.51%
- **Test Accuracy**: 90.8%
- **Test Loss**: 19.7%

### Pneumonia Detection
- **Test Accuracy**: 96.07%
- **Misclassification**: 3 out of 20 samples.

## 📊 Results
### Human Activity Recognition
- The model achieved a good balance between training and validation accuracy, indicating no overfitting.
- **Final Metrics**:
  - **Train Accuracy**: 0.9030
  - **Validation Accuracy**: 0.9051
  - **Test Accuracy**: 0.9084
  - **Test Loss**: 0.1971

### Pneumonia Detection
- The CNN model performed well with high accuracy on unseen test data.
- **Test Accuracy**: 96.07%
- The model only misclassified 3 out of 20 samples during testing.

## 🚀 Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/deep-learning-project.git
   ```
2. Navigate to the project directory:
   ```bash
   cd deep-learning-project
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the training script:
   ```bash
   python train.py
   ```

## 🛠 Installation
Make sure you have Python 3.8+ installed. Install dependencies using:
```bash
pip install -r requirements.txt
```

## 🤝 Contributing
Contributions are welcome! Please fork the repository and create a pull request for any improvements.

## 📜 License
This project is licensed under the MIT License.

---

Feel free to reach out if you have any questions or suggestions! 😊

--- 

I hope this helps! You can adjust the links and paths according to your actual project structure.
