# Central-Asian-Food-Dataset
Central Asian Food Dataset (CAFD) for food classification contains 16,499 images across 42 food classes of Central Asian cuisine. The dataset is web-scraped and manually annotated. Images have various resolution.
Figure below illustrates the samples and name for each class.

<img src="https://github.com/IS2AI/Kazakh-Food-Dataset/blob/main/figures/samples.png" width="750" height="700">

The dataset is unbalaced. The statistics across all 42 classes is shown on Figure below.

<img src="https://github.com/IS2AI/Kazakh-Food-Dataset/blob/main/figures/stats_plot.png" width="500" height="600">

# Download the dataset

The dataset can be downloaded using the link below. If there are some issues with the link, please, email us on issai@nu.edu.kz

https://drive.google.com/drive/folders/1mnfShcKkADjESW9_TuOT9_m5IhhZg1h6?usp=sharing

# Pre-trained models

To illustrate the performance of different classification models on CAFD we have trained different models. We used the largest publicly available fine-grained dataset Food1K [[1]](#1) that contains 1,000 food classes to evaluate the performance of classifier with the 1,042 food categories.

|Model| CAFD (Top-1 Acc.)| CAFD (Top-5 Acc.)| Food1K+CAFD (Top-1 Acc.)| Food1K+CAFD (Top-5 Acc.)|
|-----|-----------------|-----------------|------------------------|------------------------|
|VGG-16|86.03|98.33|80.87|96.19|
|Squeezenet1_0|79.58|97.29|69.16|90.15|
|ResNet50|88.03|98.44|83.22|97.25|
|ResNet101|88.51|98.44|84.20|97.45|
|ResNet152|88.70|98.59|84.75|97.58|
|ResNext50_32|87.95|98.44|84.81|97.65|
|Wide ResNet-50|88.21|98.59|85.27|97.81|
|DenseNet-121|86.95|98.26|82.45|96.93|
|EfficientNet-b4|81.28|97.37|87.75|98.01|

Pre-trained model weights of the best performing models: ResNet152 on KFD and EfficientNet-b4 on Food1K+KFD can be downloaded using these links:

## ResNet152 trained on CAFD: 

https://drive.google.com/drive/folders/1DWLxzN2O2eeLSdKripfWCSTJnOnQNuU2?usp=share_link

## EfficientNet-b4 trained on Food1K+CAFD:

https://issai.nu.edu.kz/wp-content/themes/issai-new/data/models/KFD_pre_trained_models/food1k_kfd_efficientnet.pt

## Model training and testing

To train and test using pre-trained models use train.py and test.py files. 

## References
<a id="1">[1]</a> 
Min, Weiqing and Wang,  Zhiling (2021). 
Large Scale Visual Food Recognition. 
arXiv.

