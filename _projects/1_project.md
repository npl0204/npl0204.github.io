---
layout: page
title: Brain Tumor Detection from MRI Images with Deep Learning
img: assets/img/10.png
importance: 1
---
## Overview
- Developed deep learning models for brain tumor detection using MRI images by employing MLP, CNN, VGG16, EfficientNet B2, and InceptionV3 models. Achieved the best performance using InceptionV3 with an F1 score of 93.55% and an accuracy score of 94.74%.
- Performed pre-processing using data generators for image processing and augmentation with the ImageDataGenerator.
- Please visit the project using this [link to my notebook](https://colab.research.google.com/drive/1toTysuD14OgQ2ZWOpBp9GFO4iaahBt57?usp=sharing).

## Details
#### Project Description:
- Brain tumors are becoming increasingly prevalent, posing a significant healthcare challenge.
- This rising occurrence necessitates early detection for effective treatment.
- Deep Learning can be used to analyze complex data and identify patterns for medical image analysis. 
- It can be leveraged to enhance accuracy, speed, and efficiency in diagnosing diseases.  
- Our project aims to contribute to the development of systems that can identify these fatal diseases in their initial stages. 
- Our objective is to develop a precise deep learning model for accurate classification of brain MRI images with tumors to improve early detection of brain tumors, leading to better patient outcomes. 

#### Contributions in the Project Domain 
- Synthesizing of contrasts using DL to correct distortions in MRI scans
- Creating and leveraging several DL models like DeepBrainNet to construct accurate classifiers for brain diseases
- Leveraging probabilistics labels for enhanced image-based diagnostics
- Vast analysis of the current limitations, benefits and future prospects in Medical Imaging Diagnosis

#### Project Goals and Benefits
1. Goals
   - Develop a deep learning model for accurate brain tumor classification.
   - Improve early detection and classification of brain tumors using advanced techniques.
2. Benefits
   - Better Patient Outcomes: Early detection and accurate classification enable timely intervention and tailored treatment plans.
   - Enhanced Healthcare Efficiency: Early detection reduces invasive procedures, healthcare costs, and optimizes resource allocation.
   - Empowering Healthcare Providers: Reliable deep learning model assists in accurate diagnoses, reducing manual analysis burden.
   - Advancement in Research and Knowledge: Contributes to the knowledge base in brain tumor detection, fostering collaboration and advancements.

## Deep Learning and Explorations
#### Project Components - Data Set
The image data came from the [Brain MRI Images for Brain Tumor Detection](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection) dataset. It consists of MRI scans of two classes, stored in separate files:
- NO (98) - no tumor, encoded as 0
- YES (155) - tumor, encoded as 1
<div class="col">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/9.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/8.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Combined the two files of classes into a single dataframe - tumor_df
</div>

#### 


