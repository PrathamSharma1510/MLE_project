# DeepFakeNet: Advanced Detection of Manipulated Multimedia Content

## Introduction
DeepFakeNet is a project designed to develop a robust method for detecting and categorizing digital content altered using advanced deepfake technologies. As these technologies become more accessible and their outputs more realistic, distinguishing between authentic and manipulated media is crucial for maintaining digital trust.

## Dataset: FaceForensics++
FaceForensics++ is a comprehensive dataset used in this project, featuring one thousand video sequences manipulated using techniques like Deepfakes, Face2Face, FaceSwap, and NeuralTextures. It provides a rich source of data for developing effective detection models.

## Pipeline Overview

### Data Preprocessing
- **Video to Frame Conversion:** Converts video files into frames at a subsample rate adjustable based on project needs.
- **Face Detection and Cropping:** Utilizes MTCNN for detecting and cropping faces, resizing them to 224x224 pixels for uniformity.
- **Data Organization:** Processed faces are stored in structured directories compatible with `torchvision.datasets.ImageFolder` for efficient model training.

### Model Training
- **Model Used:** DeeperMesoInception4, an advanced model capable of identifying manipulated content.
- **Training Details:** Employs Binary Cross-Entropy Loss with the Adam optimizer. Training is conducted over multiple epochs with a set learning rate of 0.001.

## Evaluation Methodology
The model’s effectiveness is evaluated using metrics such as accuracy, F1 score, precision, and recall. The baseline comparison is made with the standard Inception model.

## Results
The DeepFakeNet model demonstrates promising results, with detailed performance metrics provided in comparison to the baseline InceptionV3 model. Here are some highlights:
- **Accuracy:** Achieved 82.08%, comparable to InceptionV3's 82.26%.
- **F1 Score:** 0.67, with the baseline at 0.85.

## Getting Started
Clone the repository: https://github.com/Vveanta/MLEproject/


## Limitations and Future Work
Despite the promising results, the limited dataset size due to storage constraints affected the model's training potential. Future enhancements could include expanding the dataset and extending the training duration for improved accuracy and reliability in detecting deepfake content.

## Conclusion
DeepFakeNet has laid a strong foundation for future developments in the field of digital media authenticity, proving effective in detecting deepfake manipulations and exceeding some aspects of the established baseline model.


