# Dog App CNN
## Introduction
This is one of [Deep learning nanodegree](https://classroom.udacity.com/nanodegrees/nd101/parts/2e8d3b5d-aa70-4376-946f-0cdc37127d7d/modules/49d2e25d-6df2-48df-8ccd-88417ae208fc/lessons/368c9af3-c8b8-4b01-92ba-40d7e989d6e7/concepts/900d740a-e47d-4b67-be4c-ca27ea8981e2) major projects.
In this project, I learned how to build a pipeline to process real-world, user-supplied images. Given an image of a dog, my algorithm will identify an estimate of the canine’s breed. If supplied an image of a human face, the code will identify the resembling dog breed. Along with exploring state-of-the-art CNN models for classification, I made important design decisions about the user experience for your app.

## Dataset
I used [Dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip) and [Human dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip)

## Trails 
 ### Part1
 
 To reach my best model i have tried many architicuture combination which can be summarized as follows:
 ``` python
  num_conv_layers = [2-layers , 3-layers]
  num_neurons = [16 , 32 , 64 , 128]
  dropout = [0.3 , 0.5]
  num_dense_layes = 2
  Learning_rates = [0.02 , 0.002 , 0.2 , 0.001]
```
- I started with the simple model that i was practising in the exercises , it was not doing well.

- I tried to make a deep model to capture more features. It actually did well , but in the training loss only. The model was overfitting as the validation loss was increasing while training loss was decreasing.

- I started putting dropout after the last conv layer , then after every conv layer. In addition i tried to use a less complex model , by reducing the number of nodes in linear layers of conv layer. This made the performance improve a little.

- Then, i started to consider transformations in the dataset preprocessing , which solved the problem and hits the desired accuracy.

#### Results 
```
Training Loss: 3.145872 	Validation Loss: 4.041088 and Accuracy of 12 %
```
### part 2

I tried to use the poteintial of transfer learning to make a better model , so i used resnet50 as base model and added by classification layer to it and started traing this classification layer.

#### Results 
```
Training Loss: 0.618823 	Validation Loss: 0.978713 and Accuracy of 76 % 
```

## UE and results 

You can find results and UE at step 6 in this [report](https://github.com/MG-98/dog-app-CNN/blob/main/report.html)


