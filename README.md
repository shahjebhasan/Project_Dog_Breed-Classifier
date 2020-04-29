# Project_Dog_Breed-Classifier
In this project the code will accept any user-supplied image as input. If a dog is detected in the image, it will provide an estimate of the dog's breed. If a human is detected, it will provide an estimate of the dog breed that is most resembling. 

## Detect Humans
The submission returns the percentage of the first 100 images in the dog and human face datasets that include a detected, human face.

## Detect Dogs
Use a pre-trained VGG16 Net to find the predicted class for a given image.
The submission returns the percentage of the first 100 images in the dog and human face datasets that include a detected dog.

## Create a CNN to Classify Dog Breeds
loaded in the training, test and validation data separately and did the data transformation by (transforms.Compose) then created DataLoaders for each of these sets of data seperately.
# CNN Architecture:-
  (conv1): Conv2d(3, 16, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1))
  (conv2): Conv2d(16, 32, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1))
  (conv3): Conv2d(32, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1))
  (pool): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)
  (fc1): Linear(in_features=50176, out_features=500, bias=True)
  (fc2): Linear(in_features=500, out_features=133, bias=True)
  (dropout): Dropout(p=0.25)
	
	used CrossEntropyLoss and SGD Optimizer
	
## Create a CNN Using Transfer Learning
The submission specifies a model architecture that uses part of a pre-trained model.
Accuracy on the test set is 81% or greater.

## Algorithm
Accepts a file path to an image and first determines whether the image contains a human, dog, or neither. Then,

A.if a dog is detected in the image, return the predicted breed.
B.if a human is detected in the image, return the resembling dog breed.
C.if neither is detected in the image, provide output that indicates an error.

## Test Your Algorithm
The submission tests at least 6 images, including at least two human and two dog images.
