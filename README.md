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
  

(2) We replaced our basic CNN model with resnet-18

ResNet-18 is a convolutional neural network that is 18 layers deep. The pretrained network can classify images into 1000 object categories, such as keyboard, mouse, pencil, and many animals. In our advanced model, we chose not to use pretrained resnet-18 first and would like to train it with our dataset.

For more information about resnet-18, here is the link: https://www.mathworks.com/help/deeplearning/ref/resnet18.html



## Advanced Model Exeperiement with Semi-Supervised

### Conclusion: 

(1) Train our advanced model with hyperparameter below and no Semi-Supervised.

| Item                      | Value            |
|---------------------------|------------------|
| Pretrained                | False            |
| Epoch                     | 30               |
| Learning Rate             | le-4             |
| Semi-Supervised threshold | N/A              |
| Loss Function             | CrossEntropyLoss |
| Optimizer                 | Adam             |
| Weight Decay              | le-5             |
| Scheduler                 | ExponentialLR    |
| Gamma                     | 0.9              |



![image](https://user-images.githubusercontent.com/86508922/176345718-0d59039e-dfd5-46f3-bee6-8009bed63b6e.png)

![image](https://user-images.githubusercontent.com/86508922/176345724-85039ecc-4759-4a03-9832-2068a15c868d.png)

![image](https://user-images.githubusercontent.com/86508922/176345735-ec0f44d8-60eb-4098-b9bb-95d0b252d81b.png)



(2) Trained our advanced model with hyperparameter below and implmented Semi-Supervised with threshold as 0.6.


| Item                      | Value            |
|---------------------------|------------------|
| Pretrained                | False            |
| Epoch                     | 30               |
| Learning Rate             | le-4             |
| Semi-Supervised threshold | 0.6              |
| Loss Function             | CrossEntropyLoss |
| Optimizer                 | Adam             |
| Weight Decay              | le-5             |
| Scheduler                 | ExponentialLR    |
| Gamma                     | 0.9              |

![image](https://user-images.githubusercontent.com/86508922/176346478-e1e666d8-da78-41ab-b015-59844f9520d9.png)

![image](https://user-images.githubusercontent.com/86508922/176346488-0e47f62d-ebb9-4546-a432-46fe978a26ac.png)

![image](https://user-images.githubusercontent.com/86508922/176346493-3537e842-a7ba-4d2d-a2b8-1f2a90955cd0.png)



(3) Trained our advanced model with hyperparameter below and implmented Semi-Supervised with threshold as 0.9.

| Item                      | Value            |
|---------------------------|------------------|
| Pretrained                | False            |
| Epoch                     | 30               |
| Learning Rate             | le-4             |
| Semi-Supervised threshold | 0.9              |
| Loss Function             | CrossEntropyLoss |
| Optimizer                 | Adam             |
| Weight Decay              | le-5             |
| Scheduler                 | ExponentialLR    |
| Gamma                     | 0.9              |

![image](https://user-images.githubusercontent.com/86508922/176346518-b79ee665-e968-4527-8d88-7add3c3a2c08.png)

![image](https://user-images.githubusercontent.com/86508922/176346530-9eb7394b-b89c-4131-b07d-6f2b9b2a7993.png)

![image](https://user-images.githubusercontent.com/86508922/176346540-1802fa40-8343-43a5-abfb-59571598c6fd.png)



## Pretrained Model Exeperiement with Semi-Supervised



![image](https://user-images.githubusercontent.com/86508922/176346348-ead3928f-514f-4af0-a5ad-1d10593b4f17.png)

![image](https://user-images.githubusercontent.com/86508922/176346361-06cf9734-7447-49f1-88e3-2359f0d30113.png)

![image](https://user-images.githubusercontent.com/86508922/176346376-ee7f0bb8-16f9-4cdd-a086-8e001e9cf85b.png)
