# Facial_Expression_Recognition

The goal of this project is to categorize the face in each image based on the emotion shown in the facial expression. The emotion must be classified into one of the following 7 categories: **Angry, Disgust, Fear, Happy, Sad, Surprise, Neutral**. The data for this project can be found at [Kaggle](https://www.kaggle.com/sionehoghen/facial-expression). To achieve this goal, several steps were taken:
- Downloading and processing the data to obtain the paths of the training and test datasets, getting the labels, visualizing the data, etc.
- Using `tensorflow` (version >= 2.0) to create a tensorflow data object with data augmentation
- Creating a model using the `EfficientNetB2` layers. The training process is divided into two steps. The first step is to train the model with a few epochs to allow the pre-trained model (`EfficientNetB2`) to adjust its weights to the images we are working on. Second step, we have frozen the first layer related to the pre-trained model and trained the last layers related to the classification task.
- Saving the best weights that have been trained and use them later for validation.
- Deploying the created model using all encoders, best weights and the trained model. The deployment was performed on a local computer using its camera.

The deployment task must be conducted carefully as some libraries need to be installed. To start with the local configuration, I suggest you install python in your system using anaconda.
Then follow the instructions given [here](https://uoa-eresearch.github.io/eresearch-cookbook/recipe/2014/11/20/conda/) to create a virtual environment with all the libraries needed for this project.

The required libraries that need to be installed in the virtual environment are :

- **Python 3.6.8** when creating the virtual environment: 
```
# conda create -n yourenvname python=3.6.8 anaconda
```

- **Tensorflow** (must be greater than 2.0): 
```
# pip install tensorflow 
```
or 
```
# conda install -c conda-forge tensorflow  
```

- **OpenCV**: 
```
# conda install -c anaconda opencv
```

- **cmake**: 
```
# conda install -c anaconda cmake
```

- **dlib**: 
```
# conda install -c conda-forge dlib 
``` 
