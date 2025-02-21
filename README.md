# Object Localization using TensorFlow

## Overview
This project focuses on **Object Localization**, where a deep learning model is trained to classify objects and predict their bounding box coordinates within an image. Unlike full object detection models that handle multiple objects per image, this project assumes **one object per image**, requiring both classification and localization.

The model is built using **TensorFlow** and **Keras** and utilizes a **multi-output CNN (Convolutional Neural Network)** with separate branches for object classification and bounding box regression.

## Key Features
- **Multi-output CNN** for simultaneous object classification and localization.
- **Custom Intersection over Union (IoU) metric** to evaluate bounding box accuracy.
- **Custom data generator** to efficiently process images and labels.
- **Learning rate scheduling and early stopping** to optimize training.
- **Visualization of predictions** with bounding boxes drawn on images.

## Dataset
This project uses **synthetically generated images** for training. Each image contains a single object placed at a random position, and the model is trained to predict both its class and location.

## Installation

1. **Clone the repository**:
   ```bash
   git clone 'https://github.com/rishikam23/Object-Localization-using-Tensorflow'
   cd object-localization-tensorflow
   ```
2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## Usage
- Modify data_generator() in data_loader.py to customize synthetic image generation.
- Adjust model architecture in model.py.
- Train the model using train.py.
- Evaluate and visualize predictions using evaluate.py.

## Model Architecture
The CNN consists of:
1. Feature extraction layers (convolutional layers).
2. Two output branches:
     - Classification output: Uses softmax activation for multi-class classification.
     - Bounding box output: Uses linear activation to predict coordinates.
       
## Evaluation
The model is evaluated using accuracy for classification and IoU (Intersection over Union) for localization.

## Results
After training, the model achieves:
- High accuracy in classifying objects.
- Precise bounding box localization with high IoU scores.

## Contributing
Contributions are welcome! Feel free to fork the repository, submit issues, or create pull requests.

## License
This project is open-source and available under the MIT License.
