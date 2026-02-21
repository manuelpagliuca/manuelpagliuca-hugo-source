---
title:  Pain Recognition - Dataset analysis and experimental validation
summary: Test the accuracy of early and late fusion approaches on a multi-modal dataset to classify the presence of pain in patients.
tags:
  - Computer Vision
  - AI
  - Misc
date: "2021-06-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption:
  focal_point: Smart

links:

url_code: "https://github.com/manuelpagliuca/pain-recognition-ml"
url_pdf: "/uploads/Pain_Detection_Manuel_Pagliuca_AC_NI_2022.pdf"
url_slides: ""
# url_video: "about:blank"
url_files: ""
# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.

#slides: example
---
Affective Computing and Natural Interaction courses, Jan 2023, M.Sc. in Computer Science @UniMi

## About the project
This is a unified project for the courses Affective Computing and Natural Interaction at [PhuseLab](https://phuselab.di.unimi.it/), University of Milan, A.Y. 2021/2022.

The aim of this project is to test the accuracy of early and late fusion approaches on a multi-modal dataset to classify the presence of pain in patients. Participants were subjected to an external heat pain stimulus using a physical device.

Facial expressions and biophysical signals were recorded using cameras and electrodes, after which features were extracted. The descriptors from two different modalities were combined by testing both fusion approaches. Finally, classifications and accuracy estimates were made, based on which it was possible to determine that early fusion is the most accurate approach for the dataset considered.
* For more information about the project download the [report](/uploads/Pain_Detection_Manuel_Pagliuca_AC_NI_2022.pdf).

![Diagram](/uploads/diagram.jpg)

Pain stimulation occurs in patients through electrostimulators applied to the wrists. During this experiment, different biophysical signals (GSR, EMG, ...) and facial expressions are recorded using a video camera.

The analysis phase involves extracting features from the video signals using computer vision techniques. The features are Euclidean distances between specific facial landmarks and gradients in five regions of the face.

Once the biophysical signals and video features are ready, fusion techniques are used for classification.
- **Early fusion** involves combining signals and video features before classification, then training the classifier on the combined inputs.
- **Late fusion** involves training three classifiers (of the same type) on different inputs (ECG, GSR, and video). For each sample in the testing set, the prediction is calculated with all three classifiers. The majority prediction is considered correct if it matches the *ground truth*.

The classifier used in this project was *Support Vector Machines*.

### Video feature extraction
## Tools
* IntelliJ IDEA and Python for developing the project application.
* Microsoft Excel for working with the `.csv` files.
* [BioVid](https://ieeexplore.ieee.org/document/6617456) dataset.

## Dependencies
* OpenCV
* MediaPipe
* Sk-learn
* Numpy

## Computer vision techniques
The computer vision techniques used were for the extraction of facial distances, gradients of facial folds, and head position.

### Facial distances and head pose estimation
![Facial Distances](/uploads/facial_distances.gif)

### Gradient for face folds
Gradients allow changes in regions of the face to be assessed. An arithmetic average of pixel values in these regions is calculated.
This average is then weighted by the number of frames in the video window (5 seconds in this dataset).

![Facial Gradients](/uploads/facial_gradients.gif)

### Switch button
A debug branch called `cv-features` in this repository allows you to test computer vision systems directly with your computer's camera. Using the tab key you can enable and disable debugging for gradients.

![Switch](/uploads/switch.gif)

## Ideas for future extensions
- Calculate the gradient only when the pain stimulus is activated and not over the entire window.
- ...