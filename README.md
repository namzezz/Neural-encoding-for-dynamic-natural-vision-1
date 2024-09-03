# NeuroVision

## Overview

**NeuroVision** is a project that explores the intricate relationship between intracranial electroencephalography (iEEG) data and visual stimuli, aiming to predict visual experiences based on brain activity. By leveraging Convolutional Neural Networks (CNNs), the project seeks to decode neural responses to external stimuli, contributing to the broader field of brain-computer interfaces.

## Features

- **Data Preprocessing**: Preprocessing of iEEG data and visual stimuli images for model training.
- **Temporal Segmentation**: Segmentation of iEEG data based on stimulus durations.
- **Data Pairing**: Associating iEEG segments with corresponding visual stimuli.
- **Model Training**: Training a CNN model to reconstruct visual stimuli from iEEG data.
- **Evaluation**: Assessing the model's performance using visual similarity metrics and Grey Level Co-occurrence Matrix (GLCM) analysis.

## Methodology

### Data Preprocessing

- **Initial Image Data**: Extracted and resized to 224×224 pixels.
- **Temporal Segmentation**: Segments of iEEG data aligned with visual stimuli using a 2-second window.
- **Data Pairing**: Each iEEG segment is paired with its corresponding visual stimulus, creating a 224×224×36 array.

### Dataset

- **Source**: The dataset used for this project is available at [OpenNeuro](https://openneuro.org/datasets/ds004194/versions/1.0.1).
- **Structure**: The dataset includes various files related to spatial and temporal pattern tasks, along with metadata and iEEG data.

### Model

- **Architecture**: A Convolutional Neural Network (CNN) is utilized to decode visual stimuli from iEEG data.
- **Evaluation**: The model achieved a similarity score of 0.307 on a scale of -1 to 1, indicating moderate success in reconstructing visual stimuli.

## Results

- **Visual Similarity**: The model was moderately successful in reconstructing images from iEEG data.
- **GLCM Analysis**: Provided quantitative insights into the texture and spatial relationships of the original and reconstructed images.

## Challenges

1. **Variable Duration and Aggregate Stimuli**: Difficulties in handling variable stimulus durations and aggregating consecutive stimuli.
2. **Group Size and Segmenting iEEG Data**: Challenges in determining optimal group size and segmenting data.
3. **Composite Visual Stimuli**: Issues in creating effective composite representations of visual stimuli.

## Conclusion

The project makes significant strides in decoding visual stimuli from iEEG data, despite the challenges faced. The achieved results provide valuable insights, and the work sets the stage for future explorations in brain-computer interfaces and neuroscience.

## Installation

### Prerequisites

- Python 3.x
- TensorFlow/Keras
- Jupyter Notebook
- Required Python libraries (listed in `requirements.txt`)

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/neurovision.git
   ```
2. Navigate to the project directory:
   ```bash
   cd neurovision
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the Jupyter Notebook:
   ```bash
   jupyter notebook model.ipynb
   ```

## Usage

1. Load the dataset and preprocess it as per the instructions in the notebook.
2. Train the CNN model using the provided `model.ipynb` notebook.
3. Evaluate the model performance using the provided metrics and analysis tools.

