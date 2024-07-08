<div align="center">
 
![logo](https://github.com/souvikmajumder26/Land-Cover-Semantic-Segmentation-PyTorch/blob/main/assets/logo2.jpg)  

<h1 align="center"><strong>🛣 Land-Cover-Semantic-Segmentation-PyTorch:<h6 align="center">An end-to-end Image Segmentation (CV) project</h6></strong></h1>

![PyTorch - Version](https://img.shields.io/badge/PYTORCH-2.0+-red?style=for-the-badge&logo=pytorch)
![Python - Version](https://img.shields.io/badge/PYTHON-3.9+-blue?style=for-the-badge&logo=python&logoColor=white)
[![Generic badge](https://img.shields.io/badge/License-MIT-<COLOR>.svg?style=for-the-badge)](https://github.com/souvikmajumder26/Land-Cover-Semantic-Segmentation-PyTorch/blob/main/LICENSE) 
[![GitHub Issues](https://img.shields.io/github/issues/souvikmajumder26/Land-Cover-Semantic-Segmentation-PyTorch.svg?style=for-the-badge)](https://github.com/souvikmajumder26/Land-Cover-Semantic-Segmentation-PyTorch/issues)
![Contributions welcome](https://img.shields.io/badge/contributions-welcome-orange.svg?style=for-the-badge)

</div>

----
 
## 📚 Table of Contents
- [Overview](#overview)
- [Demo](#demo)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Setting up and Running the project with Docker](#with-docker)
  - [Setup without Docker](#setup)
  - [Running the project without Docker](#running-the-project)
- [Citing](#citing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

----

## 📌 Overview <a name="overview"></a>
An end-to-end Computer Vision project focused on the topic of <a href="https://en.wikipedia.org/wiki/Image_segmentation" target="_blank">Image Segmentation</a> (specifically Semantic Segmentation). Although this project has primarily been built with the <a href="https://landcover.ai.linuxpolska.com/" target="_blank">LandCover.ai dataset</a>, the project template can be applied to train a model on any semantic segmentation dataset and extract inference outputs from the model in a <b>promptable</b> fashion. Though this is not even close to actual promptable AI, the term is being used here because of a specific functionality that has been integrated here.

The model can be trained on any or all the classes present in the semantic segmentation dataset with the ability to customize the model architecture, optimizer, learning rate, and a lot more parameters directly from the config file, giving it an <b>exciting AutoML</b> aspect. Thereafter while testing, the user can pass the prompt (in the form of the config variable '<b>test_classes</b>') of the selected classes that the user wants to be present in the masks predicted by the trained model.

For example, suppose the model has been trained on all the 30 classes of the <a href="https://www.cityscapes-dataset.com/" target="_blank">CityScapes dataset</a> and while inferencing, the user only wants the class <b>'parking'</b> to be present in the predicted mask due to a specific use-case application. Therefore, the user can provide the prompt as '<b>test_classes = ['parking']</b>' in the config file and get the desired output.

----

## 💫 Demo <a name="demo"></a>
 <p>
  1. Training the model on <a href="https://landcover.ai.linuxpolska.com/" target="_blank">LandCover.ai dataset</a> with '<b>train_classes</b>': <b>['background', 'building', 'woodland', 'water']</b>...
 </p>
 <p align="center">
  <img width="60%" src="https://github.com/souvikmajumder26/Land-Cover-Semantic-Segmentation-PyTorch/blob/main/assets/training.png">
 </p>
 <p>
  2. Testing the trained model for all the classes used to train the model, i.e. '<b>test_classes</b>': <b>['background', 'building', 'woodland', 'water']</b>...
 </p>
 <p align="center">
  <img width="90%" src="https://github.com/souvikmajumder26/Land-Cover-Semantic-Segmentation-PyTorch/blob/main/assets/all_classes.png">
 </p>
 <p>
  3. Testing the trained model for selective classes as per user input, i.e. '<b>test_classes</b>': <b>['background', 'building', 'water']</b>...
 </p>
 <p align="center">
  <img width="90%" src="https://github.com/souvikmajumder26/Land-Cover-Semantic-Segmentation-PyTorch/blob/main/assets/select_classes.png">
 </p>

---

<p align="right">
 <a href="#top"><b>🔝 Return </b></a>
</p>

---
