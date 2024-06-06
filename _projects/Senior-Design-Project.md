---
layout: page
title: Health Outcome Predictions with Data Transformation and Machine Learning
img: assets/img/poster.jpeg
importance: 0
giscus_comments: true
description: Supervised by Dr. Hegler Tissot
---

## Abstract
Machine learning's integration into healthcare has significantly advanced our ability to analyze and predict complex datasets. However, challenges remain in efficiently processing and predicting health outcomes from sparse and heterogeneous patient records. This study aims to address these challenges by evaluating three different machine learning methods: XGBoost with a tabular dataset, LSTM with a time series dataset, and a hybrid XGBoost then LSTM method. We utilize a synthetic COVID-19 patient dataset to assess the performance of these methods. Our results indicate that the XGBoost model achieves the highest F1 score (0.5199) with the shortest training time (151.42 seconds), demonstrating its efficiency and effectiveness. The LSTM model, despite capturing temporal dependencies, shows a significantly lower F1 score (0.2781) and the longest training time (approximately 8.66 days), highlighting its computational inefficiency and overfitting issues. The hybrid method improves over the standalone LSTM model but still falls short of XGBoost's performance in both accuracy and computational efficiency. These findings underscore the potential of using 2D models like XGBoost to effectively replace more complex 3D models, potentially leading to broader application and faster implementation in clinical settings, thereby enhancing the ability to provide timely and accurate patient care.

## Poster
<div class="col">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/poster.jpeg" title="poster" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

## Paper
Please visit the research using this [link to my paper]([https://github.com/npl0204/npl0204.github.io/blob/master/assets/pdf/DREXEL_SENIOR_23_24_Linh.pdf]).
