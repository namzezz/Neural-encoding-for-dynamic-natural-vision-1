
ECoG and Visual Stimuli Processing Documentation
------------------------------------------------

Objective:
-----------
The main goal is to train a model that can predict visual stimuli (images) from iEEG data. The hypothesis is that the iEEG data, which is electrical activity from the brain, will have patterns that correlate with the visual stimuli the subject was seeing.

Steps Taken:
-------------
1. **Data Acquisition**:
    - The data consisted of `.mat` files containing iEEG segments and `.tsv` files containing event details.
    - Each iEEG segment corresponds to an event, which has an associated visual stimulus.

2. **Data Preprocessing**:
    - The iEEG segments were paired with the corresponding visual stimuli based on the events.tsv files.
    - This resulted in a dataset where each entry consists of an iEEG segment and a visual stimulus image.

3. **Model Building**:
    - A Convolutional Neural Network (CNN) was designed to take in the iEEG data and predict the visual stimulus.
    - The model was trained in batches due to memory limitations.

4. **Model Evaluation**:
    - The trained model was then used to predict visual stimuli from test iEEG data.
    - The predictions were compared with the actual visual stimuli to evaluate the model's performance.

Challenges:
------------
- **Data Size**: The iEEG data segments and visual stimuli images are large, which can cause memory issues during training.
- **Complexity**: Predicting visual stimuli from iEEG data is a complex task. The neural patterns in the brain that correspond to visual stimuli are intricate and can be influenced by various factors.

Next Steps for Improvement:
----------------------------
1. **Data Augmentation**: Increase the dataset size by applying transformations to the existing data, such as rotations and flips.
2. **Complex Models**: Explore more complex models like autoencoders or transformer-based models.
3. **Feature Extraction**: Instead of using raw iEEG data, extract meaningful features that could be more informative for the model.
4. **Regularization**: Apply techniques like dropout or weight decay to prevent overfitting.
5. **Hyperparameter Tuning**: Systematically search for the best hyperparameters for the model.
6. **Domain Knowledge**: Incorporate knowledge from neuroscience to inform the model-building process.

Remarks on the Stimuli Image Portion:
--------------------------------------
The visual stimuli images used in the project were portions of the original stimuli. This could be due to various reasons:
- **Focus on Regions of Interest**: The research might have been focused on specific regions of the visual stimuli that are most relevant or evoke the strongest neural responses.
- **Data Reduction**: Using portions of the stimuli can reduce the data size, making processing more manageable.
- **Experiment Design**: The experiment from which the data was collected might have been designed in a way that only portions of the stimuli were shown to the subjects
