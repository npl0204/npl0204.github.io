---
layout: page
title: Fake News Detection
img: assets/img/15.jpeg
importance: 2
giscus_comments: true
description: project utilizes natural language processing and machine learning models to distinguish between authentic and fraudulent news articles, analyzing performance metrics and overfitting concerns
---
## Overview
- Led a team of four to develop an efficient NLP model to predict the authenticity of 72,134 online news articles.
- Performed text preprocessing such as removing noise, tokenization, lemmatization, performing TF-IDF, etc.
- Examined seven Neural Network models (with Long Short-Term Memory) achieved the highest accuracy (94.51%) and F1 (94.71%) scores.
- Please visit the project using this [link to my notebook](https://drive.google.com/file/d/1OfMiaONZ3jVB1x4l0uJKjn4qcrSGs-dv/view?usp=sharing).

## Details
### Project Proposal
Fake news is a significant concern in the modern digital age, as it can negatively influence perceptions and even lead to real-world incidents. This issue has been exacerbated by the widespread dissemination of misleading information, particularly during the 2016 U.S. election and the onset of the 2020 pandemic. With the majority of U.S. news consumers being worried about the authenticity of news they consume, there's an urgent need for tools to verify news authenticity. The proposed False News Detection project intends to address this problem by creating a tool that uses machine learning and natural language processing to detect fake news. The primary objectives of this project are to reduce the circulation of unreliable articles, boost readers' confidence in news authenticity by providing a reliability score, and caution users against unreliable articles with warning labels.

### Project Description 
This report delves into natural language processing, exploring how machines interpret human communication and contextually process text. The main focus is on distinguishing between "real" and "fake" news using various classification models, including Decision Tree, Logistic Regression, Random Forest, Gradient Boosting, SVM, Multinomial Naive Bayes, and Neural Network with LSTM. The study follows a three-step approach: preprocessing the data, converting text to numeric representation using models like TF-IDF, Count Vectorizer, and Word2Vec, and then classifying this numeric data with advanced machine learning techniques.

### Dataset and Pipeline
The study employed the WELFake dataset from Kaggle, comprising 72,134 news articles, with 35,028 being real and 37,106 being fake. This dataset has four attributes: serial number, title, text, and a label indicating real (1) or fake (0) news. The primary focus during analysis and modeling was the text attribute, given its significance in distinguishing between real and fake news. However, the dataset has limitations, including the absence of links or sources for validation, unclear classification criteria for articles, and uncertainty about the data curation process, which could introduce potential biases.

The project follows a structured pipeline: starting with data collection and cleaning, followed by feature extraction and exploratory analysis. The primary focus for modeling was the text attribute. The dataset was then divided into training and testing sets. The training data was used to train various models, which were subsequently evaluated. If necessary, models were refined and retrained until a satisfactory classification of the articles was achieved.

<div class="col">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/14.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Project Pipeline
</div>

### Data Pre-Processing
In the data pre-processing stage:
1. **Cleaning/Denoising Text:** The text was cleaned by removing non-textual characters using regex and the Unicode library. Commonly used words, or 'stop words,' were removed to enhance the content's meaningfulness. Texts in languages other than English were discarded.
2. **Lemmatization:** Words were reduced to their base form using the Word library from text blobs, which ensures returned words have meaningful roots.
3. **Tokenization:** Texts were split into discrete units or tokens based on spaces using the text blob library, aiding in understanding the text's meaning.
4. **Sentiment Analysis:** The subjectivity and polarity of each text instance were determined using the text blob library, aiming to identify positive or negative sentiments in the text.
5. **Basic Feature Extraction:** Aspects like the number of words, characters, and numerics, along with average word length, were determined. These features were analyzed later in exploratory data analysis.
6. **TF-IDF:** Texts were separated based on their authenticity (real or fake). Word counts for each category were compiled into dictionaries. Term frequency, inverse document frequency, and term frequency-inverse document frequency were computed for titles and texts of both categories. Preliminary findings indicated differences in TF-IDF values between real and fake articles.

### Modeling
**Natural Language Processing Models - Pre-Training Algorithm**
- Two pre-training algorithms, Count Vectorizer and TF-IDF Vectorizer, are utilized to turn textual data into vectors.
- Count Vectorizer tokenizes and creates a vocabulary from text documents.
- TF-IDF Vectorizer calculates term frequency-inverse document frequency values for words.
- For Neural Networks, Word2Vec Vectorizer is used. Word2Vec predicts words in context using two architectures: Continuous Bag of Words (CBOW) and Skip Gram.
**Dataset Split and Overfitting Concerns**
- Initially, the dataset was split 70/30 for training/testing, revealing potential overfitting in some models.
- To address overfitting, the split was changed to 80/20.
**Machine Learning Models**
1. **Decision Tree Classifier**: Uses decision rules to classify data.
2. **Logistic Regression**: Determines the probability of an event using independent variables.
3. **Random Forest Classifier**: Utilizes multiple decision trees for better accuracy.
4. **Gradient Boosting Classifier**: Uses decision trees in series, adjusting based on prior model errors. F1 scores for fake and real instances were 0.90 and 0.92, respectively.
5. **Support-Vector Machines (SVM)**: Separates data using hyperplanes. The F1 scores varied slightly based on the vectorizer used.
6. **Multinomial Naive Bayes**: Uses the Bayes theorem focusing on word frequencies.
7. **Neural Network with LSTM**:
   
<div class="col">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/16.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/17.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Neural Network with Long Short Term Memory (LSTM)
</div>

Addressing issues in regular neural networks, LSTMs provide better performance. Word2Vec was used for word embeddings. After training, the F1 scores were 0.95 for fake news and 0.96 for real news.

In essence, various models were trained with different pre-processing techniques to classify news items. They showed high accuracy and F1 scores, suggesting reliable performance.

### Results and Conlusion
Our study revealed that the Neural Network model was the top performer, achieving the highest accuracy and F1 score, with SVM following closely behind. In contrast, the Multinomial Naive Bayes model lagged behind the others in performance. The Gradient Boosting Classifier and Neural Network models demonstrated good resistance to overfitting. When comparing dataset splits, the 80/20 ratio yielded superior results over the 70/30 split. Impressively, almost all models achieved accuracy and F1 scores above 90%. 

In detail, the Neural Network model's accuracy and F1 scores were approximately 95.90% and 96.10%, respectively, with negligible differences between training and testing scores. The Multinomial Naive Bayes model, however, displayed significant overfitting and lower scores, particularly when comparing training and testing results with the two vectorizers.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/18.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/19.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Models Comparisons
</div>

Overall, while our models achieved commendable outcomes in terms of accuracy and F1 scores, overfitting was identified as an issue in many models. Future endeavors will focus on refining our approach by fine-tuning hyperparameters, exploring different word embeddings, and testing advanced pre-trained models like Transformer and BERT. Additionally, to validate our findings and methods, we plan to test the algorithm on new datasets and revisit our initial preprocessing and data exploration stages.
