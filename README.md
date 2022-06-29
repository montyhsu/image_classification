# Apply CNN to Identify Food Images

This project is the final delivery for the course MSDS631.

## Description

People loves to share the foods they love in social media platforms today, and by labeling these food images could help the platforms plan better advertising projection and increase the metrics such as click through rate for adversting.

In this project, we would like to utilize CNN to build a food classifcation model with several deep learning optimization skills like augmentation, semi-supervised, and pre-trained model applications. 


## Dataset Source

The dataset we use is a subset of Food-11 image dataset(https://www.kaggle.com/trolukovich/food11-image-dataset) from Kaggle.

  ● Training set: 280 * 11 labeled images + 6786 unlabeled images

  ● Validation set: 60 * 11 labeled images

  ● Testing set: 3347 images



## Basic Model Development

## Basic Model Exeperiement with Semi-Supervised

## Advanced Model Development

We took two improvement on the advanced model.

(1) We implemented augmentation to help us generate more data in training and validation dataset. 

  ● transforms.RandomResizedCrop(size=256, scale=(0.8, 1.0))
  
  ● transforms.Resize(256)
  
  ● transforms.RandomRotation(degrees=15)
  
  ● transforms.CenterCrop(size=224)
  
  ● transforms.RandomResizedCrop(size=256, scale=(0.8, 1.0))
  

(2) We utilize resnet-18 as our CNN training model 

https://www.mathworks.com/help/deeplearning/ref/resnet18.html

## Advanced Model Exeperiement with Semi-Supervised

![image](https://user-images.githubusercontent.com/86508922/176341831-d6df756d-4498-4ab7-8ed7-4e9ed0168caa.png)


## Pretrained Model Exeperiement with Semi-Supervised
