# Visual sentimen analysis using CNN

The project contains main findings related with transfer learning using Tensorflow, Keras, fast.ai and D2L and test new proposed architectures. All of them are Convolutional Neural Networks (CNN) and for the best training model fine tunning techniques have been applied.

Access to hardware is a barrier to training more epochs, more deep networks or use big datasets.

## Technical requierements

Hardware is a main issue when you try to training CNN. The models presented in this document were tested using Google Colab Pro and a AWS EC2 instance.

Colab PRO is a paid service thah offer more RAM compared with free version and access to better GPU, but this access is limited in process time and hardware. Information related with this service could be consult in https://colab.research.google.com/signup#

Characteristics for EC2 instance:

Architecture:        x86_64
CPU op-mode(s):      32-bit, 64-bit
Byte Order:          Little Endian
CPU(s):              16
On-line CPU(s) list: 0-15
Thread(s) per core:  2
Core(s) per socket:  8
Socket(s):           1
NUMA node(s):        1
Vendor ID:           GenuineIntel
CPU family:          6
Model:               63
Model name:          Intel(R) Xeon(R) CPU E5-2666 v3 @ 2.90GHz
Stepping:            2
CPU MHz:             2900.139
BogoMIPS:            5800.10
Hypervisor vendor:   Xen
Virtualization type: full
L1d cache:           32K
L1i cache:           32K
L2 cache:            256K
L3 cache:            25600K
NUMA node0 CPU(s):   0-15

## Datasets

The models included in this document were training on "Users" dataset and testing for "Users Boston City", as a part of "Visual Sentiment Analysis for Review Images with
Item-Oriented and User-Oriented CNN" writed by Truong et.al in 2017 and reviewed in 2020 as "Reproducibility Companion Paper: Visual Sentiment Analysis for Review Images with Item-Oriented and User-Oriented CNN" by the same authors. 

Datasets could be download follow the instructions in https://github.com/PreferredAI/vs-cnn/tree/reproducibility

Users dataset -used for training- consist of 45.646 images from YELP reviews and Users Boston dataset has 1.194 images for validation.

All of the datasets included in mentioned documents could not be used due to their size and restrictions related with hardware avalaible.

## Models

According to the articles mentioned, Truong et.al propose the following architecture for the problem of binary sentiment classification based on images:

![Architecture used by Truong et.al](/Images/acmmm17.PNG)

* __"Réplica"__ model try to training a similar architecture with augmented data, early stoping and l2 regularization
* __"Best"__ dir contains model with best results, based on AutoKeras
* __AK_FULL__ first AutoKeras, used to propose other architectures
* __ALPropio__ architecture based on AlexNet, augmented data and l2 regularization
* __BasedOnAlexnet__ architectural proposal based on AlexNet
* __FT_Modelo1__ Fine tunning to Model1
* __"Inception"__ model training this architecture type. Input size is 96 due to computational restrictions
* __ModelPAdjusted__ model with regularization, data augmentation and initializers. __It was a base model__
* __Modelo1__ another AutoKeras model
* __Propio__ a model proposed by the author of this project
* __ResNet18__ a model using residual nets and fast.ai
* __TFM2__ a model based on VGG16 with fine tunning
* __DenseNet__ a proposal using DenseNet concepts
* __VGG16__ a fast.ai model using VGG19

## Results

Table below summarise main findings

![Main results](/Images/Results.PNG)
