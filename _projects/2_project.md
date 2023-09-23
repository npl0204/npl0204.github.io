---
layout: page
title: Brain Tumor Detection from MRI Images with Deep Learning
img: assets/img/10.png
importance: 2
giscus_comments: true
---
## Overview
- Led a team of four to develop an efficient NLP model to predict the authenticity of 72,134 online news articles.
- Performed text preprocessing such as removing noise, tokenization, lemmatization, performing TF-IDF, etc.
- Examined seven Neural Network models (with Long Short-Term Memory) achieved the highest accuracy (94.51%) and F1 (94.71%) scores.
- Please visit the project using this [link to my notebook](https://drive.google.com/file/d/1OfMiaONZ3jVB1x4l0uJKjn4qcrSGs-dv/view?usp=sharing).

## Details
### Project Proposal
Fake news is a significant concern in the modern digital age, as it can negatively influence perceptions and even lead to real-world incidents. This issue has been exacerbated by widespread dissemination of misleading information, particularly during the 2016 U.S. election and the onset of the 2020 pandemic. With the majority of U.S. news consumers being worried about the authenticity of news they consume, there's an urgent need for tools to verify news authenticity. The proposed False News Detection project intends to address this problem by creating a tool that uses machine learning and natural language processing to detect fake news. The primary objectives of this project are to reduce the circulation of unreliable articles, boost readers' confidence in news authenticity by providing a reliability score, and caution users against unreliable articles with a warning label.

### Contributions in the Project Domain 
- Synthesizing of contrasts using DL to correct distortions in MRI scans
- Creating and leveraging several DL models like DeepBrainNet to construct accurate classifiers for brain diseases
- Leveraging probabilistics labels for enhanced image-based diagnostics
- Vast analysis of the current limitations, benefits and future prospects in Medical Imaging Diagnosis

### Project Goals and Benefits
1. Goals
   - Develop a deep learning model for accurate brain tumor classification.
   - Improve early detection and classification of brain tumors using advanced techniques.
2. Benefits
   - Better Patient Outcomes: Early detection and accurate classification enable timely intervention and tailored treatment plans.
   - Enhanced Healthcare Efficiency: Early detection reduces invasive procedures, healthcare costs, and optimizes resource allocation.
   - Empowering Healthcare Providers: Reliable deep learning model assists in accurate diagnoses, reducing manual analysis burden.
   - Advancement in Research and Knowledge: Contributes to the knowledge base in brain tumor detection, fostering collaboration and advancements.

## Deep Learning and Explorations
### Project Components - Data Set
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

### Project Components - Preprocessing
I set up data generators for image processing and augmentation using the Keras ImageDataGenerator. This technique allowed me to artificially increase the size of the training dataset and improve the generalization ability of my model. This, in turn, helped me address the problem of overfitting and made my model more robust, enabling it to handle different types of images.

I used these data generators to provide augmented images in batches during model training, testing, and validation processes.

With this approach, my model was able to learn from a wider range of examples, enabling it to perform well on new, unseen images.

### Deep Learning Models Used + Performance 
I employed a range of deep learning models in my project, each serving a specific purpose:

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Performance of 5 Models
</div>

1. **MLP (Multi-Layer Perceptron):** This model was widely utilized for both classification and regression tasks, showcasing its versatility in handling various data types.
2. **CNN (Convolutional Neural Network):** For image processing tasks, I turned to CNN, a well-established choice known for its effectiveness in handling visual data.
3. **VGG16:** This model was specifically chosen for image classification tasks, as it has a proven track record of achieving high accuracy in this domain.
4. **EfficientNetB2:** My project benefited from the impressive performance of EfficientNetB2. This member of the EfficientNet family offers improved accuracy and efficiency for image-related training tasks. It utilizes a novel scaling technique that uniformly adjusts network dimensions, including width, depth, and image resolution, resulting in optimal performance without the need for manual tuning.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/12.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

5. **InceptionV3:** To further enhance image recognition capabilities, I employed InceptionV3. This advanced model incorporates a variety of building blocks and techniques to achieve outstanding performance. Its architecture features both symmetric and asymmetric building blocks, including convolutional layers, average pooling, max pooling, concatenations, dropouts, and fully connected layers. The extensive use of batch normalization enhances stability and speeds up the training process. Moreover, InceptionV3 employs the softmax function for loss computation, a crucial component in multi-class classification tasks like image recognition.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/13.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

In terms of performance, EfficientNet and InceptionV3 stood out as the top performers in my project, demonstrating their capability to excel in computer vision tasks and image-related challenges.

### Nest Steps
For fine-tuning and optimizing the model, I undertook the following steps:

1. **Architectural Modifications:** I made adjustments to the model's architecture, including alterations to hyperparameters and regularization techniques, in order to enhance its performance.

2. **Data Augmentation:** I implemented additional data augmentation methods, such as image cropping, to improve the quality of training data and the model's ability to generalize effectively.

3. **Optimization Strategies:** I conducted experiments with various optimization strategies, exploring different learning rates, batch sizes, and regularization techniques. This iterative process aimed to fine-tune the model's parameters for optimal performance.

In the pursuit of continual refinement and evaluation:

1. **Dataset Variation:** To ensure the model's robustness, I tested it on various datasets and augmented data sources, verifying its consistent and reliable performance across different scenarios.

2. **Performance Analysis:** I rigorously analyzed the model's outputs and systematically made improvements based on the evaluation results, ensuring that it continued to meet the desired performance criteria.

Regarding documentation:

1. **Comprehensive Documentation:** I diligently documented the entire development process, capturing the methods employed and the results obtained. This documentation provided transparency and served as a valuable resource for future reference.

2. **Ongoing Documentation:** This documentation process was not a one-time effort; I maintained it throughout the further refinement and optimization stages, ensuring that each iteration and improvement was well-documented for a complete record of the project's evolution.
