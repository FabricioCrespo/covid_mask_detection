# Covid Mask Classification Pipeline

This repository contains the necessary notebooks to traing, test, and probe different Deep Learning models in order to classify the incorrect use of face masks for COVID-19 awareness. 

## Structure of this repo:

```
📦covid_mask_detection
 ┣ 📂colab_notebooks
 ┃ ┣ 📂analyzing_results
 ┃ ┃ ┣ 📜covid_mask_classification_GradCams.ipynb
 ┃ ┃ ┣ 📜mask_classification_analysis_2classes.ipynb
 ┃ ┃ ┗ 📜mask_classification_analysis_3classes.ipynb
 ┃ ┣ 📂make_detections
 ┃ ┃ ┣ 📜detect_on_video_facenet.ipynb
 ┃ ┃ ┗ 📜detect_on_video_retinaface.ipynb
 ┃ ┗ 📂trainings
 ┃ ┃ ┗ 📜training_covid_mask_models.ipynb
 ┣ 📜.gitignore
 ┣ 📜LICENSE
 ┗ 📜README.md

```

## Description of main files

- [training_covid_mask_models.ipynb](colab_notebooks/trainings/training_covid_mask_models.ipynb) : This notebook let us to make trainings using different Deep Learning models available in TorchHub. Here, we used Resnet, ResneSt and Efficienet architecture. In the same way, we can test the models obtained after the training.

- [detect_on_video_retinaface.ipynb](colab_notebooks/make_detections/detect_on_video_retinaface.ipynb) : This notebook allow us to make detections in custom videos using RetinaFace as the detection model.

- [detect_on_video_facenet.ipynb](colab_notebooks/make_detections/detect_on_video_facenet.ipynb) : This notebook allow us to make detections in custom videos using Facenet as the detection model. FaceNet is an alternative detection model to the RetinaFace used on this work but. Facenet is less 
accurate.

- [mask_classification_analysis_2classes.ipynb](colab_notebooks/analyzing_results/mask_classification_analysis_2classes.ipynb) and [mask_classification_analysis_3classes.ipynb](colab_notebooks/analyzing_results/mask_classification_analysis_3classes.ipynb) are notebooks with the neccesary code to analyze the predictions made by a classification model. Some useful tools presented in these notebooks are code to plot filters, feature maps, the architecture of a model and the wrong predictions by class.

- [covid_mask_classification_GradCams.ipynb](colab_notebooks/analyzing_results/covid_mask_classification_GradCams.ipynb) : This notebook let us to plot the Grad-CAMS for the wrong predictions. Grad-CAMS are useful to determine the regions of an image the model focus on to make a prediction. 


## Datasets

The dataset is publicy available on Google Drive. It is a merge between the FMLD dataset and the Medical Mask Dataset. 

- Two classes dataset:[Google Drive link](https://drive.google.com/drive/folders/15HORjeYRJ-u7BeW6KZa_E0i7AUWmu_2V?usp=sharing)

- Three classes dataset: [Google Drive link](https://drive.google.com/drive/folders/1bWnqBIES8xdlHYjuyP0f14X5uld4eJaF?usp=sharing)